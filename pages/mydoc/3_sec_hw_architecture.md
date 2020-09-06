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

|.|.|
|-|-|
|MULTITHREADING| CPU/single core can execute multiple processes/thread concurrently|
|MULTIPROCESSING|computer using more than 1 CPU for a task|
|MULTITASKING|tasks sharing a common resource (1 CPU)|
|MULTIPROGRAMMING|computer running more than one program at a time|

**Memory protection** --> prevents one process from affecting the CIA of another; used in multi-user/multitasking envs

**Process isolation** --> logical control that prevents one proc interferring w/ another

**Hardware segmentation** --> maps processes to specific memory locations

**Virtual memory** --> provides virt addr mapping btw apps and hw memory

**SWAPPING** --> moves entire processes from RAM to secondary memory (disk)

**PAGING** --> copies block from RAM (pri memory) from/to secondary memory (disk)

_

{% include links.html %}
