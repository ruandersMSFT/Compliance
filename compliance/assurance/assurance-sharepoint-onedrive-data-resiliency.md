---
title: "SharePoint and OneDrive data resiliency in Microsoft 365"
description: In this article, find an explanation of the various aspects of data resiliency within SharePoint and OneDrive and Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
---

# SharePoint and OneDrive data resiliency in Microsoft 365

Within Microsoft 365, OneDrive is built on top of the SharePoint file platform; for the remainder of the document only SharePoint will be used to refer to both products.

There are two primary assets that make up the core content storage of SharePoint:

- **Metadata**: Metadata about each file is stored in Azure SQL Database. Azure SQL offers a complete business continuity story that SPO takes full advantage of and is outlined in greater detail below.
- **Blob storage**: User content that is uploaded into SharePoint is stored in Azure Storage. SharePoint has built a custom resiliency plan on top of Azure Storage to ensure near real-time duplication of user content and a truly active/active system.

The complete set of controls to ensure data resiliency is explained in further sections.

>[!Note]
>The contents of this article are relevant to Microsoft 365 and do not apply to consumer services.

## Blob storage resilience

SharePoint has a custom-built solution for storage of customer content in Azure Storage. Every file is simultaneously written into both a primary and a secondary datacenter region (fig 1 below). If writes to either Azure region fail, the file save will fail. After the contents are written into Azure Storage, checksums are stored separately with metadata, and are used to ensure that the committed write is identical to the original file sent to SharePoint during all future reads. This same technique is used in all workflows to prevent propagation of any corruption that should occur. Within each region, Azure Locally Redundant Storage (LRS) provides an extremely high level of reliability. See the [Azure Storage redundancy](https://docs.microsoft.com/azure/storage/common/storage-redundancy-lrs) article for details.

SharePoint uses Append-Only storage. This ensures that files cannot be changed or corrupted after an initial save, but also by using in-product versioning, any previous version of the file contents can be retrieved.

SharePoint environments in either datacenter can access storage containers in both Azure regions. For performance reasons the storage container in the same local datacenter is always preferred, however, read requests that do not see results within a desired threshold will have the same content requested from the remote datacenter to ensure data is always available.

## Metadata resilience

SharePoint metadata is also critical to accessing user content as it stores the location of and access keys to the content stored in Azure Storage. These databases are stored in Azure SQL, which has an extensive [business continuity plan](https://docs.microsoft.com/azure/sql-database/sql-database-business-continuity).

SharePoint uses the replication model provided by Azure SQL and has built a proprietary automation technology to determine a failover is required and to initiate the operation if necessary. As such, it falls into the 'Manual database failover' category from an Azure SQL perspective. The latest metrics for Azure SQL database recoverability are available [here](https://docs.microsoft.com/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview#recover-a-database-to-the-existing-server).

SharePoint uses Azure SQL's backup system to enable Point in Time Restores (PITR) for up to 14 days. PITR is covered more in a [later section.](#deletion-backup-and-point-in-time-restore)

## Automated failover

SharePoint uses a custom-built automated failover to minimize the impact on customer experience when a location-specific event occurs. Monitoring-driven automation detecting a single or multi-component failure beyond certain thresholds will result in automated redirection of all users' activity out of the problematic environment and over to a warm secondary. A failover results in metadata and compute storage being served entirely out of the new datacenter. As blob storage runs entirely active/active at all times, no change is required for a failover. Rather, the compute tier will prefer the nearest blob container but can and will use both local and remote blob storage locations at any time to ensure availability.

SharePoint uses the Azure Front Door service to provide routing internal to the Microsoft network. This allows failover redirection to happen independent of DNS and reduce the effect of local-machine caching. Most failover operations are transparent to end users. In the event of a failover, customers will not need to make any changes in order to maintain access to the service.

## Versioning and Files Restore

For newly created document libraries, SharePoint defaults to 500 versions on every file but can be configured to retain additional versions if desired. The UI will not allow a value less than 100 versions to be set, but it is possible to set the system to store fewer versions using public APIs. For reliability, any value less than 100 is not recommended as it can result in user activity causing inadvertent data loss.

Files Restore is the ability to go 'back in time' on any Document Library in SharePoint to any second of time in the last 30 days. This can be used to recover from Ransomware, mass delete, corruption, or any other event. This feature uses file versions so reducing default versions can reduce the effectiveness of this restore.

The Files Restore feature is documented for both [OneDrive](https://support.office.com/article/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15) and [SharePoint](https://support.office.com/article/Restore-a-document-library-317791c3-8bd0-4dfd-8254-3ca90883d39a).

## Deletion, backup, and Point in Time Restore

User content deleted from SharePoint goes through the following deletion flow.

Deleted items are retained in recycle bins for a certain period of time. For SharePoint, the retention time is 93 days. It begins when you delete the item from its original location. When you delete the item from the site recycle bin, it goes into the [site collection recycle bin](https://support.office.com/article/restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b). It stays there for the remainder of the 93 days, and then is permanently deleted. More information about how to use the recycle bin is available at these links:

- [Restore items in the Recycle Bin](https://support.office.com/article/Restore-items-in-the-Recycle-Bin-of-a-SharePoint-site-6df466b6-55f2-4898-8d6e-c0dff851a0be)
- [Restore deleted items from the Site Collection Recycle Bin](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b).

This is the default deletion flow and does not take into account retention policies or labels. For more information, see [Learn about retention for SharePoint and OneDrive](https://docs.microsoft.com/microsoft-365/compliance/retention-policies-sharepoint).

After the 93-day recycle pipeline is complete, deletion takes place independently for Metadata and for Blob Storage. Metadata will be removed immediately from the database, which makes the content unreadable unless the metadata is restored from backup. SharePoint maintains 14 days-worth of backups of metadata. These backups are taken locally in near real time and then pushed to storage in redundant Azure Storage containers on, [according to documentation](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups) at the time of this publication, a 5-10-minute schedule.

When deleting Blob Storage content, SharePoint utilizes the soft delete feature for Azure Blob Storage to protect against accidental or malicious deletion. Using this feature, we have a total of 14 days in which to restore content before it is permanently deleted.

>[!Note]
>While Microsoft applications will send content to the recycle bin for the standard process, SharePoint does provide APIs that allow for skipping the recycle bin and forcing an immediate delete. Review your applications to ensure this is only done when necessary for compliance reasons.

## Integrity Checks

SharePoint uses various methods to ensure the integrity of blobs and metadata at all stages of the data lifecycle:

- **File hash stored in metadata**: Hash of the entire file is stored with file metadata to ensure document level data integrity is maintained during all operations
- **Blob hash stored in metadata**: Each blob-item stores a hash of the encrypted content (protects against corruption in underlying Azure storage)
- **Data integrity job**: Every 14 days, each site is scanned for integrity by listing items in the database and matching those up with listed blobs in Azure storage. The job reports any blob-references missing storage-blobs and can retrieve those blobs through the [Azure storage soft-delete](https://docs.microsoft.com/azure/storage/blobs/soft-delete-blob-overview) feature if needed.
