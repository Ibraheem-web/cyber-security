---
title: "How Keytrap Almost Brought Down The Internet"
meta_title: ""
description: ""
date: 2024-02-23T05:00:00Z
image: "/images/blog/how-keytrap-down-the-internet.webp"
categories: []
author: "Blog"
tags: []
draft: false
---

The “KeyTrap” vulnerability, discovered by a team of German researchers, represents a significant threat to the stability and functionality of the internet. This vulnerability lies in the design of the Domain Name System Security Extensions (DNSSEC), a suite of Internet Engineering Task Force (IETF) specifications for securing certain kinds of information provided by the Domain Name System (DNS).

DNSSEC was designed to protect the internet from certain attacks, such as DNS cache poisoning. It is a set of extensions to DNS, which provide origin authentication of DNS data, data integrity, and authenticated denial of existence. However, the researchers discovered that an aspect of DNSSEC’s design could be exploited to disable any DNSSEC-capable DNS resolver for up to 16 hours with a single UDP DNS query packet. This would effectively deny anyone else that server’s DNS services, causing a significant disruption to internet services.

The researchers identified three main issues in DNSSEC’s design that contribute to this vulnerability:
1. **Key-tag collisions**: DNSSEC allows for multiple cryptographic keys in a given DNS zone. When validating DNSSEC, DNS resolvers are required to identify a suitable cryptographic key to use for signature verification. However, the key-tag, used to differentiate between the keys, is not necessarily unique, leading to potential collisions. This means that multiple different DNS keys can have an identical key-tag, which can cause confusion and inefficiency during the validation process.
2. **Multiple keys**: The DNSSEC specification mandates that a resolver must try all colliding keys until it finds a key that successfully validates the signature or all keys have been tried. This requirement is meant to ensure availability, even if some keys may result in failed validation. However, this “eager validation” can lead to heavy computational effort for the validating resolver, as the number of validations grows linearly with the number of colliding keys.
3. **Multiple signatures**: Similarly, the DNSSEC specification also mandates that in the case of multiple signatures on the same record, a resolver should try all the signatures it received until it finds a valid signature or until all signatures have been tried. This can also lead to a significant increase in computational effort for the resolver.

The researchers devised four different server-side resource exhaustion attacks exploiting these issues, including “SigJam”, “LockCram”, and “KeySigTrap”. These attacks could cause a significant increase in the number of validations, leading to a denial of service (DoS) attack. In the worst-case scenario, a resolver could be stalled for as long as 16 hours by a single DNS query packet.

Fortunately, the vulnerability was responsibly disclosed, and all major implementations of DNS had already been quietly updated before the issue was made public, which was an impressive feat from all involved. This incident underscores the importance of responsible disclosure and the need for robust security measures in the design of critical internet infrastructure. It also highlights the potential risks associated with complex systems like DNSSEC, and the need for ongoing research and vigilance to identify and mitigate such risks.

In conclusion, while the “KeyTrap” vulnerability could have had a devastating impact on the internet, the responsible actions of the researchers and the swift response of the DNS community helped to avert a potential crisis. This incident serves as a reminder of the importance of cybersecurity in maintaining the stability and functionality of the internet, and the need for ongoing vigilance and collaboration in addressing potential threats.

Original research paper: [Technical_Report_KeyTrap.pdf (athene-center.de)](https://www.athene-center.de/fileadmin/content/PDF/Technical_Report_KeyTrap.pdf)