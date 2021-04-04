---
title: "Domain 3: Security Architecture and Engineering"
tags: [domain_3]
##keywords: release notes, announcements, what's new, new features
last_updated: Aug 30, 2020
summary: "Notes for Domain 3"
sidebar: mydoc_sidebar
permalink: 3_notes.html
folder: mydoc
---


# MALWARE

**_catch-all name for any malicious sw_**

**1. VIRUSES** --> require some sort of human interaction, often spread via portable devices (USB sticks, etc.)

|.|.|
|-|-|
|**_macro (document) viruses_**|embedded in other docs (Word/Excel/Outlook)|
|**_boot sector viruses_**|infect PC boot sector/MBR, run at boot|
|**_stealth viruses_**|try to hide themselves|
|**_polymorphic viruses_**|change their signature to avoid id from AV sw|
|**_multipart viruses_**| spread across multiple vectors|

**2. WORMS** --> self-propagated, need no human interaction; do damage && replicate themselves via network

**3. TROJANS** --> malicious code embedded in a normal program

**4. ROOTKITS** --> replaces some of the OS/kernel w/ malicious payload: user rootkits & kernel rootkits

**5. LOGIC BOMBS** --> executed at a certain time/event, dormant until then

**6. PACKERS** --> compress .exe files, can be used to hide malware in an exec.

**7. ANTIVIR SOFTWARE** --> tries to protect against malware
-- signature based --> looks for signatures, needs constant updates
-- heuristic (behavioral) based --> looks for anomalies.


TOCTTOU attacks, race condition exploits, and communication disconnects are known as **state attacks** because they attack timing, data flow control, and transition between one system state to another


**CERTIFICATION** --> technical evaluation to assess its concordance w/ sec standards

**ACCREDITATION** --> process of formal acceptance of a certified config by a designated authority

{% include links.html %}
