---
title: "Security development and operations overview"
description: "Learn about security development and operations in Microsoft 365"
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

# Security development and operations overview

## How does Microsoft implement secure development practices?

Microsoft's Security Development Lifecycle (SDL) is a security assurance process focused on developing and operating secure software. The SDL provides detailed, measurable security requirements for developers and engineers at Microsoft to reduce the number and severity of vulnerabilities in our products and services. All Microsoft software development teams must follow SDL requirements, and we continuously update the SDL to reflect the changing threat landscape, industry best practices, and regulatory standards for compliance.

## How does Microsoft's SDL improve application security?

The SDL process at Microsoft can be thought of in terms of five phases of development: requirements, design, implementation, verification, and release. It begins by defining software requirements with security in mind. To do this, we ask security-relevant questions about what the application must accomplish. Does the application need to collect sensitive data? Will the application perform sensitive or important tasks? Does the application need to accept input from untrusted sources?

Once relevant security requirements have been identified, we design our software to incorporate security features that meet these requirements. Our developers implement SDL and design requirements in the code, which we verify through manual code review, automated security tooling, and penetration testing. Finally, before code can be released, new features and material changes undergo final security and privacy review to ensure all requirements are met.

## How does Microsoft test source code for common vulnerabilities?

To support our developers in implementing security requirements during code development and after release, Microsoft provides a suite of secure development tools to automatically check source code for security flaws and vulnerabilities. Microsoft defines and publishes a list of approved tools for our developers to use, such as compilers and development environments, along with the built-in security checks executed automatically within Microsoft build pipelines. Our developers use the latest versions of approved tools to take advantage of new security features.

Before code can be checked into a release branch, the SDL requires manual code review by a separate reviewer. Code reviewers check for coding errors and verify that code changes meet SDL and design requirements, pass functional and security tests, and perform reliably. They also review associated documentation, configs, and dependencies to ensure code changes are documented appropriately and will not cause unintended side-effects. If a reviewer finds problems during code review, they can ask the submitter to resubmit the code with suggested changes and additional testing. Code reviewers may also decide to block check-in entirely for code that does not meet requirements. Once the code has been deemed satisfactory by the reviewer, the reviewer provides approval, which is required before code can proceed to the next deployment phase.

In addition to secure development tools and manual code review, Microsoft enforces SDL requirements using automated security tooling. Many of these tools are built into the commit pipeline and automatically analyze code for security flaws as it is checked in and as new builds are compiled. Examples include static code analysis for common security flaws and credential scanners that analyze code for embedded secrets. Issues uncovered by automated security tools must be fixed before new builds can pass security review and be approved for release.

## How does Microsoft manage open-source software?

Microsoft has adopted a high-level strategy for managing open-source security, which leverages tools and workflows designed to:

- Understand which open-source components are being used in our products and services.
- Track where and how those components are used.
- Determine whether those components have any vulnerabilities.
- Respond properly when vulnerabilities are discovered that affect those components.

Microsoft engineering teams maintain responsibility for the security of all open-source software included in a product or service. To achieve this at scale, Microsoft has built essential capabilities into engineering systems through CG, which automates open-source detection, legal requirement workflows, and alerting for vulnerable components. Automated CG tools scan builds at Microsoft for open-source components and associated security vulnerabilities or legal obligations. Discovered components are registered and submitted to the appropriate teams for business and security reviews. These reviews are designed to evaluate any legal obligations or security vulnerabilities associated with open-source components and resolve them before approving components for deployment.

## Related external regulations & certifications

Microsoft's online services are regularly audited for compliance with external regulations and certifications. Refer to the following table for validation of controls related to security development and operation.

| **External audits** | **Section** | **Latest report date** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3: System Development Life Cycle | September 24, 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Change management controls <br> A.14.2: Security in development and support processes | February 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Change management controls <br> A.14.2: Security in development and support processes | February 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03: Risk management <br> CA-18: Change management <br> CA-19: Change monitoring <br> CA-21: Change testing <br> CA-38: Baseline configurations <br> CA-46: Security review | September 30, 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03: Risk management <br> CA-18: Change management <br> CA-19: Change monitoring <br> CA-21: Change testing <br> CA-38: Baseline configurations <br> CA-46: Security review | September 30, 2019 |

## Resources

- [Microsoft's Security Development Lifecycle](https://www.microsoft.com/securityengineering/sdl)
