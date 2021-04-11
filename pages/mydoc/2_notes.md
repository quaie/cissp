---
title: "Domain 2: Asset security"
tags: [domain_2]
#keywords: release notes, announcements, what's new, new features
last_updated: Apr 3, 2021
summary: "Notes for Domain 2"
sidebar: mydoc_sidebar
permalink: 2_notes.html
folder: mydoc
---

```
SENSITIVITY --> amount of damage that would be done if info is disclosed
CRITICALITY --> time sensitivity of data - how much revenue the asset generates; damage done if info unavailable
```
**Data classification policies**
- FORMAL ACCESS APPROVAL --> data owner approves access (written document)
- NEED TO KNOW --> (applied to DATA) need VALID reason to access the data
- LEAST PRIVILEGE --> (applied to ACTIONS) users have minimum necessary access to perform their job duties

**Sensitive information**
- DATA HANDLING --> policies for HOW/WHERE/WHEN/WHY data was handled
- DATA STORAGE --> where is data kept
- DATA RETENTION --> not kept beyond its period of usefulness/legal req's

**STATES OF DATA**

| state | protection method |
| ------ | ------ |
| at rest | FS encryption |
| in use| physical security, screen protectors |
| in transit| SSL/TLS (VPN, IPv6 built-in encryption |

**THREATS TO DATA AT REST (on storage)**

| threat | countermeasure |
| ------ | ------ |
| **_unauth usage/access_** | - strong auth |
|| - encryption |
|| - obfuscation, anonymization, tokenization, masking |
|| - org policies & layered defence |
| **_liability due to non compliance_** | - due care & due diligency |
|| - SLAs|
| **_DoS/DDoS_**| - redundancy|
|| - data dispersion|
| **_corruption, modification, destruction of data_**| - hashes/digitally signed files |
| **_data leakage/breaches_** | - DLP - Data Loss Prevention |
| **_theft/accidental media loss_**| - encryption | 
| **_malware attack_** | - anti-malware |
| **_improper sanitization at end of data lifecycle_** | - destroy data if end of life |

```
DATA DISPERSION --> data replicated in multiple physical locations (cloud).
DATA FRAGMENTATION --> dataset split into smaller fragments (shards) distributed across several servers
```

**DLP - Data Loss/Leakage Prevention**
- controls put in place to ensure that certain types of data remain under org control in line w/ policies/standards/procedures
- help ensure compliance w/ PCI-DSS, HIPAA, etc
```
OBFUSCATION --> hide/replace/omit sensitive info
MASKING --> use specific chars to hide parts of a dataset
DATA ANONYMIZATION --> encrypt/remove PII from datasets
TOKENIZATION --> access to tokenized data, not real data
PSEUDONYMIZATION --> aliases to represent other data (id instead of username)
```

**DRM - DATA rights management**
- aka IRM - Information Rights Management
- extra layer of access controls on top of the data object to control print/save/copy/etc.
- travels w/ the data, agnostic of its location; IRM travels w/ the file

**DATA REMANCENCE**
**_residual data that remains on storage/memory after a file/data has been deleted/erased._**


**ILM - Information Lifecycle Management**

|stage|remarks|
|-|-|
|CREATION|-classified & owner is assigned|
|DISTRIBUTION|- "data in motion"|
||- vulnerable to compromise |
||- encryption, DLP (Data Loss Prevention) technologies |
|USE|-"data in use"|
||- accessed by user/app & actively being used|
||- must be accessed only on auth systems by auth ppl|
|MAINTENANCE|- "data at rest"|
||- data on any kind of storage for backup, archive, etc.|
||- review of classif levels, encryption|
||- protect for CIA|
||- Confidentiality: system/dir/file permissions & encryption|
||- Integrity: hashes, CRC, file locking|
||- Availability: db/file clustering, backup, real-time replication|
|DISPOSITION|- data has no longer value --> properly destroyed|

**Removing data remnants**
- ERASING --> OS delete, only marks storage space as unavailable (if not overwritten, can be read)
- CLEARING --> overwriting, data inaccessible by normal means
- PURGING --> data overwritten several times
- DEGAUSSING --> magnetic field; ineffective against SSD's
- DESTRUCTION --> phy destruction, **irreversible

**CONTROL SELECTION FRAMEWORKS**

- PCI-DSS
- ISO 27001/2
- OCTAVE ---> self-directed risk management
- COSO --> goals for the entire organisation
- COBIT --> goals for IT
- ITIL --> IT service mgmt
- FRAP --> Facilitated Risk Analysis Process

```
SCOPING --> which portions of a standard will be used
TAILORING --> customize a standard to implement in an org
```

```
CERTIFICATION --> certified to meet the security reqs of the data owner
ACCREDITATION --> data owner's acceptance of certification & residual risk, before it goes into prod
```

**SECURITY MARKING** --> use of human-readable security attr; reflects laws, policies, standards; enable organisational process-based enforcement of policies

**SECURITY LABELING** --> use of security attr for internal data structures withing information systems

# GDPR

|||
|-|-|
|**data processor**|processes personal data on behalf of data controller|
|**data controller**|controls processing|
|**data transfer**|not outside EU|
|**anonymization**|remove all relevant data to make id of the subject impossible (if done ok, GDPR is no longer relevant; data is modified|
|**pseudonymization**|use aliases to represent other data|

# Security Test & Evaluation Program
- req'd for certif & accred of all US gov agencies according to FISMA
- management controls --> risk mgmt & management of info sec (perform risk assess/ensure inventory of all assets exists)
- operational controls --> processes exec/implem by people (sec training program/AUP signed)
- technical controls --> processes implem/exec by hw/sw mech. (change passwd regularly/logon display)

{% include links.html %}
