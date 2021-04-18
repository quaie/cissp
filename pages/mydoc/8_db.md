---
title: Databases
tags: [domain_8]
##keywords: release notes, announcements, what's new, new features
last_updated: Mar 29, 2021
summary: "Notes for  Domain 8"
sidebar: mydoc_sidebar
permalink: 8_db.html
folder: mydoc
---
# Databases

**relational** --> two-dimensional tables (rows aka tuple + columns aka attributes)

**keys** --> subset of fields, uniquely id records
- **primary key** --> unique value in each row; ONE PER TABLE
- **candidate key** --> any column w/ unique values
- **foreign key** --> key that matches a primary key in another table

**cardinality** = # of rows

**degree** = # of columns



**DB integrity**
- _**referential**_ --> every foreign key matches a primary key
- _**semantic**_ --> each column value is consistent w/ the attribute data type
- _**entity**_ --> each row has a unique non-null primary key

**normalization** --> data is logically concise, organised & consistent; removes duplicates
- 1NF
- 2NF
- 3NF


**DB view** --> results of a query, used to provide a constrained user interface

**TRANSACTIONS**
- ensure data integrity
- set of SQL instructions that succeed/fail as a group
- commit/rollback
- required characteristics - ACID:
  - Atomicity - "all or nothing": one fails, transaction fails
  - Consistency - 
  - Isolation - separate from each other
  - Durability - once commited, must be preserved (transaction logs)
  
 **CONCURRENCY** --> aka edit control - preventive sec mech that makes certain that info stored in db is always correct (Integrity + Availab protected)
 - uses the LOCK feature, to block the element
 
 no concurrency:
 - **LOST UPDATES** -->two diff processes make updates unaware of each other 
 - **DIRTY READS** --> record from an unsuccessfully committed transaction is read

**Open Database Connectivity (ODBC)** --> proxy btw app - backend db, more freedom for programmers to interact w/ db

|.|.|
|-|-|
|REPLICATION|cpoy data btw live mirrors of a single db; backup or HA/redundancy; BOTH visible to users|
|SHADOWING|copy data from live db to a backup, read-only db; USERS don't see the shadow|


{% include links.html %}
