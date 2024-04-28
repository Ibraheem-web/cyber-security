---
title: "Unpacking The WEBP Vulnerability Be Scure Cyber"
meta_title: ""
description: ""
date: 2023-09-27T05:00:00Z
image: "/images/blog/unpacking-the-webp.webp"
categories: []
author: "Blog"
tags: []
draft: false
---

On September 27, 2023, Progress Software published a security advisory on multiple vulnerabilities affecting WS_FTP Server, a secure file transfer solution. Two of these vulnerabilities are critical:

CVE-2023-40044: A .NET deserialization vulnerability in the WS_FTP Server Ad Hoc Transfer module that allows an unauthenticated attacker to execute remote commands directly on the server’s underlying operating system.
CVE-2023-42657: A directory traversal vulnerability in WS_FTP Server versions prior to 8.7.4 and 8.8.2 that allows an attacker to perform file operations on files and folders outside of their authorized WS_FTP folder path.
Multiple security vendors have observed multiple instances of WS_FTP exploitation in the wild since the vulnerabilities were disclosed.

Exploitation of CVE-2023-40044 has been observed in multiple customer environments.

What to do if you are using WS_FTP Server:

Upgrade to WS_FTP Server version 8.7.4 or 8.8.2 **immediately**.
If you are unable to upgrade, you can mitigate the risk of exploitation by:
Disabling the WS_FTP Server Ad Hoc Transfer module.
Restricting access to the WS_FTP Server manager interface.
Implementing a web application firewall (WAF) to block malicious requests.
General recommendations for protecting against file transfer vulnerabilities:

Keep your file transfer software up to date.
Use strong passwords and two-factor authentication for all user accounts.
Implement network segmentation to isolate file transfer servers from other critical systems.
Monitor your network for suspicious activity.


**Conclusion**

The critical vulnerabilities in WS_FTP Server are a serious risk to organizations that use this software. It is important to upgrade to the latest version of WS_FTP Server as soon as possible. If you are unable to upgrade, you should take steps to mitigate the risk of exploitation.

If you would like help with navigating and mitigating issues like this. Contact Be Secure Cyber for a no obligation chat.

Links:

[NVD – CVE-2023-40044 (nist.gov), NVD – CVE-2023-42657 (nist.gov), Observed Exploitation of Critical WS_FTP Vulnerabilities : msp (reddit.com)](https://nvd.nist.gov/vuln/detail/CVE-2023-42657),

[Critical Vulnerabilities in WS_FTP Server | Rapid7 Blog](https://www.rapid7.com/blog/post/2023/09/29/etr-critical-vulnerabilities-in-ws_ftp-server/)

(We take no responsibility for the content of external links.)

How do you ensure that your critical software is patched? Be Secure Cyber can help you ensure that your business stays secure.