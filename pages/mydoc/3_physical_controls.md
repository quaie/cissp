---
title: "Domain 3: Security Architecture and Engineering"
tags: [domain_3]
##keywords: release notes, announcements, what's new, new features
last_updated: Apr 04, 2021
summary: "Physical security controls"
sidebar: mydoc_sidebar
permalink: 3_physical_controls.html
folder: mydoc
---

1. administrative
  - policies & procedures, facility selection, personnel controls, awareness, site management

2. logical
  - technical controls - alarms, CCTV, HVAC, fire detection

3. physical
  - physical means - fences, lighting, locks, dogs/guards, mantraps
  - ideal humidity - 40 - 60 percent
  - ideal temp - 15 - 23 Celsius

```sh
there is no security without physical security !!!
```

|||
|-|-|
|blackout|prolonged loss of power|
|fault|short loss of power|
|brownout|prolonged low voltage|
|sag|temp low voltage|
|surge|prolonged high voltage|
|spike|temp high voltage|

**clean power** --> UPS in order to prevent damage

**too much humidity** --> CORROSION

**too little humidity** --> STATIC ELECTRICITY

# FIRE SUPPRESSION

|class (mnemonic)|type|extinguished with|
|-|-|-|
|**A** (ash)|wood, paper|water, soda acid|
|**B** (boil)|burning alchool, oil, gasoline|CO2, soda acid, halon|
|**C** (conductive)|electrical|CO2, halon|
|**D** (Dilythium)|burning metals|dry powder|
|**K** (Kitchen)|kitchen fire, oil, grease|wet chemicals|

**fire detection**
- smoke sensing
- flame sensing
- heat sensing

**electromagnetic interference**
- common mode noise --> diff in power btw hot/ground wires
- traverse mode noise --> diff in power btw hot/neutral wires

**RFI - Radio Frequency Interference** --> generated by electrical appliances, light sources, cables, etc.

**water suppression systems**
- preaction   --> closed sprinkler heads, pipe charged w/ air
- wet pipes   --> filled w/ water
- dry pipes   --> filled w/ air
- deluge      --> dry pipes w/ larger open sprinkler heads

```sh
water and electricity do not mix !!!
```

**gas discharge suppression systems**
- halon not anymore --> FM-200, argon, argonite, inergen


**mantrap** --> only one person in

**masquerading** --> Pretend to be someone else

**piggybacking** --> follow someone through a secure gate w/o being id/auth personally

**sensors for glass**
- shock --> built in the window
- glass-break --> mic that listens for sounds

air quality - no dust + **_positive pressurization_** (DC room has a bigger pressure, when door is opened the air should flow OUT, not IN)


{% include links.html %}
