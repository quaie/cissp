---
title: "Domain 3: Security Architecture and Engineering"
tags: [domain_3]
##keywords: release notes, announcements, what's new, new features
last_updated: Sep 04, 2020
summary: "Security Models"
sidebar: mydoc_sidebar
permalink: 3_sec_models.html
folder: mydoc
---

# Security models

|model|name|Remarks|
|-|-|-|
|DAC|Discretionary Access Control|subjects = full control of objects created/given access to |
|MAC|Mandatory Access Control|system-enforced access based on subject's clearance & object's labels|
|RBAC|Role Based Access Control|access based on the role of the subject|
|ABAC|Attribute Based Access Control|access to obj granted to subj/obj/environ conditions: name/role/id/owner/etc|
|RUBAC|Rule Based Access Control|access granted on if/then statements|

**Bell-LaPadula (confidentiality, MAC)** 

- simple security property "**NO READ UP**" 
- \* security property "**NO WRITE DOWN**" 
- strong * property "**NO READ/WRITE UP/DOWN**" --> access data only at own level

**Biba (integrity, MAC)**

- simple integrity axion "**NO READ DOWN**" 
- \* integrity axion "**NO WRITE UP**" 
- invocation property "**NO READ/WRITE UP**"

**Clark-Wilson (integrity)**

- subject/program/object --> all transactions via program
- "well-formed transactions" --> series of ops that transition to another consistent state
- "separations of duties" --> certifier is different from implementer
- requires that users are authorized to access/modify data


**Brewer-Nash (Chinese Wall)**

- not concerned w/ data flow, but w/ what a subject knows about the state of the system
- no info can flow in a way that would create conflict of interests
- any actions at a higher level do not affect/interfere w/ actions at lower level


# Security Frameworks

**Zachman Framework**

- 6 questions (what/how/where/who/when/why) mapped to rules for 6 roles (planner/owner/designer/builder/programmer/user)


# Security Modes

- can be MAC/DAC
- systems contain info at various levels of security classification
- mode is determined by:
-- type of users accessing
-- type of data processed
-- type of levels of users, their need to know

|security mode| description|
|-|-|
|DEDICATED|system contains **only one classif label**|
|SYSTEM HIGH|mixed labels, subjects must possess a **clearance equal to the system's highest object**|
|COMPARTIMENTED|all subjects have clearance, but not appropr. formal access approved, nor need to know for all info --> compartments|
|MULTILEVEL|different labels and allows access from subjects w/ different clearances|


# Trusted Computing Base
combo of hw/sw/controls working together to enforce a sec policy; only portion that can be trusted

**security perimeter** --> imaginary boundary that separates TCB from the rest of the system

TCB must create secure channels to comm w/ rest of the system

**reference monitor** --> enforces access control, logical part of TCB confirming the access rights before granting access

**security kernel** --> implements access control, implement the func of the reference monitor







{% include links.html %}
