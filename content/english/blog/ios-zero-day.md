---
title: "CISCO IOS Zero Day"
meta_title: ""
description: ""
date: 2023-10-18T05:00:00Z
image: "/images/blog/ios-zero-day.webp"
categories: []
author: "Blog"
tags: []
draft: false
---

On October 17, 2023, Cisco disclosed a critical zero-day vulnerability in its IOS XE software that is being actively exploited by attackers. The vulnerability, tracked as CVE-2023-20198, allows an unauthenticated attacker to gain root access to affected devices.

Cisco has reported that over 10,000 Cisco devices have already been hacked in this wave of attacks. Affected devices include routers, switches, and firewalls that run IOS XE software.

The attackers are exploiting the vulnerability to install a backdoor on affected devices. This backdoor gives the attackers full control over the devices, allowing them to execute arbitrary code, steal data, and disrupt operations.

Cisco has released a patch for the vulnerability, but it is important to note that the patch is not yet available for all affected devices. In the meantime, Cisco recommends that customers implement the following mitigations:

- Disable the web UI on affected devices if it is not needed.
- Block access to the web UI from untrusted networks.
- Implement strong passwords and multi-factor authentication for all users.
- Regularly monitor your network for suspicious activity.

If you are concerned that your Cisco device may have been compromised, you should contact Cisco support for assistance.

### What can you do to protect your business?

In addition to the mitigations recommended by Cisco, there are a number of other things that businesses can do to protect themselves from this zero-day attack, including:

- **Educate your employees about cyber security**: Your employees should be aware of the signs of a cyber attack and know what to do if they suspect that your network is under attack.
- **Keep your software up to date**: Software vendors regularly release security updates to fix vulnerabilities. It is important to install these updates as soon as they are available.
- **Use a web application firewall (WAF)**: A WAF can help to filter out malicious traffic and protect your website from cyber attacks.
- **Use a content delivery network (CDN)**: A CDN can help to distribute your website’s traffic across multiple servers, making it more difficult for attackers to overwhelm your website.

Links:

[Over 10,000 Cisco devices hacked in IOS XE zero-day attacks (bleepingcomputer.com)](https://www.bleepingcomputer.com/news/security/over-10-000-cisco-devices-hacked-in-ios-xe-zero-day-attacks/)

[Cisco Releases Security Advisory for IOS XE Software Web UI | CISA](https://www.cisa.gov/news-events/alerts/2023/10/16/cisco-releases-security-advisory-ios-xe-software-web-ui)

(We take no responsibility for the content of external links.)