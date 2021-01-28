---
title: "Microsoft 365 security incident management"
description: "This article, provides an overview of the security incident management process in Microsoft 365."
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance0
titleSuffix: Microsoft Service Assurance
---

# Microsoft 365 security incident management

Microsoft works continuously to provide highly secure, enterprise-grade services for Microsoft 365 customers. This document describes how Microsoft handles security incidents in Microsoft 365. A security incident refers to any unlawful access to customer data stored on Microsoft's equipment or in Microsoft's facilities, or unauthorized access to such equipment or facilities that have the potential to result in the loss, disclosure, or alteration of customer data. Microsoft's goals when responding to security incidents are to protect customer data and the Microsoft 365 services.

The Microsoft 365 Security team and the various service teams work jointly and take the same approach to security incidents:

- Preparation
- Detection and Analysis
- Containment
- Eradication
- Recovery
- Post-Incident Activity

## Microsoft approach to security incident management

Microsoft's approach to managing a security incident conforms to [National Institute of Standards and Technology (NIST)](https://www.nist.gov/) Special Publication (SP) 800-61. Microsoft has several dedicated teams that work together to prevent, monitor, detect, and respond to security incidents.

|**Team/Area**|**Description**|
|:------------|:--------------|
| Microsoft Security Response Center | Identifies, monitors, resolves, and responds to security incidents and Microsoft software security vulnerabilities. |
| Cyber Defense Operations Center | The Cyber Defense Operations Center is the physical location that brings together security response teams and experts from across the company to help protect, detect, and respond to threats in real time. |
| Corporate, External, and Legal Affairs | Provides legal and regulatory advice for a suspected security incident. |
| Microsoft 365 Security Response Team | Partners with Microsoft 365 Service teams to build the appropriate security incident management process and to drive any security incident response. |
| Office 365 Trust | Provides guidance on regulatory requirements, compliance, and privacy. |
| Microsoft 365 Datacenter Security Team | Team that focuses across the various services on common security engineering investments to protect, detect, and respond to Microsoft 365 service architecture risks and threats. |
| Service teams | Engineering teams for Microsoft 365 services, such as Exchange, SharePoint, and Microsoft Teams, that are responsible for security-related policies and decisions for each service. |
| Microsoft Threat Intelligence Center (MSTIC) | Provides the current state of art in digital security threats against Microsoft infrastructure and assets, helps partner teams inside Microsoft prioritize mitigation and prevention effort action plans, and increases protection by adopting near real-time incident monitoring/detection. |
| Partner Security teams | Other partner security teams inside Microsoft that provide key services or are responsible for key dependencies in Microsoft 365, such as the Azure Security Response team, Identity Security Response, and Microsoft Corporate Security Response teams. |
| Microsoft 365 Customer Experience Communications | Engineering team responsible for all customer communications about security and service incidents. |

## Response management process

The Microsoft 365 Security team and the service teams work together on and take the same approach to security incidents, which is based on the NIST 800-61 response management phases:

- **Preparation**: Refers to the organizational preparation that is needed to be able to respond, including tools, processes, competencies, and readiness.
- **Detection & analysis**: Refers to the activity to detect a security incident in a production environment and to analyze all events to confirm the authenticity of the security incident.
- **Containment, eradication, recovery**: Refers to the required and appropriate actions taken to contain the security incident based on the analysis done in the previous phase. More analysis may also be necessary in this phase to fully recovery from the security incident.
- **Post-incident activity**: Refers to the post-mortem analysis performed after the recovery of a security incident. The operational actions performed during the process are reviewed to determine if any changes need to be made in the preparation or detection and analysis phases.

## Federated security response model

Microsoft 365 services include core Microsoft online services (Exchange, SharePoint, and Microsoft Teams, etc.) and other Microsoft cloud services, such as Azure Active Directory, the Microsoft Commerce Platform, and the MSTIC. These services are operated by separate teams with their own security operational processes. Other teams at Microsoft are also engaged in various security aspects of Microsoft 365. Because of the multitude of teams working on security operations management across all the various services that make up Microsoft 365, Microsoft has implemented a federated security response model.

This table presents the operational boundaries between the various Microsoft 365 security operations teams and the Microsoft 365 service teams:

|**Activity**|**Microsoft 365 Security Team Operations**|**Microsoft 365 Service Team Operations**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Detection and analysis | - Detection requirements <br> - Security monitoring and analysis <br> - Indicator of compromise (IOC) sweeps <br> - Breach hunt <br> - 24x7 security on-call and incident response lead | - Detection requirements <br> - Monitoring infrastructure deployment <br> - Service analysis and insight <br> - Event and alert triage <br> - 24x7 service engineering on-call  |
| Containment, eradication, recovery | - Incident response lead <br> - Forensics investigation <br> - Security expertise and consulting <br> - Recovery guidance | - Security incident owner <br> - Service insight and expertise <br> - Execute containment, eradication, and recovery |
| Post-incident activity | - Post-incident analysis lead <br> - Data collection and archival <br> - Lessons learned and bug requests <br> - Incident reporting | - Service-side incident analysis <br> - Prioritize follow-up activities <br> - Implementation security investments <br> - Service security readiness |

## Related articles

- [Microsoft 365 security incident management preparation](assurance-sim-preparation.md)
- [Microsoft 365 security incident management containment, eradication, and recovery](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 security incident management detection and analysis](assurance-sim-detection-analysis.md)
- [Microsoft 365 security incident management post-incident activity](assurance-sim-post-incident-activity.md)
