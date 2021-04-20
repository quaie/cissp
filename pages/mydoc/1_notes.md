---
title: "Domain 1: Security and Risk Management"
tags: [domain_1]
#keywords: release notes, announcements, what's new, new features
last_updated: Apr 3, 2021
summary: "Notes for Domain 1"
sidebar: mydoc_sidebar
permalink: 1_notes.html
folder: mydoc
---

# CIA
- **confidentiality** --> only auth subjects access objects
- **integrity**       --> no modif w/o authorization
- **availability**    --> it's there when it's needed

# ISC2 code of ethics (short version)

1. Protect society, commonwealth and the infrastructure
2. Act honorably, honestly, justly, responsibly and legally
3. Provide diligent & competent service to principals
4. Advance & protect the profession




**DUE DILIGENCE** --> practicing the activities that maintain due care _**before decision**_
- research, planning, evaluation
- best practices, ind standards, laws & regulations
- INCREASES understanding, REDUCES risk

**DUE CARE** --> do what a reasonable person would do _**after decision**_
- implementation, upkeep, measures
- report sec incidents, sec awareness training, disable access
- "prudent man" rule

**Security planning**

- **STRATEGIC** --> long term, CISO
- **TACTICAL**  --> medium term, IT manager
- **OPERATIONAL** --> short term, IT engineer

# 4 levels of security policy development

- acceptable use policy --> assign roles & responsibilities
- baseline              --> minimum levels
- guideline             --> recommendaations
- procedure             --> step-by-step description

# Response to risk

1. **ACCEPT**     --> do nothing
2. **MITIGATION** --> implement countermeasure & accept residual risk
3. **ASSIGNMENT** --> transfer to 3rd party (insurance)
4. **AVOID**      --> mitigating costs > benefits, let it go ...
5. **DETERRENCE** --> implement deterrents to would-be violators (video surveillance)
6. **REJECTION**  --> aka ignore, DON'T DO IT!!!

# Risk mgmt frameworks

1. NIST 800-37 --> _**the only one relevant for the exam**_
2. OCTAVE - Operationally Critical Threat, Asset and Vuln Evaluation
3. FAIR - Factor Analysis of Information Risk
4. TARA - Threat Agent Risk Assessment

## NIST 800-37 steps
- **prepare** to execute the RMF
- **categorize** IS
- **select** security controls
- **implement** sec controls
- **assess** sec controls if work correctly
- **authorize** the system
- **monitor** sec controls 

```sh
!!! NOT EVERY RISK CAN BE MITIGATED --> mgmt decides how the risk is handled --> HUMAN LIFE = HIGHEST IMPORTANCE

legal issues are involved --> "call an attorney"
```

# Types of risk

- **RESIDUAL**  --> remains after safeguards - AFTER safeguards
- **INHERENT**  --> newly identified, not yet addressed (absence of controls) - BEFORE safeguards
- **TOTAL**     --> amount of risk if no safeguards were implemented - NO safeguards

**controls gap** --> amount of risk reduced by implementing safeguards



```sh
threats X vulnerabilities X asset value = total risk

rusk = threat * vulnerability

total risk - controls gap = residual risk
```

# Risk analysis

1. **QUANTITATIVE** --> assign $ value to evaluate effectiveness of countermeasures; works with VALUES; is **objective**
      - six steps in quantitative risk analysis
        - inventory assets & assign a value --> **AV = asset value**
        - identify threats --> calculate EF & SLE - **EF - Exposure Factor (percentage destroyed), SLE = Single Loss Expectancy**
        - perform a threat analysis --> likelihood of each threat within a year - **ARO = Annual Rate of Occurence (expected frequency)**
        - estimate the potential loss --> **ALE = annualized loss expectancy (possible yearly cost)**
        - research countermeasures for threats & calculate their improvements
        - perform cost/benefit analysis --> see if the value is positive
      
2. **QUALITATIVE**  --> uses a scoring systems to rank threats & effectiveness of countermeasures; is **subjective**
        - Delphi technique --> anonymous feedback/response to arrive at a consensus


**LOSS POTENTIAL**        --> what would be lost if the threat agent is successful

**DELAYED LOSS**          --> amount of loss that can occur over time

**SAFEGUARD EVALUATION**    --> mitigate risk, cost effective & difficult to bypass

```sh

SLE = AV * EF

ALE = SLE * ARO

ALE before safeguard - ALE after safeguard - annual cost of safeguard = VALUE OF SAFEGUARD
```

**SUPPLY CHAIN** --> chain of multiple entities delivering a service; must be secure, reliable, trustworthy

**supply chain evaluation**
- on-site evaluation
- document exchange & review
- process/policy review
- third-party audit

# Threat modeling
security process where potential threats are id, categorised and analysed.

goal: eradicate/reduce threats

can be focused on:
- **assets** --> use asset evaluation results to id threats
- **attackers** --> based on attacker's goals
- **software** --> potential threats against the sw

## Threat modeling methodologies

1. STRIDE (Microsoft)
      - Spoofing
      - Tampering
      - Repudiation
      - Information disclosure
      - DoS
      - Elevation of privilege
2. PASTA --> focuses on controls relative to asset value
3. VAST  --> based on Agile 
      - Visual
      - Agile
      - Simple
      - Threat
 4. TRIKE --> focuses on a risk-based approach
 5. DREAD --> ?
      - Damage potential
      - Reproducibility
      - Exploitability
      - Affected users
      - Discoverability
 6. Diagramming potential attacks
 7. Reduction analysis --> 
            - trust boundary --> any location where the level of trust/security changes
            - data flow paths --> movement of data
            - input points --> external input
            - privileged operations --> greater privs than of a standard user

**SECURITY CONTROLS** --> safeguard = proactive, countermeasure = reactive

_**categories**_:
- technical (hw, sw)
- administrative (policies, procedures)
- physical (can touch)


_**types**_:
- **deterrent** - discourage
- **preventative** - stop
- **detective** - discover/detect
- **compensating** - aid other controls
- **corrective** - modify env to return systems to normal after smth has happened
- **recovery** - extension of corrective w/ more capabilities
- **directive** - direct/confine/control actions of subjects to force/encourage compliance

# Legal and regulatory

- criminal law
- civil law
- administrative law


**LAWS**
- CFAA - first US cybercrime-specific
- FISMA - infosec operations for federal agencies
- DMCA - literary/musical works

**Intellectual property**
- trademark
- patent
- trade secret
- copyright

**Licensing**
- contractual --> written contract
- shrink-wrap --> written outside of the sw package
- click-through --> click button to agree
- cloud services --> link & checkbox for terms/conditions

**privacy laws**
- HIPAA - health
- HITECH - health
- Gramm-Leach-Bliley --> financial institutions
- COPPA --> Children's Online Privacy Protection Act
- ECPA --> Electronic Communications Privacy Act
- CALEA --> Comms Assistance for Law Enforcement Act

```sh
awareness = WHAT
sec training = HOW
sec education = WHY
```

{% include links.html %}
