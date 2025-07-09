---
layout: single
title: Hiding Data in Plain Sight: Blockchain and More
date: 2025-07-09
author_profile: true
read_time: true
tags:
  - Security+
  - fundamentals
  - blockchain
  - obfuscation
  - hashing
  - salting
image: /assets/images/lock-on-keyboard.png
excerpt: Examining blockchain, obfuscation, and hashing
---

{% include figure
  image_path="/assets/images/raccoon-hiding-in-tree.png"
  alt="Picture of raccoon hiding"
%}

Encrypting everything costs precious CPU cycles. How else can we keep secrets, or at least hide them in plain sight?

---
### Obfuscation

Making information *difficult* to interpret

Different from encryption since encryption makes information practically impossible to interpret (without the relevant key)

Obfuscation is useful to hide important information. For example hiding back-end functionality of an application may make the code harder to reverse engineer and attack.

However it can also be used maliciously. Malicious actors can embed instructions in a JPEG file through steganography

---
#### Types of Obfuscation 

**Steganography**

Hiding data inside other data. For example embedding a hidden message in an audio file that can only be understood when played backwards. Typically the audio file would seem normal when played normally.

**Tokenisation**

Swap a sensitive value for a meaningless one using a token vault. For example during a credit card payment, the customer's credit card number would be substituted by a token from the third-party token vault service. The token is then sent to merchant who then checks the token with the token vault and will find that it maps back onto the user.

**Data Masking**

Overwriting sensitive fields while keeping the data somewhat realistic.

For example replacing a 16-digit credit card number with \*\*\*\*\*\*\*\*\*\*\*\*1234 on a transaction receipt.

---
#### Hashing

In the context of cryptography, a hash is a deterministic, one-way function that is collision-resistant. 

Let us examine some of the terminology:

- Deterministic: Same input means same hash. Important for integrity checks.

- One-way: Computationally hard (infeasible) to reverse. Important for security

- Collision-resistant: Hard to find two inputs with same hash. 

Notable hashing algorithms:

- SHA-2 family: The current convention
- SHA-3: Less used but has been tested
- SHA-1: Deprecated as they were found to be susceptible to collisions

Now, whenever cybersecurity professionals design a secure system, people will of course try and break said system. 

One method of attacking hashes is through rainbow tables. Imagine an attacker obtains a user's hashed password and knows the hashing algorithm. The attacker can use a rainbow table, a precomputed table of hash outputs revealing their original input. Now a simple lookup can result in the attacker obtaining the plain-text password

How do we counteract rainbow tables? We can use *salting*

Salting is random data prepended or appended to the input value before hashing. 

This makes it so that attackers cannot use rainbow tables to decipher the hash unless they also know the exact salt used.

----
### Blockchain

Traditional ledgers (records of transactions) have an integrity problem: they are stored on a single server and therefore whoever has control over that server can rewrite transactions.

Blockchain is a decentralised, distributed ledger.

In other words, everyone on the blockchain can maintain the ledger.

All transactions on the ledger are accessible to everyone

To add a transaction to the blockchain, the transaction is first added to a "block" of other transactions.

Each block has its own hash and also stores the hash of the previous block. If any transaction is tampered with, the hash will become invalid and the block will be discarded.

---
### References

1. Thomas Bormans, picture of raccoon [Unsplash](https://unsplash.com/photos/a-raccoon-peeks-out-of-a-hole-in-a-tree-stump-y5XNvg3utOI)






