---
title: "Architecture overview"
description: "Learn about architecture in Microsoft 365"
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
---

# Architecture overview

## What is Microsoft 365?

Microsoft 365 is the cloud-powered, subscription-based version of Office, Windows 10, Enterprise Mobility + Security, and Compliance. Microsoft 365 customers get clients such as Outlook and Windows, and they also benefit from services that Microsoft hosts on their behalf, such as Exchange Online, Microsoft Teams, and SharePoint Online. All components of the service are regularly updated as part of the subscription model, so that our customers have an 'evergreen' product. Microsoft manages the service infrastructure on behalf of customers, meaning that Microsoft is responsible for securing the infrastructure that stores customer data.

In terms of scale, we currently use close to a million machines to power Microsoft 365 services. The infrastructure powering these services varies widely across service-specific hardware and virtualized environments in Azure, Windows and Linux, and multi-tenant and dedicated platforms. Microsoft 365 is a global business, and our infrastructure is distributed in datacenters around the world, enabling our customers to meet data residency and sovereignty requirements.

In short, the service is complex, runs at incredible scale, and requires thousands of Microsoft engineers to build and maintain. It is our top priority for us to keep all this infrastructure secure.

## How does Microsoft 365 ensure isolation between customer tenants?

Microsoft's cloud services are built on the assumption that all tenants are potentially hostile to all other tenants. To properly isolate tenants from one another, Microsoft implements a variety of isolation technologies and controls. These controls are designed to safeguard against information leakage or unauthorized access to customer data across tenants and to prevent the actions of one tenant from adversely affecting the service for another tenant.

Customer content is logically isolated within Microsoft 365 tenants using Azure Active Directory (Azure AD). User authentication in Microsoft 365 verifies not only the user identity, but also the tenant identity the user account is part of, preventing users from accessing data outside their tenant environment. To supplement the logical isolation of Azure AD, customer content is always encrypted at rest and in transit. Individual services may also provide additional layers of tenant isolation, such as SharePoint Online isolation of tenant data in separate, encrypted databases.

## How does Microsoft 365 engineer resilient services that avoid single points of failure?

Microsoft designs and builds cloud services to maximize reliability and minimize the negative effects on customers in the face of faults and challenges to normal operations. This strategy begins with the design of the network connecting our geographically distributed datacenters. Microsoft's network architecture includes direct interconnections and multiple network paths. Microsoft 365 services leverage this redundancy to automatically route traffic around failures to improve service quality.

At the service level, Microsoft 365's resilience strategy prioritizes software resiliency. Wherever possible, our services are deployed in active/active configurations with automated service health monitoring, allowing the service to detect and recover from many common faults and failures without human intervention. In addition to active/active configurations, Microsoft 365 services increase fault-tolerance by ensuring the service is deployed in separate fault zones, preventing a fault in one zone from affecting the availability of other zones.

Data resiliency complements service resiliency by protecting the integrity and availability of data in Microsoft 365 services. Our services use local storage redundancy and geo-redundancy to replicate copies of customer data into different fault zones. If data is corrupted or lost in one fault zone, it can be accessed in another fault zone without loss of availability. Automated integrity checking automatically restores data impacted by many kinds of physical or logical corruption. Microsoft 365 also provides customers with tools to restore data accidentally deleted or modified by the customer in Exchange Online and SharePoint Online.

## How does Microsoft 365 track dependencies and prevent unauthorized external system connections?

Microsoft 365 service teams identify critical system components and their dependencies as part of Business Continuity Management. In addition, Microsoft 365 documents and tracks all external system connections to ensure only authorized connections are allowed in network firewall configurations. Microsoft 365 systems, dependencies, and external connections are documented in Microsoft 365's information security architecture. Both the information security architecture and corresponding data flow diagrams are reviewed and updated annually at a minimum, as well as whenever significant changes are made to the system.

Microsoft 365 architecture is validated regularly and automatically using cloud-based tools to verify alignment with our security principles and to continuously test isolation and resiliency features. Architectural validation works to automatically identify instances where the current state of the service has drifted from the desired state, flagging any deviations for review and mitigation. The goal of architecture validation is to ensure the security capabilities of our service infrastructure continue to function as expected.

## Related external regulations & certifications

Microsoft's online services are regularly audited for compliance with external regulations and certifications. Refer to the following table for validation of controls related to the architecture of Microsoft 365.

| **External audits** | **Section** | **Latest report date** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: Information flow enforcement <br> CP-9: Information system backup <br> PL-8: Information security architecture <br> SC-7: Boundary protection <br> SC-22: Architecture and provisioning | September 24, 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organization of information security <br> A.13.1: Network security management <br> A.17.2: Redundancies | February 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organization of information security <br> A.13.1: Network security management | February 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-37: Tenant isolation <br> CA-49: Backup policies <br> CA-51: Data replication | September 30, 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-05: Data flow diagrams <br> CA-37: Tenant isolation <br> CA-49: Backup policies <br> CA-51: Data replication | September 30, 2019 |