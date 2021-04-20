---
title: "Domain 3: Security Architecture and Engineering"
tags: [domain_3]
##keywords: release notes, announcements, what's new, new features
last_updated: Aug 30, 2020
summary: "Cryptography"
sidebar: mydoc_sidebar
permalink: 3_crypto.html
folder: mydoc
---

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
salt/seed - used w/ passwords - additional random data to a one-way hashing function; against rainbow tables
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
|**_cryptanalysis_**|study of methods to defeat codes and ciphers|
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
**CIPHER**: always meant to hide msg's true meaning

```
**running key ciphers aka "book ciphers" ** --> the encryption key is as long as the message itself and is often chosen from a common book

**CONFUSION** --> relationship between the plaintext and the key is so complicated that an attacker can’t merely continue altering the plaintext and analyzing the resulting ciphertext to determine the key

**DIFFUSION** --> a change in the plaintext results in multiple changes spread throughout the ciphertext

```

**Distribution of symmetric keys**
- OFFLINE --> physical exchange
- PUBLIC KEY ENCR. --> public key to setup a secure channel, over which the secret key is exchanged
- DIFFIE-HELLMAN KEY EXCH ALG

**zero-knowledge proof** --> prove knowledge of a fact w/o revealing the fact itself

**split knowledge** --> no single person has sufficient privileges to compromise the security

**work function (factor)** --> measure the strength of a crypto system by measuring the effort in terms of cost/time to decrypt

**key clustering** --> weakness where a plaintext generates identical ciphertext using the same alg w/ different keys

# DES (3DES) modes

||||
|-|-|-|
|ECB|Electronic Codebook|**block**; simplest, least secure; enc w/ chosen key, same block will produce same ciphertext|
|CBC|Cipher Block Chaining|**block**; unenc text XOR w/ preceding ciphertext block; propagates errors|
|CFB|Cipher Feedback|**stream**; same as CBC, propagates errors|
|OFB|Output Feedback|**stream**; plain text XOR seed; no chaining, no propagation of errors|
|CTR|Counter|**stream**; inc counter instead seed; no error propagation|

# DSS - Digital Signature Standard

- rely on public key crypto + hashing functions
- uses SHA-1/2/3 message digest functions
- uses one of 3 encryption alg:
  - DSA
  - RSA
  - ECDSA

**meet-in-the-middle attack** --> exploits protos that use two rounds of encryption

**man-in-the-middle attack** --> both parties comm w/ attacker instead w/ each other

**birthday attack** --> attempt to find collisions in hash functions

**replay attack** --> reuse auth requests

# symmetric algorithms

|Name|type|block size|key size|strength|
|-|-|-|-|-|
|AES|block|128|128-256|strong|
|Blowfish||64|32-448||
|DES|Block|64|56|very weak/obsolete|
|3DES|block|64|112/168|moderate|
|IDEA||64|128||
|RC5||32, 64,128|0-2040|very strong|
|Skipjack||64|80||
|Twofish||128|1-256||

# asymmetric algorithms

|name|type|size|strength|
|-|-|-|-|
|RSA|key transport|512|strong|
|Diffie-Hellman|key exchange||moderate|
|El Gamal|key exchange||very strong|
|ECC|elliptic curve|variable w/ smaller key|very strong|

# hash algorithms

|Name|hash value length|
|-|-|
|HMAC|variable|
|HAVAL|128-256|
|SHA-224|224|
|SHA-256|256|
|SHA-384|384|
|SHA-512|512|
|MD5|128|

# 3 major public key cryptosystems

- RSA             --> factoring product of prime numbers
- El Gamal        --> extension of Diffie-Hellman
- Elliptic Curve  --> discrete logarithm



# salt'n'pepa

**SALT**
- unique, NON-SECRET value appended to pwd before hashing
- stored in the db
- UNIQUE FOR EACH USER

**PEPPER**
- SECRET value appended to pwd before hashing
- SAME FOR ALL USERS
- NOT stored in the db, but in cfg file/hardcoded 

**QUANTUM COMPUTING**
- no additional advantage over classical in terms of computability
- enable design of novel algorithms 
- **_Shor's alg endangers most PKI algorithms_**

{% include links.html %}
