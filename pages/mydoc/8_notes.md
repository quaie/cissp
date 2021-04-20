---
title: Domain 8 Notes
tags: [domain_8]
##keywords: release notes, announcements, what's new, new features
last_updated: Mar 29, 2021
summary: "Notes for  Domain 8"
sidebar: mydoc_sidebar
permalink: 8_notes.html
folder: mydoc
---

# SDLC - systems development life cycle
- system development model
- in the context of CISSP --> secure systems development LC
- **prepare a sec plan**
- **initiation**
  - conduct a sensitivity assessment
- **dev/acquisition**
  - determine sec reqs
  - incorporate sec reqs in specifications
- **implementation**
  - install controls
  - sec testing
  - accreditation
- **operation/maintenance**
  - sec operations & administration
  - operational assurance
  - audits & monitoring
- **disposal**
  - destroy/archive info
  - media sanitization/destruction

- [SDLC](https://www.youtube.com/watch?v=pnS1z-KyxfM){:target="_blank"}.
- [SDLC](https://www.youtube.com/watch?v=Xe5qQBI8MeM){:target="_blank"}.
- 

# CASE - computer-aided software engineering
uses programs to assist  in the creation/maint of other programs

three types of CASE software:
- **tools** --> support only a specific task
- **workbench** --> integrate several tools in a single app
- **environment** --> collection of tools and workbenches

# Types of publicly released software

- **closed source** --> released in executable form, source code = confi
- **open source** --> source code = public
- **proprietary** --> subject to intellectual property protections

- **free software** --> free of charge (gratis) or free to modify it (libre)
- **freeware** --> free of charge to use
- **shareware** --> fully functional proprietary sw that can be used for free initially
- **crippleware** --> proprietary sw w/ key features disabled (pay for the full version)

# Application development models

**Waterfall model**
- linear, rigid phases; steps come in sequence, _**not possible to go back to the previous step**_
- _**modified waterfall**_ --> can return to previous phase for verif/validation

**Sashimi model**
- like waterfall, but with overlapping phases

**Agile**
- modern concepts, include Scrum & XP

**Scrum**
- team works as a unit: scrum team, scrum master, product owner

**XP - extreme programming**
- Agile dev method: pairs of programmers working together a detailed specification

**Spiral**
- designed to control risk
- repeats steps of a project, starting small, expanding outwards -- **rounds**
- each round --> is a project w/ own sw dev method
- risk analysis - each round

**RAD - Rapid Application Development**
- uses prototypes (dummy GUI, db, etc)
- goal = quickly meet the business needs, technical = secondary
- customer = heavily involved

```sh
CHANGE MGMT --> manage changes made to the systems (WHY) - formal review/approval from all stakeholders before implem
CONFIG MGMT --> record modifications to a prod environ (WHAT)
```

**GANTT chart** --> bar chart that shows the interrelationships over time between projects and schedules. It provides a graphical illustration of a schedule that helps to plan, coordinate, and track specific tasks in a project.

**PERT (Program Evaluation Review Technique)** --> project-scheduling tool used to judge the size of a software product in development and calculate the standard deviation (SD) for risk assessment. used to direct improvements to project management and software coding in order to produce more efficient software

# Maturity models
to benchmark the software development maturity
- **CMMI - Capability Maturity Model Integration** --> defines 5 levels
  - _**initial**_ 
  - _**managed**_
  - _**defined**_
  - _**quantitatively managed**_
  - _**optimizing**_

- **SAMM - Software Assurange Maturity Model** --> open framework geared towards including sec features

- **BSIMM - Building Security in Maturity Model** --> measure the extent to which sec is included in software dev processes

- **AMM - Agile Maturity Model** --> sw process improvement model for Agile

# Integrated Product Team --> TBD
- customer-focused group that focuses on the entire lifecycle of a project
- multidisciplinary group, collectively responsible
- no strict hierarchy, involves ppl from various org structures

**software escrow** --> third party stores an archive of the software code

# Threat modeling
systematic & detailed analysis of all interfaces, API & interaction w/ components (db, OS) - try to understand the ways in which they could be misused/abused

**STRIDE** --> threat classif. model
- Spoofing of user identity
- Tampering
- Repudiation
- Info disclosure
- DoS
- Elevation of privilege

# Software testing

**reasonableness check** --> ensures that values returned by software match specified criteria that are within reasonable bounds (500 kg human weight?!)

software testing methods
- black box testing --> from user's perspective, input something; NO ACCESS TO CODE
- white box testing --> internal logical structure, CODE line by line
- grey box testing  --> combines both above, popular for sw validation; code used to define tests, not analysed


**tests for security app**
- **STATIC** --> analyses code w/o running it
- **DYNAMIC** --> code runs

# Databases

**relational** --> two-dimensional tables (rows aka tuple + columns aka attributes)

**primary key** --> unique value in each row

**candidate key** --> any column w/ unique values

**foreign key** --> key that matches a primary key in another table

**DB integrity**
- _**referential**_ --> every foreign key matches a primary key
- _**semantic**_ --> each column value is consistent w/ the attribute data type
- _**entity**_ --> each row has a unique non-null primary key

**normalization** --> data is logically concise, organised & consistent; removes duplicates

**DB view** --> results of a query, used to provide a constrained user interface

**SDLC - systems development life cycle**

1. initiation/planning --> idea & objectives
2. func. req. definition --> how the functions will fit the users
3. system design specifications --> how data enters the system, flows and exits
4. dev & implem --> source code
5. docu & common program controls --> documentation, logging
6. acceptance --> tested by a third party (func & sec tests)
7. testing & evaluation controls --> guidelines how testing will be conducted
8. certification --> compared against set of standards to ensure it complies
9. accreditation --> mgmt approves system for implementation
10. implementation --> from dev to prod

_**additional in the larger SLC process:**_

11. operations & maintenance --> live prod, monitored & patched, etc
12. revisions & system replacement --> evaluate for new functionalities/retired

**INFERENCE** --> deduce sensitive info based on available info

**AGGREGATION** --> combine benign info from several sources to reveal sensitive info

# Storage types

|||
|-|-|
|primary memory| directly available to CPU - most high perf|
|secondary storage|long term, HDD, DVD|
|virtual memory|simulate pri memory by using secondary storage (swapping)|
|virtual storage|simulate secondary storage by use primary storage (RAM disk)|
|random access storage|RAM/HDD - OS can request contents from any pont within the media|
|sequential access storage|tape - requires scanning through entire media from beginning to reach a specific addr|
|volatile storage|loses content when power down - RAM|
|nonvolatile storage|survives a reboot - magnetic, optical, NVRAM|

# Knowledge-based AI systems

**EXPERT SYSTEMS**
- applies accumulated knowledge to future decisions
- 2 components:
  - _**knowledge base**_ --> contains rules, codified as series of if-then statements
  - _**inference engine**_ --> analyses information in KB to reach a decision

**MACHINE LEARNING**
- use analytic capabilities to develop knowledge from datasets without the direct application of human insight
- allow the computer to analyze and learn directly from data, developing and updating models of activity
- 2 categories:
  - _**supervised learning**_ - labeled data; dataset + correct answers and algorithm develops a model for future cases
  - _**unsupervised learning**_ - unlabeled data; no correct answers, alg has to develop a model independently

**NEURAL NETWORKS**
- chains of computational units are used in an attempt to imitate the human brain (reasoning)
- extension of ML, **aka deep learning / cognitive systems**
- **Delta (learning) rule** --> neural networks are able to learn from experience

```sh
EXPERT SYSTEM --> rules stored in knowledge base
NEURAL NETWORK --> long chain of computational decisions feed into each other and sum to produce the desired output
```


{% include links.html %}
