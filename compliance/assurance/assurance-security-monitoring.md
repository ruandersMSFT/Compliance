---
title: "Security monitoring overview"
description: "Learn about security monitoring in Microsoft 365"
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

# Security monitoring overview

## What is Microsoft's strategy for monitoring security?

Microsoft 365 engages in continuous security monitoring of its systems to detect and respond to threats to Microsoft 365 Services. Our key principles for security monitoring and alerting are:

- Robustness: signals and logic to detect a variety of attack behaviors
- Accuracy: meaningful alerts to avoid distractions from noise
- Speed: ability to catch attackers quickly enough to stop them

Automation, scale, and cloud-based solutions are key pillars of our monitoring and response strategy. For us to effectively catch and stop attacks at the scale of some of the Microsoft 365 core services, our monitoring systems need to automatically raise highly accurate alerts in near real time. Likewise, when an issue is detected, we need the ability to mitigate the risk at scale, we cannot rely on our team to manually fix issues machine-by-machine. To mitigate risks at scale, we use cloud-based tools to automatically apply countermeasures and provide engineers with tools to apply approved mitigations quickly across the environment.

## How does Microsoft 365 perform security monitoring?

Microsoft 365 uses centralized logging to collect and analyze log events for activities that might indicate a security incident. Centralized logging tools aggregate logs from all system components, including event logs, application logs, access control logs, and network-based intrusion detection systems. In addition to server logging and application level data, core infrastructure in our service is equipped with customized security agents that generate detailed telemetry and provide host-based intrusion detection. We use this telemetry for monitoring and forensics.

The logging and telemetry data we collect enables 24/7 security alerting. Our alerting system analyzes log data as it gets uploaded, producing alerts in near real time. This includes rules-based alerts and more sophisticated alerting based on machine learning models. Our monitoring logic goes beyond generic attack scenarios and incorporates deep awareness of service architecture and operations. We use security monitoring data to continuously improve our models to detect new kinds of attacks and improve the accuracy of our security monitoring.

## How does Microsoft 365 respond to security monitoring alerts?

When we need to take an action in response to an alert or to further investigate forensic evidence throughout the service, our cloud-based tools allow us to respond rapidly throughout the environment. These tools include fully automated, intelligent agents that respond to detected threats with security countermeasures. In many cases, these agents deploy automatic countermeasures to mitigate security detections at scale without human intervention. When this is not possible, the security monitoring system automatically alerts the appropriate on-call engineers, who are equipped with a set of tools that enable them to act in real time to mitigate detected threats at scale. Potential incidents escalated to the Microsoft 365 Security Response team are resolved using the security incident response process.

## How does Microsoft 365 monitor system availability?

Microsoft 365 actively monitors its systems for indicators of resource over-utilization and abnormal use. Resource monitoring is complemented by service redundancies to help avoid unexpected downtime and provide customers with reliable access to products and services. Service health issues are communicated promptly to customers through the Service Health Dashboard (SHD).

## Related external regulations & certifications

Microsoft's online services are regularly audited for compliance with external regulations and certifications. Refer to the following table for validation of controls related to security monitoring.

| **External audits** | **Section** | **Latest report date** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: Account management <br> AC-17: Remote access <br> AU-7: Audit reduction and report generation <br> SI-4: Information system monitoring <br> SI-7: Software, firmware, and information integrity <br> | September 24, 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Availability monitoring and capacity planning | February 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Availability monitoring and capacity planning <br> A.16.1: Management of information security incidents and improvements | February 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19: Change monitoring <br> CA-26: Security incident reporting <br> CA-29: On-call engineers <br> CA-48: Datacenter logging | September 30, 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19: Change monitoring <br> CA-26: Security incident reporting <br> CA-29: On-call engineers <br> CA-30: Availability monitoring <br> CA-48: Datacenter logging | September 30, 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-08: Reporting incidents <br> CUEC-10: Service contracts | September 30, 2019 |

## Resources

- [Behind the Scenes: Securing the Infrastructure Powering the Microsoft 365 Service](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
