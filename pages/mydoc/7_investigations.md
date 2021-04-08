---
title: Investigations and Forensics
tags: [domain_7]
##keywords: release notes, announcements, what's new, new features
last_updated: Mar 28, 2021
summary: "Notes for  Domain 7"
sidebar: mydoc_sidebar
permalink: 7_investigations.html
folder: mydoc
---

# Investigations

- administrative --> internal (operational investigations - resolve tech issues; root cause analysis)
- criminal --> beyond a reasonable doubt standard of evidence
- civil --> between parties; preponderence of the evidence standard
- regulatory --> compliance w/ industry standards

**documentary evidence rules**
- **authentication rule** --> must be auth by testimony
- **best evidence rule** --> original superior to copies
- **parol evidence rule** --> written contracts are assumed to be the entire agreement

# Forensics
the process of collecting/preserving/examining/analysing/presenting EVIDENCE

**legal hold** --> order that suspends the modif/deletion/destruction of records & media; issued to avoid _**evidence spoliation**_ (alter/destroy evidence)

**order of volatility** --> acquisition of evidence before it disappears/overwritten:
- RAM
- dump files
- temp files
- log files
- static data (media)

**data acquisition tools**
- memory imaging --> dump RAM
- write blocker --> intercepts device writes
- bit stream image --> bit by bit copy preserving everything, doesn't change data
- clone --> exact copy of the entire HDD (data, residual data, slack)

```sh
hash the media before using the tools above; HASH = FINGERPRINT

hash also the cloned media & at the end of the examination the fingerprints must be the same
```

**file recovery**

|tool|purpose|
|-|-|
|cluster|fixed length blocks of disk space (referenced in FAT)|
|slack space|space btw end of file - end of cluster|
|unallocated (free) space| clusters not allocated to a file. _**CARVING**_ = deleted files/fragments are recovered|
|metadata|data about data (see below)|

**Metadata**
- **pseudo** --> user created: comments, track changes, formulas, embedded files
- **file system** --> file attr: date created, date last accessed
- **application** --> appl. created: info about who wrote the docu, doc created date, specific to the application

# Investigation

internal investigations can lead to **administrative hearing** (trial-like process before an administrative agency), can morph into civil/criminal case

**witnesses**:
- _**factual**_ - individual who has directly participated/observed; CAN ONLY TELL THE STORY
- _**expert**_ - person with knowledge, CAN GIVE AN OPINION



# Log analysis techniques
- **deduplication** --> remove duplicates
- **correlation** --> relate log entries
- **aggregation** --> consolidate log entries
- **normalization** --> standardize log details
- **synchronization** --> NTP synced
- **identification** --> identify normal/abusive activity


**network forensics - NETFLOW DATA** --> summarizes traffic, high-level info (IP addr, ports, timestamp + amount of data)


{% include links.html %}
