---
title: Domain 3: Security Architecture and Engineering
tags: [domain_3]
##keywords: release notes, announcements, what's new, new features
last_updated: Aug 30, 2020
summary: "Notes for  Domain 3"
sidebar: mydoc_sidebar
permalink: 3_notes.html
folder: mydoc
---

------------------------------------------------------------------
**_Certification Exam Outline_**

`3.1 Implement and manage engineering processes using secure design principles`

`3.2 Understand the fundamental concepts of security models`

`3.3 Select controls based upon systems security requirements`

`3.4 Understand security capabilities of information systems (e.g., memory protection, Trusted
Platform Module (TPM), encryption/decryption)`

`3.5 Assess and mitigate the vulnerabilities of security architectures, designs, and solution
elements`
- Client-based systems
- Server-based systems
- Database systems
- Cryptographic systems
- Industrial Control Systems (ICS)
- Cloud-based systems
- Distributed systems
- Internet of Things (IoT)

`3.6 Assess and mitigate vulnerabilities in web-based systems`

`3.7 Assess and mitigate vulnerabilities in mobile systems`

`3.8 Assess and mitigate vulnerabilities in embedded devices`

`3.9 Apply cryptography`
- Cryptographic life cycle (e.g., key management, algorithm selection)
- Cryptographic methods (e.g., symmetric, asymmetric, elliptic curves)
- Public Key Infrastructure (PKI)
- Key management practices
- Digital signatures
- Non-repudiation
- Integrity (e.g., hashing)
- Understand methods of cryptanalytic attacks
- Digital Rights Management (DRM)

`3.10 Apply security principles to site and facility design`

`3.11 Implement site and facility security controls`
- Wiring closets/intermediate distribution facilities
- Server rooms/data centers
- Media storage facilities
- Evidence storage
- Restricted and work area security
- Utilities and Heating, Ventilation, and Air Conditioning (HVAC)
- Environmental issues
- Fire prevention, detection, and suppression
------------------------------------------------------------------


# Cryptography

**COMPRESSION** --> reduces redundancy before plaintext is encrypted, increases crypto strength \
**DECOMPRESSION FUNCTIONS** --> run on the text before it enters the encryption algorithm

**Security services provided by cryptography**
- PRIVACY --> unauth disclosure
- AUTHENTICITY --> verifies the claimed identity
- INTEGRITY --> detects modif
- NON-REPUDIATION --> combines Authenticity + Integrity; cannot deny sending/content of msg


**plain text + initialization vector + algorithm (cipher) + key = cipher text**
```
Initialization vector - IV - adds randomness to the process
IV - confidentiality of data
salt/seed - used w/ passwords
```

all crypto algs rely on **keys**: nothing more than a (big) number. \
**key space**: range of values that are valid for use as a key \
** bit size of key space**:  number of binary bits (0s and 1s) in the key

```
KERCKHOFFS'S PRINCIPLE --> crypto system should be secure even if everything about it, except the key, is public knowledge.
```

|term|meaning|
|-|-|
|**_cryptography_**|creating and implementing secret codes and ciphers|
|**_cryptanalysi_s**|study of methods to defeat codes and ciphers|
|**_cryptology_**|cryptography and cryptanalysis|
|**_cryptosystems_**|Specific implementations of a code or cipher in hardware and software|

**Logical operations**
|op|sign|result|
|-|-|-|
|AND|∧| 1∧1=1; rest is 0|
|OR|∨| 1 everytime there is a 1|
|NOT|~ or !| |
|EXCLUSIVE OR|XOR ⊕|returns a true value when only one of the input values is true|
|MODULO|mod %| the remainder value left over after a division operation|

**one-way function** --> mathematical operation that produces output values for each possible combination of inputs but makes it impossible to retrieve the input values \
**NONCE** --> random number acting as a placeholder variable in mathematical functions. When the function is executed, the nonce is replaced with a random number generated at the moment of processing for one-time use. The nonce must be a unique number each time it is used.

**CODE**: crypto systems of symbols representing words/phrases, sometimes secret, not meant to provide confidentiality
vs \
**CYPHER**: always meant to hide msg's true meaning

```
**running key ciphers aka "book ciphers" ** --> the encryption key is as long as the message itself and is often chosen from a common book

**CONFUSION** --> relationship between the plaintext and the key is so complicated that an attacker can’t merely continue altering the plaintext and analyzing the resulting ciphertext to determine the key

**DIFFUSION** --> a change in the plaintext results in multiple changes spread throughout the ciphertext

```

**Distribution of symmetric keys**
- OFFLINE --> physical exchange
- PUBLIC KEY ENCR. --> public key to setup a secure channel, over which the secret key is exchanged
- DIFFIE-HELLMAN KEY EXCH ALG



{% include links.html %}
