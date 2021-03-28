---
title: Domain 7 Notes
tags: [domain_7]
##keywords: release notes, announcements, what's new, new features
last_updated: Mar 28, 2021
summary: "Notes for  Domain 7"
sidebar: mydoc_sidebar
permalink: 7_notes.html
folder: mydoc
---

# Metadata
- **pseudo** --> user created: comments, track changes, formulas, embedded files
- **file system** --> file attr: date created, date last accessed
- **application** --> appl. created: info about who wrote the docu, doc created date, specific to the application

# Log analysis techniques
- **deduplication** --> remove duplicates
- **correlation** --> relate log entries
- **aggregation** --> consolidate log entries
- **normalization** --> standardize log details

# supporting processes for Configuration Mgmt
- **Asset & Inventory Management** --> ensure CI visibility
- **Change control** --> manage CI changes
- **Version control** --> track/document baseline configs over time

**INVENTORY MANAGEMENT** --> program responsible for documenting/tracking assets

**SecCM - security focused config mgmt** --> CM variant that focuses on the integration of security requirements

**LEAST FUNCTIONALITY** --> devices should be cfg to provide ONLY essential capabilities and specifically prohibit the use of functions/ports/protocols/services

```sh
Least functionality - about objects, least privilege - about subject
```

# Windows service accounts
- **local system** --> very high priv BUILT-IN
- **local service** --> BUILT-IN, same as Users group
- **network service** -->   BUILT-IN, more access than Users group; access netw resources by using the credentials of the computer account

**Group policy** --> centralized management/cfg of OS, apps & users settings in an AD env

**Application sprawl** is the growth of an IT system to include more applications, and to use more resources overall. Systems that suffer from inefficiency due to poor design are often talked about in terms of application sprawl.

# Local storage

- **DAS - Direct Attached Storage** --> locally attached disk
- **NAS - Network Attached Storage** --> storage device accessed via network (shares) - _**file based**_
- **SAN - Storage Area Network** --> enterprise-level storage, accessed via private network using fiber channel, FCoE, iSCSI (_**at block level**_)
- **NUS - Network Unified Storage** --> combines NAS + SAN --> file based + block based

**Virtual storage** --> pool resources to present them as one unit (cloud storage)

# Hardware encryption
hw mechanism to automatically encrypt data written to the magnetic media
- **FDE - Full Disk Encryption**
- **SDE - self-encrypting drives**

#############

**MDM - Mobile device management** --> deploy, secure, monitor, integrate & manage mobile devices in the workplace.

# Mobile device ownership & deployment
- **COBO - Company-owned business only
- **CYOD - Choose your own device
- **COPE - Company-owned personal enabled
- **BYOD - Bring your own device



{% include links.html %}
