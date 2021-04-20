---
title: "Domain 3: Security Architecture and Engineering"
tags: [domain_3]
##keywords: release notes, announcements, what's new, new features
last_updated: Aug 30, 2020
summary: "Secure Hardware Architecture"
sidebar: mydoc_sidebar
permalink: 3_sec_hw_architecture.html
folder: mydoc
---

|.|.|
|-|-|
|**PROCESS**| - executable program and its associated data loaded/running in memory|
|| - HWP - Heavy Weight Process = TASK |
|| - parent process can spawn additional children (threads)|
|**THREAD**| - LWP - Light Weight Process, can share memory|

**Process states**

- NEW --> being created
- READY --> waiting to be exec'd by CPU
- RUNNING --> being exec'd by CPU
- BLOCKED --> waiting for i/o
- TERMINATE --> completed

|.|.|.|
|-|-|-|
|MULTITHREADING| CPU/single core can execute multiple processes/thread concurrently|divides CPU time among child processes (aka threads)|
|MULTIPROCESSING|computer using more than 1 CPU for a task|divide load among multiple CPUs|
|MULTITASKING|tasks sharing a common resource (1 CPU)|divide CPU time among multiple _**processes**_|
|MULTIPROGRAMMING|computer running more than one program at a time||

**Memory protection** --> prevents one process from affecting the CIA of another; used in multi-user/multitasking envs

**Process isolation** --> logical control that prevents one proc interferring w/ another

**Hardware segmentation** --> maps processes to specific memory locations

**Virtual memory** --> provides virt addr mapping btw apps and hw memory

**SWAPPING** --> moves entire processes from RAM to secondary memory (disk)

**PAGING** --> copies block from RAM (pri memory) from/to secondary memory (disk)


**STORAGE**
- _**primary**_ --> info that is required by CPU, volatile
- _**secondary**_ --> non-volatile memory used for long-term storage (HDD, CDROM)


**Faraday cage** --> block electromagnetic signals (radio, wireless, cellular, RFID tags)

**Lockdown enclosure prevents theft of computer equipment**


**CONFINEMENT** --> restricts a process to read/write from/to specific memory locations

**BOUNDS** --> limits of memory a process cannot exceed (read/write)

**ISOLATION** --> process running confined through the use of memory bounds

# Describing vulnerabilitites
needs a common set of standards to provide a common language for describing/evaluating vulns.

**SCAP - Security COntent Automation Protocol**
- common framework, w/ several components
  - _**Common Vulnerabilities and Exposures (CVE)**_ - naming system for describing security vulnerabilities.
  - _**Common Vulnerability Scoring System (CVSS)**_ -  standardized scoring system for describing the severity of security vulnerabilities.
  - _**Common Configuration Enumeration (CCE)**_  -  naming system for system configuration issues.
  - _**Common Platform Enumeration (CPE)**_  -  naming system for operating systems, applications, and devices.
  - _**Extensible Configuration Checklist Description Format (XCCDF)**_ - language for specifying security checklists.
  - _**Open Vulnerability and Assessment Language (OVAL)**_ - language for describing security testing procedures



{% include links.html %}
