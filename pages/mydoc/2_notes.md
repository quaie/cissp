---
title: Domain 2 Notes
tags: [domain_2]
#keywords: release notes, announcements, what's new, new features
last_updated: Aug 29, 2020
summary: "Notes for the Domain 2"
sidebar: mydoc_sidebar
permalink: 2_notes.html
folder: mydoc
---
```
SENSITIVITY --> amount of damage that would be done if info is disclosed
CRITICALITY --> time sensitivity of data - how much revenue the asset generates; damage done if info unavailable
```
**STATES OF DATA**

| state | protection method |
| ------ | ------ |
| at rest | FS encryption |
| in process| physical security, screen protectors |
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
```

**DRM - DATA rights management**
- aka IRM - Information Rights Management
- extra layer of access controls on top of the data object to control print/save/copy/etc.
- travels w/ the data, agnostic of its location; IRM travels w/ the file

**Removing data remnants**
- CLEARING --> overwriting, data inaccessible by normal means
- PURGING --> degaussing, media unusable by normal means
- DESTRUCTION --> phy destruction, **irreversible


# 1
## 2
### 3

{% include links.html %}