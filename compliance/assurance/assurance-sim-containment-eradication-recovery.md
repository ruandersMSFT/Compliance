---
title: "Microsoft 365 security incident management: Containment, eradication, and recovery"
description: "This article, provides an overview of the security incident management containment, eradication, and recovery process in Microsoft 365."
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

# Microsoft 365 security incident management: Containment, eradication, and recovery

Based on the analysis performed by the Microsoft 365 Security Response team, the service team, and others, an appropriate containment and recovery plan is developed to minimize the effect of the security incident. The appropriate service teams then apply that plan in production with support from the Microsoft 365 Security Response team.

## Containment

After detecting a security incident, it is important to contain the intrusion before the adversary can access more resources or cause more damage. The primary goal of our security incident response procedures is to limit impact to customers or their data, or to Microsoft systems, services, and applications.

## Eradication

Eradication is the process of eliminating the root cause of the security incident with a high degree of confidence. The goal is two-fold:

- to evict the adversary completely from the environment
- to mitigate the vulnerability (if known) that enabled or could enable the adversary to reenter the environment.

Depending on the nature of the incident, the scope of the security incident, the depth of the penetration and possible repercussions, the Microsoft 365 Security Response team will recommend that service teams adopt eradication techniques. Considering the potential business impact that may be caused by these eradication steps, these decisions will be made by service teams and the Microsoft 365 Security Response team after a detailed analysis and approval from the Executive Incident Manager (if necessary).

## Recovery

As the response team gains a reasonable level of confidence that the adversary has been evicted from the environment and all known vulnerable paths have been eliminated, the individual service teams, will initiate restoration steps to bring the service to a known and good configuration. These restoration steps will be in consultation with the Microsoft 365 Security Response team. This activity includes identifying the last known good state of the service, restoring from backups to this state, inspecting vulnerable attack paths in the restored state, etc. The Microsoft 365 Security Response team, in consultation with the service teams, will determine the best possible recovery plan for the environment.

A key aspect to the recovery is to have enhanced vigilance and controls in place to validate that the recovery plan has been successfully executed, and that no signs of breach exist in the environment.

## Customer notification of security incident

If Microsoft determines that a security incident has occurred, we will notify you with undue delay, and within contractual and compliance requirements we have agreed to. After identifying all affected tenants, the Microsoft 365 Customer Experience (CxP) Communications team works to identify any relevant regulations that might apply to affected tenants. The Microsoft 365 CxP Communications team uses the appropriate communication channel defined in applicable regulations to notify the appropriate tenant contact.

Notification will include detailed information about the incident, such as a description of the incident, the effect on customer data, if any, actions taken by Microsoft, and/or suggested actions for customers to take to resolve the issue and prevent recurrence. Notification will be delivered to the designated administrator(s) of the Microsoft 365 tenant. To ensure notifications are received, you should ensure that your administrators provide and maintain accurate contact information in their tenant profiles. In addition, depending on the nature of the incident, customers can also be notified via the Microsoft 365 Service Health Dashboard[.](http://status.yammer.com/)

## Related articles

- [Microsoft 365 security incident management](assurance-security-incident-management.md)
- [Microsoft 365 security incident management preparation](assurance-sim-preparation.md)
- [Microsoft 365 security incident management detection and analysis](assurance-sim-detection-analysis.md)
- [Microsoft 365 security incident management post-incident activity](assurance-sim-post-incident-activity.md)
