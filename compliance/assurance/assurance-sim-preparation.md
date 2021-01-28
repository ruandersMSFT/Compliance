---
title: "Microsoft 365 security incident management: Preparation"
description: "This article, provides an overview of the security incident management preparation process in Microsoft 365."
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

# Microsoft 365 security incident management: Preparation

## Training and background checks

Each employee working on Microsoft 365 is provided with training regarding security incidents and response procedures that are appropriate to their role. Every Microsoft 365 employee receives training upon joining, and annual refresher training every year thereafter. The training is designed to provide the employee with a basic understanding of Microsoft's approach to security so that upon completion of training, all employees understand:

- The definition of a security incident
- The responsibility of all employees to report security incidents
- How to escalate a potential security incident to Microsoft 365 Security Response team
- How the Microsoft 365 Security Incident Response team responds to security incidents
- Special concerns regarding privacy, particularly customer privacy
- Where to find additional information about security and privacy, and escalation contacts
- Any other relevant security areas (as needed)

The appropriate employees receive refresher training on security annually. The annual refresher training focuses on:

- Any changes made to the standard operating procedures in the preceding year
- The responsibility of everyone to report security incidents, and how to do so
- Where to find additional information about security and privacy, and escalation contacts
- Any other security focus areas that may be relevant each year

Each employee working on Microsoft 365 also goes through an appropriate and thorough background check that includes the candidate's education, employment, criminal history, and other specific information per United States regulations like Health Insurance Portability and Accountability Act (HIPAA), International Traffic in Arms Regulations (ITAR), Federal Risk and Authorization Management Program (FedRAMP), and others.

The background checks are mandatory for all employees working within Microsoft 365 engineering. Some Microsoft 365 environments and operator roles may also require full fingerprinting, citizenship requirements, government clearance requirements, and other more stringent controls. In addition, some service teams and roles may go through specialized security training as needed. Lastly, the security team members themselves get specialized training and conference participation that relates directly to security. This training varies by need of the team and employee, but includes things like industry conferences, internal Microsoft Security conferences, and external training courses through well-known security training vendors in the industry. We also have dedicated security training articles published throughout the year for the security community across Microsoft and specialized to Microsoft 365 regularly.

## Penetration testing & assessment

Microsoft works with various industry bodies and security experts to understand new threats and evolving trends. Microsoft continuously assesses its own systems for vulnerabilities, and contracts with various independent, external experts who do the same.

The tests carried out for service hardening within Microsoft 365 can be grouped into four general categories:

1. **Automated security testing:** Internal and external personnel regularly scan the Microsoft 365 environment based on Microsoft SDL practices, Open Web Application Security Project (OWASP) Top 10 risks, and emerging threats reported by different industry bodies.
2. **Vulnerability assessments:** Formal engagements with independent, third-party testers regularly validate whether key logical controls are operating effectively to fulfill the service obligations of various regulatory bodies. The assessments are carried out by Council of Registered Ethical Security Testers (CREST)-certified personnel and are based on OWASP Top 10 risks and other service-applicable threats. All threats found are tracked to closure.
3. **Continuous system vulnerability testing:** Microsoft carries out regular testing in which teams attempt to breach the system using emerging threats, blended threats, and/or advanced persistent threats, while other teams attempt to block such attempts to breach.
4. **Microsoft Online Services Bug Bounty Program**: This program operates a policy of allowing limited, customer-originated, vulnerability assessments on Microsoft 365. For more information, see [Microsoft Online Services Bug Bounty Terms](https://www.microsoft.com/msrc/bounty-terms).

The Microsoft 365 engineering team periodically publishes various compliance documents. Several of those documents are available under a non-disclosure agreement from the [Microsoft Cloud Service Trust Portal](https://aka.ms/STP) or from the Service Assurance area of the [Microsoft 365 compliance center](https://compliance.office.com)

>[!NOTE]
>See Get started with the Service Trust Portal for Office 365 for business, Azure, and Dynamics CRM Online subscriptions for details on how to access the Service Trust Portal. A Microsoft 365 subscription is required to access the Microsoft 365 compliance center.

## Attack Simulation

Microsoft engages in ongoing attack simulation exercises and live-site penetration testing of our security and response plans with the intent to improve detection and response capability. Microsoft regularly simulates real-world breaches, conducts continuous security monitoring, and practices security incident response to validate and improve the security of both Microsoft 365 and Azure.

Microsoft executes an assume breach security strategy using two core teams:

### Red teams

The Microsoft 365 Security Red Team is a group of full-time staff within Microsoft that focuses on breaching Microsoft's infrastructure, platform, and Microsoft's own tenants and applications. They are the dedicated adversary (a group of ethical hackers) performing targeted and persistent attacks against online services (but not customer applications or data). They provide continuous 'full spectrum' validation (for example, technical controls, paper policy, human response, etc.) of service incident response capabilities.

### Blue teams

The Microsoft 365 Security Blue Team is composed of a dedicated set of security responders, and members from across the security incident response, engineering, and operations teams. They are independent and operate separately from the Red Team. The Blue Team follows established security processes and uses the latest tools and technologies to detect and respond to attacks and penetration attempts. Just like real-world attacks, the Blue Team does not know when or how the Red Team's attacks will occur or what methods may be used. Their job, whether it is a Red Team attack or an actual assault, is to detect and respond to all security incidents. For this reason, the Blue Team is continuously on-call and must react to Red Team breaches the same way they would for any other adversary.

Microsoft staffs separate full-time red teams and blue teams across Microsoft in various divisions that conduct operations both across services and within them. Referred to as *Red Teaming*, the approach is to test across Microsoft services' systems and operations using the same tactics, techniques, and procedures as real adversaries, against the live production infrastructure, without the foreknowledge of the infrastructure and platform engineering or operations teams. This tests security detection and response capabilities, and helps identify production vulnerabilities, configuration errors, invalid assumptions, or other security issues in a controlled manner. Every Red Team breach is followed by full disclosure between the Red Team and Blue Team, including service teams, to identify gaps, address findings and significantly improve breach response.

>[!NOTE]
>No customer data is targeted during Red Teaming or live site penetration exercises. The tests are against Microsoft 365 and Azure infrastructure and platforms, as well as Microsoft's own tenants, applications, and data. Customer tenants, applications and data hosted in Microsoft 365 or Azure are never targeted per the agreed to rules of engagement.

### Joint exercises

At times, the Microsoft 365 Security Blue and Red teams will conduct joint operations where the relationship during the operation is more partner than adversarial with a select set of employees from each team. These exercises are well coordinated between the teams to drive a more targeted set of outcomes through real-time collaboration between ethical hackers and responders. These 'purple team' exercises are highly tailored for each operation to maximize the opportunity, but fundamental to each operation is high-bandwidth information sharing and partnership to achieve the objectives.

## Related articles

- [Microsoft 365 security incident management](assurance-security-incident-management.md)
- [Microsoft 365 security incident management containment, eradication, and recovery](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 security incident management detection and analysis](assurance-sim-detection-analysis.md)
- [Microsoft 365 security incident management post-incident activity](assurance-sim-post-incident-activity.md)
