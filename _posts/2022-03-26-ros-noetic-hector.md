---
layout: single
title: 666 - Hack The Box
excerpt: "To solve Unbalanced, we'll find configuration backups files in EncFS and after cracking the password and figuring out how EncFS works, we get the Squid proxy cache manager password that let us discover internal hosts. Proxying through Squid, we then land on a login page that uses Xpath to query an XML backend database. We perform Xpath injection to retrieve the password of each user, then port forward through the SSH shell to reach a Pi-Hole instance, vulnerable to a command injection vulnerability."
date: 2021-03-26
classes: wide
header:
  teaser: /assets/images/htb-writeup-unbalanced/unbalanced_logo.png
  teaser_home_page: true
  icon: /assets/images/hackthebox.webp
categories:
  - hackthebox
  - infosec
tags:  
  - rsync
  - encfs
  - squid
  - xpath
  - CVE-2020-11108
  - command injection
---

Holis