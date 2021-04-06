---
title: Domain 6 Notes
tags: [domain_6]
##keywords: release notes, announcements, what's new, new features
last_updated: Jan 16, 2020
summary: "Notes for  Domain 6"
sidebar: mydoc_sidebar
permalink: 6_notes.html
folder: mydoc
---

# Assessment
--> determine how effectively the entity being evaluated meets specific sec criteria (assurance)

- **EXAMINATION**
  - passive, interview, review, inspect, study to understand/obtain evidence; NON INTRUSIVE
  - determine if documentation is proper, focus on policies/standards, etc.

- **TESTING**
  - active, do smth to compare actual/expected behaviors; INTRUSIVE
  - identify vulns, pentesting, password cracking, social engineering

E + T can be conducted:
- internal personnel
- external personnel
- overt --> known to affected personnel, cooperative
- covert --> adversarial, known to few people

T + E can be required contractual or regulated (GLBA, FISMA, PCI-DSS)

# ROE - Rules of Engagement
document that details the parameters/conduct of an assessment (test/examination)

components:
- scope --> selection of assessment objects (based on size, complexity, sampling)
  - sampling --> infer characteristics based on a sample; **evidence sampling** --> apply procedure to less than 100% of the population; **sampling risk**
  - sampling techniques
    - statistical sampling --> objective, each item has an equal probability of selection
    - non-statistical sampling --> subjective, included items are based on professional judgement
    - block sampling --> all items in a selected time period, numerical/alphabetical sequence
  - sampling approaches
    - fixed sample plan --> % of occurence in a defined population (how many)
    - stop and go sampling --> stop once a reasonable conclusion can be drawn
    - discovery/exploratory sampling --> single instance is enough (fraud, illegal activity)
- level of expertise/methodology
- logistics/comm plan
  - location (access to target - phy/logical)
  - timing (outside business, maint windows)
  - notification (internal, 3rd party, customers)
- data handling req
- reporting expectations
- assessor responsibilities
- legal considerations
  - authorization
  - liability
  - indemnification
  - non-disclosure
  - privacy

# Infrastructure assessment

- system config examination
- log review
- vuln assessment
- pentesting
- red team/blue team exercise --> simulated attack (preparedness/response capabilities)


**pentest types**
- black box (blind) --> pentester = no details, target knows
- double blind --> pentest = no details, target doesn't know; COVERT
- gray box --> pentest = limited knowledge, target knows
- white box (targeted) --> pentester + target work together; OVERT

**pentest phases**
- passive recon
- active recon
- attack planning
- attack & exploitation - depends on the RoE - proof of concept or actual exploit
- reporting --> vuln findings, exploit activities & recommendations (mitigation, etc)
- remediation & retesting

# Code Testing & Analysis

**Sec code assessment** --> examine/test source code to verify that proper sec controls are in place and function as intended.

- **tatic code analysis** --> static, read code
- **dynamic analysis** --> running code
- **fuzzing** --> automated; feed invalid, unexpected, random data
- **quality & performance testing** --> response to use & misuse
  - use case --> normal conditions
  - misuse case --> unexpected input, adverse conditions
  - load testing --> normal/peak conditions
  - volume testing --> incremental volume of records (not users)
  - stress testing --> abnormal number of users
  - synthetic transactions --> emulate a specific interaction to measure availability + response times
- **regression testing** --> functionality & security post-change (patch, update, config modif)


# Collect Security Process Data
security devices generate reports about their function

**IOA** - indicator of attack (attack is coming/already happeing)

**IOC** - indicator of compromise (already exploited)

**system custodian** --> cfg monitoring & respond to output, authorize & implement change

**security analyst** --> analyze activity & report errors

# Information Security Cont. Monitoring
program to maintain ongoing awareness of vulns/threats to support risk mgmt solutions; NIST SP800-137

maps to risk tolerance; involves management; adapts to ongoing needs

- define
- establish
- implement
- analyse/report
- respond
- review/update

ISCM needs the definition of:
- metrics --> standard of measurement
- freq of data collection
- implem tools & methodologies

**SCAP Security COntent Automation Protocol** --> enables automated vuln mgmt, measurement & policy compliance.

**NVD - National Vuln Database** --> US gov repo of vuln mgmg data in SCAP format


# Analyze Test Output & generate report

**test & operational data flow**

- collect output
- analyze data
- produce actionable intelligence
  - operational metrics - vuln/threat/risk mgmt decisions
  - KPI - Key Performance Indicators, business metrics
  - Business Intelligence - supports allignment & long-term planning
    - data warehousing - combines data from various sources over time
    - data mining - looks for trends, patterns, anonalies
    - predictive analytics - attempt to predict smth based on past data
    - aggregation - summarization of data











{% include links.html %}
