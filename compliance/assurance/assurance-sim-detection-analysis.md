---
title: "Microsoft 365 security incident management: Detection and analysis"
description: "This article, provides an overview of the security incident management detection and analysis process in Microsoft 365."
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
- MS-Compliance
titleSuffix: Microsoft Service Assurance
---

# Microsoft 365 security incident management: Detection and analysis

To detect malicious activity, Microsoft 365 centrally logs security events and other data and performs various analytical techniques to find anomalous or suspicious activity. Log files are collected from Microsoft 365 servers and infrastructure devices and stored in a central and consolidated database.

Microsoft takes a risk-based approach to detecting malicious activity. We use incident data and threat intelligence to define and prioritize our detections.

Employing a team of highly experienced, proficient, and skilled people is one of the most important pillars to success in the detection and analysis phase. Microsoft 365 employs multiple service teams, and those teams include employees with competencies on all components within the stack, including the network, routers, firewalls, load balancers, operating systems, and applications.

The security detection mechanisms in Microsoft 365 also include notification and alerts that are initiated by different sources. The Microsoft 365 Security Response team is the key orchestrator of the security incident escalation process. This team receives all escalations and is responsible for analyzing and confirming the validity of the security incident.

One of the primary pillars of detection is notification:

- Each service team is responsible to log any action or event inside the service based on the requirements from the Microsoft 365 Security team. All logs created by the different service teams are processed by a Security Information and Event Management (SIEM) solution with predefined security and detection rules. These rules evolve based on the Microsoft 365 Security team’s recommendation, on information learned from previous security incidents, to determine if there is any suspicious or malicious activity.
- If a customer determines that a security incident is underway, they may open a support case with Microsoft, which is assigned to the Microsoft 365 Customer Experience (CxP) Communications team and turned into an escalation to all appropriate teams.

Microsoft 365 service teams also use the intelligence gained in trend analysis through security monitoring and logging to detect abnormalities in Microsoft 365 information systems that might indicate an attack or a security incident. Microsoft 365 servers aggregate output from these logs in the production environment into a centralized logging server. From this centralized logging server, logs are examined to spot trends throughout the production environment. Data aggregated in the centralized server is securely transmitted into a logging service for advanced querying, dashboard building and detecting anomalous and malicious activity. The service also uses machine learning to detect anomalies with log output.

During the escalation phase and depending on the nature of the security incident, the Microsoft 365 Security Response team may engage one or more subject matter experts from various teams at Microsoft:

- Online Services Security and Compliance team
- Microsoft Threat Intelligence Center (MSTIC)
- Microsoft Security Response Center (MSRC)
- Corporate, External, and Legal Affairs (CELA)
- Azure Security
- Microsoft 365 engineering, and others.

Before any escalation to the Microsoft 365 Security Response team occurs, the service team is responsible for determining and setting the severity level of the security incident based on defined criteria such as:

- Privacy
- Impact
- Scope
- Number of affected tenants
- Region
- Service
- Details of the incident
- Specific customer industry or market regulations.

Incident prioritization is determined by using distinct factors, including but not limited to the functional impact of the incident, the informational impact of the incident, and the recoverability from the incident.

After receiving an escalation about a security incident, the Microsoft 365 Security team organizes a virtual team (v-team) comprised of members from Microsoft 365 Security Response team, service teams, and the Microsoft 365 Incident Communication team. The more complex part of activities of this v-team is to confirm the security incident and to eliminate any false positives. The accuracy of information provided by the indicators determined in the preparation phase is critical. By analyzing this information by category of vector attack, the v-team can determine if the security incident is a legitimate concern.

At the beginning of the investigation, the Office Security Incident Response team records all information about the incident according to our case management policies. As the case progresses, we track ongoing actions and follow evidence handling standards for gathering, retaining, and securing this data throughout the incident lifecycle.

Some examples of these actions would include:

- A summary, which is a brief description of the incident and its potential impact
- The incident's severity and priority, which are derived by assessing the potential impact
- A list of all indicators identified which led to detection of the incident
- A list of any related incidents
- A list of all actions taken by the v-team
- Any gathered evidence, which will also be preserved for post-mortem analysis and future forensic investigations
- Recommended next steps and actions

After security incident confirmation, the primary goals of the Microsoft 365 Security Response team and the appropriate service team are to contain the attack, to protect the service(s) under attack, and to avoid a greater global impact. At the same time, the appropriate engineering teams work to determine the root cause and to prepare the first recovery plan.

In the next phase, the Microsoft 365 Security Response team identifies the customer(s) affected by the security incident, if any. The scope of effect can take some time to determine, based on region, datacenter, service, server farm, server, and so forth. The list of affected customers is compiled by the service team and the Microsoft 365 CxP Communications team, who then handle the customer notification process within contractual and compliance obligations.

## Related articles

- [Microsoft 365 security incident management](assurance-security-incident-management.md)
- [Microsoft 365 security incident management preparation](assurance-sim-preparation.md)
- [Microsoft 365 security incident management containment, eradication, and recovery](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 security incident management post-incident activity](assurance-sim-post-incident-activity.md)
