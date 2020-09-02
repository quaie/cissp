---
title: "Domain 2: Asset security"
tags: [domain_2]
#keywords: release notes, announcements, what's new, new features
last_updated: Aug 29, 2020
summary: "CEO Domain 2"
sidebar: mydoc_sidebar
permalink: 2_ceo.html
folder: mydoc
---

------------------------------------------------------------------
**_Certification Exam Outline_**

`2.1 Identify and classify information and assets`
> classification is a critical first step to better and more secure asset and data management, providing valuable insight into an environment
- Data classification
> civil vs mil+gov: public --> confidential, unclassified --> top secret
- Asset Classification
> -inventory of assets & their owners/responsible persons

`2.2 Determine and maintain information and asset ownership`
> - data owners and data processors will have  clearly outlined roles
`2.3 Protect privacy`
- Data owners
- Data processers
- Data remanence
- Collection limitation
> _(Collection Limitation Principle: Collection of personal data should be limited, obtained by lawful and fair means, and with the knowledge of the subject.)_

`2.4 Ensure appropriate asset retention`
> -  applies to record & media: data is kept in a usable state while needed & destroyed when no longer needed
> - audit trail data must be kept to reconstruct past incidents
> - 
`2.5 Determine data security controls`
- Understand data states
> at rest/in motion/in use
- Scoping and tailoring
>
> SCOPING --> which portions of a standard will be used
> 
> TAILORING --> customize a standard to implement in an org
>
- Standards selection
>
> org need to ensure the controls comply w/ certain external security standards (PCI-DSS, GDPR for example)
> 
> need to identify the standards that apply and assure controls comply w/ them
>
- Data protection methods
> - confidentiality --> encryption (at rest/in motion)
> - backups: full, differential (only data changed from last full), incremental (only changed data from last diff/full)
> - db mirroring, snapshots, availability zones (cloud), vaulting (physical)
> - data deduplication
> - RAID (0-6, 10)

`2.6 Establish information and asset handling requirements`
> - combinations of phy/adm/tech controls that assist security professionals in establishing the handling requirements for sensitive information and valued assets.
> - marking, handling, declassification, storage
> - declassify data --> remove/obfuscate sensitive elem: de-identification, obfuscation, anonymization, tokenization

------------------------------------------------------------------


{% include links.html %}
