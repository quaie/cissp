---
title: Kerberos
tags: [domain_5]
##keywords: release notes, announcements, what's new, new features
last_updated: Apr 11, 2021
summary: "Kerberos"
sidebar: mydoc_sidebar
permalink: 5_kerberos.html
folder: mydoc
---

creates logical network of devices - REALM - and uses a system of tickets and session keys to auth clients

1. client auth itself to KDC
    - receives _**TGT**_ (ticket-granting ticket) + _**session key**_
    - TGT + session key = credentials for other devices in realm
2. client needs another device in realm
    - client decrypts session key & sends it w/ TGT to TGS (ticket-granting server)
3. TGS returns a ST (service ticket) encrypted w/ a key specific to the wanted device
    - TGS returns also a  _**second session key**_
4. client sends ST + second session key to device

|role|function|
|-|-|
|KDC (key distribution center)|- authenticates the user in realm|
||- returns TGT (ticket-granting ticket) + session key
|TGS (ticket granting server)|- authenticates the user for a service/server (permission to access)|
||- returns ST (service ticket - enc w/ target's key) + session key for target|




{% include links.html %}
