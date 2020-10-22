---
title: "Supplier management overview"
description: "Learn about supplier management in Microsoft 365"
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
ms.topic: article
f1_keywords:
- 'ms.o365.cc.SupervisoryReview'
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
---

# Supplier management overview

## How does Microsoft manage risk related to suppliers?

Microsoft partners with third-party companies to help meet our customers' needs. These third-party companies are referred to as suppliers or subprocessors. Supplier security and privacy at Microsoft is governed by our [Supplier Security and Privacy Assurance (SSPA) program](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6), an enterprise-wide set of requirements for all suppliers who partner with Microsoft to deliver our online services. While the SSPA program provides comprehensive governance and management of our supplier base, individual business units, such as Microsoft 365, may maintain additional requirements for their suppliers.

## How does Microsoft's Supplier Security and Privacy Assurance (SSPA) Program protect customer data?

SSPA is a partnership between Microsoft Procurement, Corporate External and Legal Affairs, and Corporate Security to ensure suppliers adhere to Microsoft's privacy and security principles. The scope of SSPA covers all suppliers that process Personal Data or Microsoft Confidential Data. The SSPA program enrollment includes adherence to Microsoft's Data Protection Requirements (DPR). The DPR consist of security and privacy controls that suppliers must implement before beginning contracted work with Microsoft. All enrolled suppliers self-attest to compliance with the DPR annually.

DPR requirements are scoped based on six distinct data processing categories a supplier can be approved for as part of their enrollment in SSPA. These categories are used to identify the risk associated with the services a supplier provides to Microsoft. The supplier's data processing profile determines which DPR controls are considered in-scope to provide appropriate data protection. Suppliers who process data that is considered a higher risk must comply with all DPR requirements and may also need to provide independent verification of compliance. Microsoft purchasing tools validate the SSPA status of all suppliers, including compliance with applicable portions of the DPR, prior to allowing the procurement of that supplier.

## What types of subprocessors provide services for Microsoft?

A 'subprocessor' is a third party that Microsoft engages whose duties include processing Microsoft Personal Data for which Microsoft is a processor. Microsoft's subprocessors fall into three distinct categories. Each must demonstrate compliance with the SSPA before they can process customer data on Microsoft's behalf.

- **Technology** subprocessors provide technologies used to deliver specific Microsoft online services. If a customer deploys one of these services, the subprocessors identified for that service may process, store, or otherwise access customer data or personal data while helping to provide that service.
- **Ancillary** subprocessors provide services that support, operate, and maintain the online services. If a customer deploys one of these services, the subprocessors identified may process, store, or otherwise access limited customer data or personal data while providing their ancillary services.
- **Staff Augmentation** subprocessors take two different forms: In both scenarios, Personal Data resides only in Microsoft facilities, on Microsoft systems, and is subject to Microsoft policies and supervision.

    - The first form of staff augmentation provides staff that supports, operates, and maintains Microsoft online services. While fulfilling their responsibilities, these subprocessors may be exposed to customer data or personal data. For example, a subprocessor may perform remote troubleshooting on a Microsoft server and while doing so may be exposed to snippets of customer data in a server crash dump log.
    - The second form of staff augmentation involves subprocessors who work side by side with Microsoft full-time employees to support, operate, and maintain Microsoft online services. These subprocessors may be exposed to pseudonymized data as part of their work alongside Microsoft full-time employees.

Technology and Ancillary subprocessors are required to implement access controls in compliance with Microsoft's Data Protection Requirements (DPR). These requirements meet or exceed the contractual commitments Microsoft makes to its customers in the Online Service Terms (OST). Suppliers who perform staff augmentation work are subject to the same access controls in place for Microsoft full-time employees.

## How does Microsoft onboard suppliers?

Third party suppliers are required to sign a Microsoft Master Agreement as part of the onboarding process. This agreement governs the relationship between Microsoft and its suppliers and ensures consistent management of supplier relationships. As part of onboarding, suppliers enroll in the SSPA and must complete all applicable requirements before they can be approved for any data processing categories. Microsoft business units are only able to create engagements with suppliers when the data processing activity for the engagement matches data processing categories for which the supplier has been approved.

## How does Microsoft notify customers of changes to suppliers who process their data?

Per the Microsoft Online Service Data Protection Addendum (DPA), Microsoft makes additional commitments regarding notice periods for the addition of any subprocessor. Notice time frames depend on the type of data the subprocessor will process on behalf of Microsoft. As stated in the DPA, Microsoft commits to providing notice to customers at least six months in advance of any new subprocessor who will process Customer Data. For any other Personal Data, Microsoft will provide at least 30 days of notice. Notice is provided by the update of the [Microsoft Online Services Subprocessor List](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List).

## Related external regulations & certifications

Microsoft's online services are regularly audited for compliance with external regulations and certifications. Please refer to the table below for validation of controls related to supplier management.

| **External audits** | **Section** | **Latest report date** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CA-3: System interconnections <br> IA-4: Identifier management <br> PS-6: Access agreements <br> PS-7: Third-party personnel security <br> SA-4: Acquisitions process <br> SA-9: External information system services <br> SA-12: Supply chain protection | 9/24/2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Information security in supplier relationships | 2/22/2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Information security in supplier relationships | 2/22/2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A.8.1: Disclosure of sub-contractied PII processing | 9/30/2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-53: Third-party monitoring | 9/30/2019 |

## Resources

[Supplier Security Privacy and Assurance Program](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
