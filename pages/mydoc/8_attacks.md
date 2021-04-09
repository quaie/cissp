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

# XSS - cross-site scripting
- users's browser is tricked to download a (malicious) script from a site and execute it on another site
- if already logged in on the second site, the script wreaks havoc :)
- requirements:
  - reflected input (input provided by the user is later displayed to other users)
  - unvalidated input (the input above is not validated)

how it works:
- attacker updates user-provided content on website_1, including <SCRIPT> and JavaScript code accessing website_2
- victim visits website_1, browser downloads the code and the script is accessed on website_2

**SOLUTION = VALIDATE ALL USER INPUT**

# SQL injection
- attacks the backend database
- alter SQL queries by appending other commands (in the text boxes)

**defend against SQL injection**
- input validation --> check input on SERVER SIDE
- parametrized queries --> precompile SQL code on the db server to prevent user input

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

{% include links.html %}
