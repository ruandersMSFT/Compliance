---
title: "Resiliency and continuity"
description: "Learn about resiliency and continuity in Microsoft 365"
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

# Resiliency and continuity overview

## How does Microsoft ensure business continuity in the case of a disaster or other threat to service availability?

Microsoft's Enterprise Business Continuity Management (EBCM) team oversees business continuity management and disaster recovery activities across Microsoft services and cloud offerings. Representatives from Microsoft business units, such as Microsoft 365, coordinate with the EBCM team to develop business continuity plans and validate compliance with business continuity requirements.

At the core of our Business Continuity Management (BCM) methodology is the BCM lifecycle. This three-phase process is designed to be adaptable so it can be implemented by a wide variety of business models across Microsoft. It begins with an **Assessment** phase to identify critical processes and objectives that should be included in the business continuity program. The Assessment phase also requires a Business Impact Analysis (BIA). The **Planning** phase focuses on developing and implementing resilience and recovery strategies, as well as documenting them in official business continuity plans. Finally, **Capability Validation** tests business continuity plans and their implementations to verify effectiveness and identify potential improvements.

Microsoft 365's business continuity strategy leverages hardware, network, and datacenter redundancy. Data replication between datacenters provides high availability and reliability in the case of a catastrophic incident. It also increases resilience to mundane incidents such as isolated hardware failure or data corruption.

## How does Microsoft test business continuity and disaster recovery plans?

Microsoft's Enterprise Business Continuity Management (EBCM) policy stipulates that all Microsoft business continuity and disaster recovery plans must be tested, updated, and reviewed on an annual basis. Microsoft 365 services test their business continuity plans at least annually per EBCM policies. After Action reports are created and reviewed to validate,  test results and inform plan updates in response to any problems discovered during testing.

To validate resilience and recovery strategies against a wide range of potential incidents, the EBCM Program defines multiple categories of test scenarios affecting people, locations, and technology. The level of validation required for each service is based on the service's criticality, with more critical services receiving more rigorous validation. Each Microsoft 365 service team tests their business continuity plan according to EBCM guidelines to measure the plan's effectiveness and the service team's readiness to execute the plan.

Per EBCM guidelines, annual reviews of business continuity plans and capability validation must take place within 12 months of the last review. Capability validation must include review of supporting documentation, such as the BIA, to ensure it remains accurate. Microsoft makes capability validation results for select Microsoft 365 services available to our customers through quarterly reports.

## How does Microsoft 365 ensure system capacity meets demand?

Capacity planning helps service teams allocate the resources necessary to support Microsoft 365 service availability. Regular capacity planning is required as part of Microsoft's EBCM program. Service teams review capacity data during quarterly reviews, as well as during emergency situations that warrant additional capacity review.

The raw data for capacity planning is maintained by each service team and includes metrics like system processing, memory, and hardware capacity. Scheduled reviews use a model of the system's current capacity and test it against projected needs in emergency situations. If the model indicates gaps in capacity, proposed changes to system capacity are submitted to service team leadership for review. Approved changes are incorporated into a new model before implementation by service team engineers.

## How does Microsoft 365 maintain service availability during routine system failures?

Microsoft 365 achieves service resilience through redundant architecture, data replication, and automated integrity checking. Redundant architecture involves deploying multiple instances of a service on geographically and physically separate hardware, providing increased fault-tolerance for Microsoft 365 services. Data replication ensures there are always multiple copies of customer data in different fault-zones, allowing critical customer data to be recovered if corrupted, lost, or even accidentally deleted by the customer. Automated integrity checking increases data availability by automatically restoring data impacted by many kinds of physical or logical corruption.

## Related external regulations & certifications

Microsoft's online services are regularly audited for compliance with external regulations and certifications. Refer to the following table for validation of controls related to resiliency and continuity.

| **External audits** | **Section** | **Latest report date** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: Contingency plan <br> CP-3: Contingency training <br> CP-4: Contingency plan testing <br> CP-6: Alternate storage site <br> CP-7: Alternate processing site <br> CP-9: Information system backup <br> CP-10: Information system recovery and reconstitution | September 24, 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Information security continuity <br> A.17.2: Redundancies | February 22, 2020 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | All controls | March 18, 2019 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: Backup policies <br> CA-50: Business continuity <br> CA-51: Data replication | September 30, 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: Backup policies <br> CA-50: Business continuity <br> CA-51: Data replication | September 30, 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-09: EXO email restoration | September 30, 2019 |

## Resources

- [Microsoft Enterprise Business Continuity Management Program Whitepaper](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Microsoft Cloud EBCM and Disaster Recovery Plan Validation Report: FY20 Q4](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=5437a1d9-5883-468b-aee0-8c8a8e4ef56a&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## Legal disclaimer

- [Enterprise business continuity legal disclaimer](assurance-ebcm-legal-disclaimer.md)