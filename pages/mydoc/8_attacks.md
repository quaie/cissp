---
title: Software security attacks
tags: [domain_8]
##keywords: release notes, announcements, what's new, new features
last_updated: Mar 29, 2021
summary: "Notes for  Domain 8"
sidebar: mydoc_sidebar
permalink: 8_attacks.html
folder: mydoc
---

**APT - advanced persistent threat** --> sophisticated adversaries w/ advanced tech skills and significant financial resources

**zero-day vuln** --> sec flaws discovered by hackers, w/o patch

**window of vulnerability** --> delay btw vuln discovery and patch release

# password attacks
- _**guessing attack**_ --> 
- _**dictionary attack**_ --> lists of words
    - **_RAINBOW TABLES**_ --> precomputed hash tables; defence = SALT the passwords
- _**social engineering attack**_ --> trick the (l)user
    - _**phishing**_
    - _**spear phishing**_ --> target = an individual/group 
    - _**whaling**_ --> spear phishing CEO/CFO/etc
    - _**vishing**_ --> via voice
    - _**dumpster diving**_ --> search the trash

# XSS - cross-site scripting
- **exploit the trust that a user has in a website to execute code on the user’s computer**
- users's browser is tricked to run a (malicious) script from a site and execute it on another site
- requirements:
  - reflected input (input provided by the user is displayed - generated page/pop-up)
  - unvalidated input (the input above is not validated)

**SOLUTION = VALIDATE ALL USER INPUT**

# CSRF (XSRF) - cross-site request forgery
- **exploit the trust that remote sites have in a user’s system to execute commands on the user’s behalf**
- assume the user is logged into several sites
- embed code in one website that sends commands to a second website --> works only if already logged it


# XSS - cross-site scripting
- users's browser is tricked to download a (malicious) script from a site and execute it on another site
- if already logged in on the second site, the script wreaks havoc :)
- requirements:
  - reflected input (input provided by the user is later displayed to other users)
  - unvalidated input (the input above is not validated)


how it works:
- attacker updates user-provided content on website_1, including <SCRIPT> and JavaScript code accessing website_2
- victim visits website_1, browser downloads the code and the script is accessed on website_2

**SOLUTIONS**
- use secure tokens
- check referring URL - it should be originating from same site

# TOC/TOU - time of check to time of use
- timing vulnerability that occurs when a program checks access permissions too far in advance of a resource request

**back door** --> undocumented command sequences that allow individuals with knowledge of the back door to bypass normal access restrictions

**escalation-of-privilege attacks** --> once on a system, attackers expand access to admin user
- _**ROOTKIT**_ --> exploit known vulnerabilities in various OS

**SOLUTION = VALIDATE ALL USER INPUT**


# SQL injection
- attacks the backend database
- alter SQL queries by appending other commands (in the text boxes)


```sh
Databases will process multiple SQL statements at the same time, provided that you end each one with a semicolon
```

**defend against SQL injection**
- input validation --> check input on SERVER SIDE
- prepared statements --> parameterized queries & stored procedures - precompile SQL code on the db server to prevent user input (only args accepted, structure = unaltered)
- limit account privileges


# privilege escalation
- gains admin access on the underlying OS
- often use buffer overflow

**mitigation**
- perform input validation on all input received from user
- patch OS, platforms and apps
- enforce least privilege  (any serv account servicing the app should have the minimum privs)
- DEP - Data Execution Prevention
- ASLR - Address Space Layout Randomization

# Directory traversal
- allows the attacker to manipulate the file system structure on a webserver
- tries to exit the current directory by using . and .. and find unsecured files

**defence**
- input validation
- strict FS controls to limit webserver user's access

# buffer overflow
- input from user bigger than the memory buffer allocated by the app --> instability, crash, etc.

**mitigation** --> INPUT VALIDATION

# cookies
- stored on the local disk - data from websites to recognise users or to retain some information for the website
- track users
- can be used across several sites
- browser can be cfg to handle them

# session hijacking
- guess or eavesdrop

# malicious browser add-ons
- aka extensins, add new functionality to browsers/other software
- written by 3rd party devs
- **risks** --> can have trojans, can have relaxed permissions

# code execution attacks
- attacker exploits a vulnerability in a system that allows the attacker to run commands on that system (OS cmds)
  - _**arbitrary code execution**_ --> where the attacker runs his commands
  - _**remote code execution**_ --> over network
- can do what he wants with the system

**mitigation**
- limit administrative access for the user running the app
- patch OS and apps


# RECONNAISSANCE ATTACKS
- _**IP probes**_ --> ping address, see if online
- _**port scan**_ --> probe ports, see apps running
- _**vuln scan**_ --> look for vulns of a specific server/service

# MASQUERADING ATTACKS
- _**IP spoofing**_ --> impersonate a trusted IP address --> **FIREWALL: NO RFC 1918 INBOUND**
- _**session hijacking**_ --> intercept comm btw auth. user - resource & takes over (cookie, mitm, capture details)

{% include links.html %}
