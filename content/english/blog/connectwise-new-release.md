---
title: "Connectwise Screenconnect 23-9-8 Security Fix"
meta_title: ""
description: "this is meta description"
date: 2024-02-20T05:00:00Z
image: "/images/blog/connectwise.webp"
categories: []
author: "Blog"
tags: []
draft: false
---

Connectwise have released a fix to a CVSS 10, critical, remotely exploitable vulnerability which gives a threat actor full control over your ScreenConnect instance.

The noted vulnerabilities are:

CWE-288 Authentication bypass using an alternate path or channel
CWE-22 Improper limitation of a pathname to a restricted directory (“path traversal”)

Although there are no reports so far, ScreenConnect (and remote control products of this type in general) are such a big target to attackers, we would be amazed if this was not already being exploited.

This is a developing story as these often are, don’t delay, get patching.

Connectwise link with patching instructions [connectwise.com/company/trust/security-bulletins/connectwise-screenconnect-23.9.8](https://www.connectwise.com/company/trust/security-bulletins/connectwise-screenconnect-23.9.8)

Update 23/02/24 –

Huntress have confirmed the anecdotal reports of further exploitation. As expected, multiple methods of persistence have been deployed to the endpoints after initial exploitation of the ScreenConnect tenant. This has been big, just how big we are yet to see.

[SlashAndGrab: ScreenConnect Post-Exploitation in the Wild (CVE-2024-1709 & CVE-2024-1708) (huntress.com)](https://www.huntress.com/blog/slashandgrab-screen-connect-post-exploitation-in-the-wild-cve-2024-1709-cve-2024-1708)

Update 21/02/24 –

CWE-288 Authentication bypass is worryingly trivial. The setup wizard was available on already installed instances, meaning that the administrator password could be reset. Connectwise have so far released some IP addresses as indicators of compromise, however these are not much use on their own, and assumes that only a single/limited attacker knew about this bug, which is unlikely.

Huntress have some further information on where to look for possible compromise and general excellent content on this as always:

[A Catastrophe For Control: Understanding the ScreenConnect Authentication Bypass | Huntress](https://www.huntress.com/blog/a-catastrophe-for-control-understanding-the-screenconnect-authentication-bypass)

[BlogDetection Guidance for ConnectWise CWE-288 (huntress.com)](https://www.huntress.com/blog/detection-guidance-for-connectwise-cwe-288-2)