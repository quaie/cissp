---
title: Domain 4 Notes
tags: [domain_4]
##keywords: release notes, announcements, what's new, new features
last_updated: Mar 23, 2021
summary: "Notes for  Domain 4"
sidebar: mydoc_sidebar
permalink: 4_notes.html
folder: mydoc
---

**VPN screen scraper** = app that allows an attacker to capture what is on the user's display (abernathy?)

**Screen scraping** is the act of copying information that shows on a digital display so it can be used for another purpose.

**SDN** (Software Defined Network) --> physical separation of network control plane from fwd plane (decisions are taken remote, not on the hardware)

**VSAN** (Virtual Storage Area Network) --> sw-defined storage that allows pooling of storage capabilities & instant/automatic provisioning of VM storage.

**Noise** --> interference introduced to the cables, distorts the signal --> problems

**Attenuation** --> weakening of the signal as it travels down the cable

**Crosstalk** --> wires in parallel --> signals interfere w/ each other & distort the signal

**Eavesdropping** --> fiber optic is the safest !

# Network attacks

**non-blind spoofing** --> attacker in the same subnet, sniffs the seq/ack numbers and hijacks the session

**blind spoofing** --> pkts sent to victim to obtain a sampling of seq numbers & generate a valid seq number for the attack (works on older systems)

**MITM** --> intercepts legitimate traffic between 2, attacker controls info flow & can alter comm

# Remote access
- Caller ID --> dial in & auth, server checks if incoming number is correct
- callback --> dial in & auth, server hangs up and calls back to a predefined number

**MAC flooding** --> overflow the MAC table w/ many entries, transforming the device into a hub-like device

**ARP poisoning** --> within VLAN, fools routers into learning false MAC addr; then pose as that device and do MITM

# ICMP attacks

**Ping of Death** --> send oversized packets, victim's OS becomes unstable

**Smurf** --> ICMP echo request --> sent to the broadcast on victim's behalf (faked) --> all devices in the network answer --> DDoS

**Fraggle** --> uses UDP, echo & chargen packets, DDoS like smurf

**ICMP redirect** --> alter the routing table of the host that receives the message using ICMP redirect packets (type 5, used to specify better routing paths)

**ping scanning** --> pings every IP address to see if it's alive

**LAND - LAN Denial** --> DoS, malformed IP src/dst/port = same

**Teardrop** --> DoS, several large overlapping IP fragments sent --> reassembly = crash

# DNS attacks

**DNS cache poisoning** --> attacker attempts to refresh/update the record when it expires w/ a fake address (on the DNS server's cache)

**pharming** --> redirect a website's traffic to a fake site (by changing the hosts file on a victim's computer or by exploitation of a vulnerability in DNS server software)

**DoS** --> attack the DNS server

**DDoS** --> DoS from several devices

**DNSSEC** --> stronger auth mechanism, digital signatures to validate the source of DNS messages

**URL hiding** --> embed URL in web pages/email (text ok, hyperlink fake)

**domain grabbing** --> idividuals register a domain name of a well-known company before the company does it

**cybersquatting** --> domains registered to hold them hostage (sell them to the "right owner")

# Email attacks

**email spoofing** --> fake the headers to look like it comes from somebody else

**phishing** --> convince the stupid user to click a link in a unsolicited email (social eng)

**spear phishing** --> phishing targeted to specific persons

**whaling** --> important person in the company 

**spam** --> mass email


**teardrop** --> fragmentation attack, malformed fragments of the packet are sent, @reassembly the victim crashes

**session hijacking** --> attacker places himself in the middle of an active conversation

**IP addr spoofing** --> impersonate another IP addr

**zero day** --> previously unknwon sec vuln

# Bluetooth

operates in 2.4 GHz, uses FHSS and AFH (Adaptive Freq Hopping) - switches congested channels, low power

**uses a weak encryption cipher, E0; has 128-bit key, is vulnerable**
- buffer overflow
- bluejacking (unsolicited msg are sent)
- BlueBug attacks (can overtake phone, send SMS, download/modify data)


|||
|-|-|
|bluejacking|send unsolicited msg over Bluetooth|
|Red Fang|find non-discoverable Bluetooth devices|
|bluesnarfing|theft of data via Bluetooth|

|layer|proto|
|-|-|
|7 - application|HTTP, FTP, TFTP, DHCP, DNS, SMTP, POP3. telnet, SSH|
|6 - presentation|GIF, JPEG, MPEG|
|5 - session|PAP, RPC|
|4 - transport|UDP, TCP|
|3 - network|IP, RIP, OSPF|
|2 - data link|ethernet, frame relay, token ring, PPP, CDP|
|1 - physical||


# Firewalls

|type|descr|
|-|-|
|static pkt filtering |(aka screening routers) examines msg headers - src/dst/port; **LAYER 3**|
|app-level gateway|(aka proxy) copies pkt from netw to another; change src/dst addr; based on content **LAYER 7**|
|circuit-level gateway|establish comm sessions btw trusted partners; based on circuit, not content; **LAYER 5**|
|stateful inspection|(aka dynamic) evaluate state/context of connection; **LAYER 3+4**|
|deep pkt inspection (DPI)|filter the payload, can block domains, malware, spam from payload; **LAYER 7**|
|NG firewalls|MFD - multifunction device: IDS, IPS, NAT, VPN, antivir, etc|


# TRICKS

HTTPS encrypts @ layer 4, using SSL/TLS; the entire HTTPS message; S-HTTP - never widely used, encrypts only data @ layer 7
{% include links.html %}
