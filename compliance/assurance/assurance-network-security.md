---
title: "Network security"
description: "Learn about network security in Microsoft 365"
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

# Network security overview

## How does Microsoft 365 secure the network boundary?

Microsoft 365 employs multiple strategies for securing its network boundary, including automated detection and prevention of network-based attacks, specialized firewall devices, and Exchange Online Protection (EOP) for anti-spam and anti-malware protection. In addition, Microsoft 365 separates its production environment into logically isolated network segments, with only necessary communication permitted between segments. Network traffic is secured using additional network firewalls at boundary points to help detect, prevent, and mitigate network attacks.

## How does Microsoft 365 defend against DDoS attacks?

Microsoft's large internet presence insulates it from the negative effects of many distributed denial-of-service (DDoS) attacks. Distributed instances of each Microsoft 365 service and multiple routes to each service limit the impact of DDoS attacks against the system. This redundancy improves Microsoft 365’s ability to absorb DDoS attacks and increases the amount of time available to detect and mitigate DDoS attacks before they impact service availability.

In addition to Microsoft’s redundant system architecture, Microsoft uses sophisticated detection and mitigation tools to respond to DDoS attacks. Special-purpose firewalls monitor and drop unwanted traffic before it crosses the boundary into the network, reducing stress on systems located inside the network boundary. To further protect our cloud services, Microsoft utilizes a DDoS defense system deployed as part of Microsoft Azure. The Azure DDoS defense system is designed to withstand attacks from the outside as well as from other Azure tenants.

## How does Microsoft 365 protect users against spam and malware being uploaded or sent through online services?

Microsoft 365 builds antimalware protection into services that might be vectors for malicious code, such as Exchange Online and SharePoint Online. Exchange Online Protection (EOP) scans all emails and email attachments for malware as they enter and exit the system, preventing infected messages and attachments from being delivered. Advanced spam filtering is automatically applied to inbound and outbound messages to help prevent customer organizations from receiving and sending spam. This layer of protection guards against attacks that take advantage of unsolicited or unauthorized email, such as phishing attacks. SharePoint Online uses the same virus detection engine to selectively scan uploaded files for malware. If a file is marked as infected, users are prevented from downloading or syncing the file to protect client endpoints.

## Related external regulations & certifications

Microsoft’s online services are regularly audited for compliance with external regulations and certifications. Please refer to the following table for validation of controls related to network security.

<table>
<thead>
<tr class="header">
<th><strong>External audits</strong></th>
<th><strong>Section</strong></th>
<th><strong>Latest report date</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="https://sip.compliance.microsoft.com/compliancemanager"><strong>FedRAMP</strong></a></td>
<td><p><strong>SC-5: Denial of service protection</strong></p>
<p><strong>SC-7: Boundary protection</strong></p>
<p><strong>SI-2: Flaw remediation</strong></p>
<p><strong>SI-3: Malicious code protection</strong></p>
<p><strong>SI-8: Spam protection</strong></p></td>
<td>9/24/2020</td>
</tr>
<tr class="even">
<td><a href="https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&amp;downloadType=Document&amp;downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&amp;tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&amp;docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports"><strong>SOC 1 (Office 365)</strong></a></td>
<td><strong>CA-27: Vulnerability Scanning</strong></td>
<td>9/30/2019</td>
</tr>
<tr class="odd">
<td><a href="https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&amp;downloadType=Document&amp;downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&amp;tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&amp;docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports"><strong>SOC 2 (Office 365)</strong></a></td>
<td><p><strong>CA-27: Vulnerability Scanning</strong></p>
<p><strong>CA-45: Anti-malware</strong></p></td>
<td>9/30/2019</td>
</tr>
<tr class="even">
<td><a href="https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&amp;downloadType=Document&amp;downloadId=22d75122-9d83-4b44-8e25-c273dcbafdc3&amp;tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&amp;docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports"><strong>SOC 2 (Azure)</strong></a></td>
<td><p><strong>IVS-13: Network-based attack response</strong></p>
<p><strong>KOS-01: Network-based attack detection</strong></p></td>
<td>11/4/2019</td>
</tr>
</tbody>
</table>

## Resources
