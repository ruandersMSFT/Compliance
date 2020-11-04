---
title: "Encryption and key management overview"
description: "Learn about encryption and key management in Microsoft 365"
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
---

# Encryption and key management overview

## What role does encryption play in protecting customer content?

Most Microsoft business cloud services are multitenant, meaning that customer content may be stored on the same physical hardware as that of other customers. To protect the confidentiality of customer content, Microsoft 365 encrypts all data at rest and in transit with some of the strongest and most secure encryption protocols available.

Encryption is not a substitute for strong access controls. Microsoft 365's access control policy of Zero Standing Access (ZSA) protects customer content from unauthorized access by Microsoft employees. Encryption complements access control by protecting the confidentiality of customer content wherever it is stored and by preventing content from being read while in transit between Microsoft 365 systems or between Microsoft 365 and the customer.

## How does Microsoft 365 encrypt data-at-rest?

All customer content in Microsoft 365 is protected by one or more forms of encryption. Microsoft servers use BitLocker to encrypt the disk drives containing customer content at the volume-level. The encryption provided by BitLocker protects customer content in case of lapses in other processes or controls (for example, access control or recycling of hardware) that could lead to unauthorized physical access to disks containing customer content.

Exchange Online, Microsoft Teams, SharePoint Online, and OneDrive for Business also use Service Encryption at the application layer to encrypt customer content. Service Encryption provides rights protection and management features on top of strong encryption protection. It also allows for separation between Windows operating systems and the customer data stored or processed by those operating systems.

## How does Microsoft 365 encrypt data-in-transit?

Microsoft 365 products and services use strong transport protocols, such as TLS, to prevent unauthorized parties from eavesdropping on customer data while it moves over a network. Examples of data in transit include mail messages that are in the process of being delivered, conversations taking place in an online meeting, or files being replicated between datacenters.

In Microsoft 365, data is considered 'in transit' whenever a user's device is communicating with a Microsoft server or a Microsoft server is communicating with another server. Exchange Online, SharePoint Online, Microsoft Teams, and Office Online all use TLS to ensure data remains confidential while in transit.

## How does Microsoft 365 manage the keys used for encryption?

Strong encryption is only as secure as the keys used to encrypt data. Microsoft uses its own security certificates to encrypt TLS connections for data-in-transit. For data-at-rest, BitLocker-protected volumes are encrypted with a full volume encryption key, which is encrypted with a volume master key, which in turn is bound to the Trusted Platform Module (TPM) in the server. BitLocker uses FIPS-compliant algorithms to ensure that encryption keys are never stored or sent over the wire in the clear.

Service Encryption provides an additional layer of encryption for customer data-at-rest in Exchange Online, Microsoft Teams, SharePoint Online, and OneDrive for Business. Service Encryption gives customers two options for encryption key management: Microsoft-managed keys or Customer Key. When using Microsoft-managed keys, Microsoft 365 services automatically generate and securely store the root keys used for Service Encryption.

Customers with requirements to control their own root encryption keys can leverage Service Encryption with Customer Key. Using Customer Key, customers can generate their own cryptographic keys using either an on-premises Hardware Service Module (HSM) or Azure Key Vault (AKV). Customer root keys are stored in AKV, where they can be used as the root of one of the keychains that encrypts customer mailbox data or files. Customer root keys can only be accessed indirectly by Microsoft 365 service code for data encryption and cannot be accessed directly by Microsoft employees.

## Related external regulations & certifications

Microsoft's online services are regularly audited for compliance with external regulations and certifications. Refer to the following table for validation of controls related to encryption and key management.

| **External audits** | **Section** | **Latest report date** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: Transmission confidentiality and integrity <br> SC-13: Use of cryptography <br> SC-28: Protection of information at rest <br>  | September 24, 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Cryptographic controls <br> A.18.1.5: Cryptographic controls | February 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Cryptographic controls <br> A.18.1.5: Cryptographic controls | February 22, 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Encryption of PII transmitted over public data transmission networks | February 22, 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-44: Data-in-transit encryption <br> CA-54: Data-at-rest encryption <br> CA-62: Customer key mailbox encryption <br> CA-63: Customer key data deletion <br> CA-64: Customer key | September 30, 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-16: Customer encryption keys <br> CUEC-17: Customer key vault <br>  CUEC-18: Customer key rotation| September 30, 2019 |
