---
title: WordPress on Pantheon Quick Start Guide
subtitle: WordPress Security
description: Keep your WordPress on Pantheon site secure.
categories: [wordpress]
tags: [wordpress, webops]
contributors: [whitneymeredith]
reviewed: "2022-05-18"
layout: guide
showtoc: true
permalink: docs/guides/wordpress-pantheon/wp-security
anchorid: wordpress-pantheon/wp-security
---

Pantheon automatically provides the following security measures:

- Automated HTTPS
- Secure Dev environment
- DDOS and intrusion protection
- Automated backups
- [Dashboard Security](/guides/secure-development/security-tool) to lock your environments

## Additional Security

Pantheon provides additional security through the following features:

- [Pantheon Global CDN](/guides/global-cdn)

- [Secure Runtime Access](/guides/secure-development/secure-runtime-access)

- [Lockr](/guides/lockr)

- [Secure Integration](/guides/secure-development/secure-integration)

- [Two factor authentication](/guides/secure-development/two-factor-authentication)

- [Secure Connections to Pantheon Services via TLS or SSH Tunnels](/guides/secure-development/ssh-tunnels)

## Avoid WordPress Login Attacks

The `wp-login.php` is the primary WordPress login. The `wp-login.php` path is subject to abuse by bots and other spammers. Review these [recommended actions](/wordpress-best-practices#avoid-wordpress-login-attacks) to protect yourself against login abuse.
