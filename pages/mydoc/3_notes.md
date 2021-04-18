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


# Authentication factors

1. something you **know** --> pin, password
2. something you **have** --> trusted device
3. something you **are** --> biometric
4. **somewhere** you **are** --> geolocation
5. time

**AuthN - authentication** --> prove you are who you say you are - IDENTITY

**AuthZ - authorization** --> grant an authenticated user permissions to do something - ACCESS


**FIRMWARE** --> sw on a ROM chip, containing basic instructions needed to start a device (comp/printer/etc.)

**Functional order of security controls** --> DETERRENCE - DENIAL - DETECTION - DELAY

# security modes for systems processing classified information

|mode|details|
|-|-|
|**dedicated**|clearance + approval + need to know for ALL INFO|
|**system high**|clearance + approval for ALL INFO; need to know for OWN INFO|
|**compartmented**|clearance for ALL INFO|approval + need to know for OWN INFO|
|**multilevel**|clearance + approval + need to know for OWN INFO|


# Models & frameworks

**Enterprise architecture security models**
- Zachman --> 6 questions vs 6 views matrix
- SABSA --> like Zachman, risk-driven
- TOGAF --> break org into components to build sec

**Security models**
- **_lattice-based_** (layers of confid/integrity w/ rules to write/read between them(
  - Bell-LaPadula --> confidentiality
    - only read down / only write up
  - Biba --> integrity
    - only read up / only write down
  - Lipner implementation --> both confid & integrity
- **_rule-based models_**
  - Clark-Wilson --> integrity
    - defines 3 goals of integrity: well formed transactions, separation of duties & access triple SUBJECT-PROGRAM-OBJECT
  - Brewer-Nash (Chinese Wall) --> prevent conflict of interest
  - Graham-Denning --> rules specifying subj accessing object
  - Harrison-Rizzo-Ullman --> enhancement of Graham-Denning 

**Security frameworks**
- ISO 27001 --> best practice recommendations for ISMS (controls across domains, defining best practices) - can be certified
- ISO 27002 --> implementation guidance for 27001 - cannot be certified here
- NIST 800-53 --> federal agencies
- COBIT --> for IT audit
- COSO --> focused on financial reporting controls
- ITIL --> framework of best practices for delivering IT Services
- HIPAA --> safeguarding PHI
- SOX --> top mgmt must certify the accuracy of financial information; financial records

**Privacy requlation**
- GDPR

**Risk framework**
- NIST 800-37 - RMF - Risk management framework
  - structured process to manage security & privacy risk
  - 6 steps:
    - categorise information systems   
    - select sec controls
    - implement sec controls
    - assess sec contr
    - authoriss IS
    - monitor
- ISO 31000
- COSO
- ISACA Risk IT

# Emanations
any source of radio waves, light, sound, vibration, electrical that radiate from a system and can be eavesdropped

protect against emanation:
- **SHIELDING** (Tempest) --> block the emanation (Faraday, walls, insulation, etc.)
- **WHITE NOISE** --> emit noise to block the emanation
- **CONTROL ZONE** --> physical zone is very secure



{% include links.html %}
