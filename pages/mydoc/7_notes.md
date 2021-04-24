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

**cfg mgmt**
- baselining
- patch mgmt
- vuln mgmt

**chg mgmt**
- request chg
- review chg
- approve/reject chg
- test chg
- schedule/implement chg
- document chg

```sh
CHANGE MGMT --> standard process for req/review/approve/implem changes to IT systems

tool for change = RFC - Request for Change
- description
- expected impact
- risk assessment
- rollback pl an
- identity of implementer
- proposed schedule
- affected CI

###

CFG MGMT --> track specific device settings
- baseline = snapshot of a system
- versioning (+ version control)

```



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

# MDM - Mobile device management
deploy, secure, monitor, integrate & manage mobile devices in the workplace.

control categories
- device tracking
- data protection
- authentication
- app/content management

## Mobile device ownership & deployment
- **COBO** - Company-owned business only
- **CYOD** - Choose your own device
- **COPE** - Company-owned personal enabled
- **BYOD** - Bring your own device

device tracking (both can be part of a multifactor auth)
- **geolocation** --> determine its location
- **geofencing** --> define an area where it can be used

## data protection
- **containerization** --> segregate high-risk app by running them in a secure virtual container
- **storage segmentation** --> segment personal from corporate data (different encry policies)
- **full device encryption** --> 
- **DLP** --> copy/paste restrictions


# Incident Management

- **prevention** --> threat modeling, risk assessment, controls implem, monitoring
- **preparation** --> planning, documenting, assign resp, training
- **detection** --> monitoring, reporting, analysis
- **response** --> containment, eradication, recovery

```sh
SETA --> Security Education, Training & Awareness (program)
```

## Incident Response Phases
```sh
highest prio of first responder = containg damage through ISOLATION
```
- **preparation** --> establish incident mgmt capability
- **detection** --> id IOA (indicator of attack) and IOC (indicators of compromise) - logs, SIEM, threat intel
- **containment** --> minimize the damage (disc from network, shutdown)
- **eradication** --> eliminate components of the incident (delete malware, mitigate vulns)
- **recovery** --> restore system to normal operation
- **lessons learned** --> document, root cause, update playbook


```sh
ANOTHER VARIANT

- detection
- response      --> limit damage
- mitigation    --> contain the incident
- reporting
- recovery
- remediation   --> include root cause analysis
- lessons learned --> include root cause analysis
```


**Incident mgmt plan** --> roles & resp, strategies & procedures for preparing/responding to/managing incidents

**Incident playbook** --> set of instructions for plan/respond to a specific type of attack

```sh
AUTO WIPE --> after x failed logins, data protection
REMOTE WIPE --> admin delete (MDM)
```

**INCIDENT COMMUNICATION**
- notify stakeholders
- regular progress update
- documentation for historic purposes

```sh
federal agencies must inform US-CERT of any cybersecurity incident
```

# Detective and preventative solutions

|solution|focus|
|-|-|
|firewall|ingress/egress traffic|
|filters|data access (email, content, URL)|
|IDS/IPS|intrusion attempts|
|NAC|conns to the network|
|DLP|data exfiltration|
|honeypot|knowledge and investigation|
|sandbox|isolation|
|anti-malware|malicious code|

## Firewall security features
- packet filtering
- ACL
- state (stateless - each datagram individually; stateful - can "see" streams)
- L7 (application) filtering
- proxy server - accepts & forwards requests from clients
- NAT

## IDS/IPS

detection approach
- **signature-based** --> known signatures
- **rule-based** --> preconfigured behavior rules
- **behavior-based** --> finds anomalies after being trained for what is normal
- **heuristic** --> continually trains on behavior (cont learning)

**IDS responses**
- logging --> passive
- notification --> passive, informs
- shunning --> passive, ignores
- terminating --> active, end conn
- instructing --> active, makes a config change
- deception --> active, allows attacker thing it's successful

# Vuln mgmt

```sh
VULNERABILITY --> hw/sw weakness that can be potentially exploited.
EXPOSURE --> system/sw config issue that can contribute to a successful exploit/compromise.
```

**patch categories**
- security update
- critical update
- functionality patch
- feature patch

**Threat intel** --> evidence-based info about threats/vulns/exploits

**ISAC - Information Sharing and Analysis Center** --> trusted, sector-specific entity that provides secor-specific info sharing about vulns, threats and incidents.

# Change Mgmt

ITIL terminology for types of changes
- standard --> planned
- normal --> must go through the change process before being approved
- emergency --> time is critical

# Implement recovery strategies

**alternate locations & processing sites**
- **cold site** --> basic building, no IT equip
- **mobile site** --> transportable modular unit
- **warm site** --> HVAC, servers & comm; data needs to be restored
- **hot site** --> HVAC, servers & comm; sys preconfigured, data near-time
- **mirrored site** --> all available, can assume processing on the fly
- **reciprocal site** --> agreement for access to another org's facilities

## Data backup & restoration

**backup strategies**
|type|process|archive bit|restore|
|-|-|-|-|
|FULL|all files||full backup media|
|DIFF|all created/modified from last FULL|no reset|full + last diff|
|INCR|ALL changed files| reset|full + all subsequent incr|

```sh
archive bit --> FS marker that the file has changed
```

**backup rotation cycles**
- **son** --> one full backup cycle (daily)
- **father-son** --> two full backup cycles (week/month)
- **grandfather-father-son** --> three/more backup cycles (week/month/year)

## online backup strategies

|strategy|description|
|-|-|
|cloud backup services|scheduled to an internet location|
|disk shadowing|data r/w to 2/more disks (transparent for the user)|
|electronic vaulting|files backed-up as they change - tx bulk data to an offsite backup storage|
|remote journaling|db: transaction logs periodically copied remote|
|ASR - Automated System Recovery|disk image that can be used to restore OS files|

**replication strategies**
- point-in-time --> periodic snapshots replicated
- async repl --> write = complete when local storage commits; remote has a small lag
- sync repl --> data written to 2 locations, both writes must be complete

## Resiliency & fault tolerance

```sh
AVAILABILITY --> measure of system's uptime (99.9999%)
RESILIENCY --> capability to continue operating when disruption
FAULT TOLERANCE --> capability to continue operating w/ one/more components failed
REDUNDANCY --> duplication of critical components
FAILOVER --> graceful transition to a standby device
```

**SWAPPING** --> process of replacing a failed component
- **warm swap** --> insert/remove hw while system is in a suspended state
- **hot swap** --> insert/remove hw while system is running
- **hot plug** --> add component w/o interruption


# Hypervisor
aka VMM - Virtual Machine Monitor
- type 1 --> installed on bare metal, next to hardware
- type 2 --> installed as app on an OS

**the 5 rules of evidence**
- be authentic
- be accurate
- be complete
- be convincing
- be admissible

# categories of disruption

|||
|-|-|
|**non-disaster**|disruption in service (device malfunction/user error)|
|**disaster**|entire facility unusable for 1/more day(s)|
|**catastrophe**|destroys facility; req short+long term solution|

**BCP/DRP MOU/MOA = Memorandum of Understanding/Agreement**
- legal document acknowledging the responsibility for a certain activity
- "critical stuff is missing, was supposed to be here; what could have fixed the problem?"


{% include links.html %}
