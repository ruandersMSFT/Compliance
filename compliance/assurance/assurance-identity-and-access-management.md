---
title: "Identity and access management overview"
description: "Learn about identity and access management in Microsoft 365"
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

# Identity and access management overview

## How does Microsoft 365 protect production systems from unauthorized or malicious access?

Microsoft 365 is designed to allow Microsoft's engineers to operate the service without accessing customer content. By default, Microsoft 365 engineers have Zero Standing Access (ZSA) to customer content and no privileged access to the production environment. Microsoft 365 uses a Just-In-Time (JIT), Just-Enough-Access (JEA) model to provide service team engineers with temporary privileged access to production environments when such access is required to support Microsoft 365. The JIT access model replaces traditional, persistent administrative access with a process for engineers to request temporary elevation into privileged roles when required.

Engineers assigned to a service team to support production services request eligibility for a service team account through the Identity Management Tool (IDM). The request for eligibility triggers a series of personnel checks to ensure the engineer has passed all cloud screening requirements, completed necessary training, and received appropriate management approval prior to account creation. Only after meeting all eligibility requirements can a service team account be created for the requested environment.

Service team accounts do not grant any standing administrator privileges or access to customer content. When an engineer requires additional access to support their Microsoft 365 service, they request temporary elevated access to the resources they require using an access management tool called Lockbox. Lockbox restricts elevated access to the minimum privileges, resources, and time needed to complete the assigned task. If an authorized reviewer approves the JIT access request, the engineer is granted a temporary account with only the privileges necessary to complete their assigned work. This temporary account requires multi-factor authentication and is automatically deleted after the approved period expires.

## How does Microsoft 365 handle remote access to production systems?

Microsoft 365 system components are housed in datacenters geographically separated from the operations teams. Datacenter personnel do not have logical access to Microsoft 365 systems. As a result, Microsoft 365 service team personnel manage the environment through remote access. Service team personnel who require remote access to support Microsoft 365 are only granted remote access after approval from an authorized manager. All remote access uses FIPS 140-2 compatible TLS for secure remote connections.

Microsoft 365 uses Secure Admin Workstations (SAWs) for service team remote access to help protect Microsoft 365 environments from compromise. These workstations are specifically designed to prevent intentional or unintentional loss of production data, including locking down USB ports and limiting the software available on the SAW to what is required for supporting the environment. SAWs are closely tracked and monitored to detect and prevent malicious or inadvertent compromise of customer data by Microsoft engineers.

## How does Customer Lockbox add additional protection for customer content?

Customers can add an additional level of access control to their content by enabling Customer Lockbox. When a Lockbox elevation request involves access to customer content, Customer Lockbox requires approval from the customer as a final step in the approval workflow. This gives organizations the option to approve or deny these requests and provides direct access control to the customer. If the customer rejects a Customer Lockbox request, access to the requested content is denied. If the customer does not reject or approve the request within a certain period, then the request will expire automatically without Microsoft obtaining access to customer content. If the customer approves the request, then Microsoft's temporary access to customer content will be logged, auditable, and revoked automatically after the time assigned to complete the troubleshooting operation expires.

## Related external regulations & certifications

Microsoft's online services are regularly audited for compliance with external regulations and certifications. Refer to the following table for validation of controls related to identity and access control.

| **External audits** | **Section** | **Latest report date** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://sip.compliance.microsoft.com/compliancemanager) | AC-2: Account management <br> AC-3: Access enforcement <br> AC-5: Separation of duties <br> AC-6: Least privilege <br> AC-17: Remote access | 9/24/2020 |
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Business requirements of access control <br> A.9.2: User access management <br> A.9.3: User responsibilities <br> A.9.4: System and application access control <br> A.15.1: Information security in supplier relationships | 2/22/2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.2: User access management <br> A.9.4: System and application access control <br> A.15.1: Information security in supplier relationships | 2/22/2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-33: Account modification <br> CA-34: User authentication <br> CA-35: Privileged access <br> CA-36: Remote access <br> CA-57: Customer Lockbox Microsoft management approval <br> CA-58: Customer Lockbox service requests <br> CA-59: Customer Lockbox notifications <br> CA-61: JIT review and approval | 9/30/2019 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-32: Shared account policy <br> CA-33: Account modification <br> CA-34: User authentication <br> CA-35: Privileged access <br> CA-36: Remote access <br> CA-53: Third-party monitoring <br> CA-56: Customer Lockbox customer approval <br> CA-57: Customer Lockbox Microsoft management approval <br> CA-58: Customer Lockbox service requests <br> CA-59: Customer Lockbox notifications <br> CA-61: JIT review and approval | 9/30/2019 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-15: Customer Lockbox requests | 9/30/2019 |