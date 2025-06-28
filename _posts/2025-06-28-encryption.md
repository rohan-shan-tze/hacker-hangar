---
layout: single
title: Encryption, an Introduction
date: 2025-06-28
author_profile: true
read_time: true
tags:
  - Security+
  - fundamentals
  - encryption
image: /assets/images/lock-on-keyboard.png
excerpt: An overview of cryptography for beginners.
---

{% include figure
  image_path="/assets/images/lock-on-keyboard.png"
  alt="Picture of encryption"
%}

In today's world of big data, data analysis and data transmission, how do we ensure that data is secure? The answer is encryption

### Good Ol' Fashioned Passwords Have a Problem

Imagine you were trying to log into your Netflix account and you entered your password and it was sent to the Netflix server without encryption. Any malicious actor who intercepted the transmission would be able to see your password in plain text.

The solution is to use (asymmetric) encryption to encrypt your data so that even if a malicious actor gets every single piece of information that you send to Netflix, they will not be able to read your password or anything else.

### What is a Key?

A key is a piece of information that allows the encryption or decryption of data when used with an encryption algorithm.

A ***private key*** is a secret key typically only accessible to the entity that generated the key.

A ***public key*** would be a key that is available for anyone to see.

Sometimes it is convenient to store keys in one place. Such an arrangement is known as a ***key escrow***. One situation where this is common is in corporations, since it is a necessity to be able to access employee keys to access their company-related data once they leave the corporation. 

### Symmetric vs Asymmetric Encryption

Symmetric encryption methods involve using the same key for encryption and decryption. This would work well when only one entity needs to access the data. For example local storage of data (The encryption still protects against unauthorised remote access). 

However, symmetric encryption has a similar problem to passwords in that for communication of data to another entity, the key has to be shared to that entity first, but in the middle of transmission the key may be intercepted. Allowing malicious actors to decrypt any future encrypted communication.

Asymmetric encryption is the solution to this. Using clever mathematics, it is possible to send messages by encrypting them with the recipient's public key, and only the private key (which only the recipient would have) can be used for decryption. 

Such a process relies on the recipient generating the private-public key-pair in a way such that the keys are mathematically related.

### Encryption Tools and Hardware

Specialised tools and hardware enable efficient cryptographic processes. Here are some examples.

- Trusted Platform Module: A common specialised chip in computer motherboards that perform cryptographic operations efficiently
- Hardware Security Module (HSM): A device that manages multiple keys as well as performing cryptographic operations efficiently. Has larger-scale use cases than TPM. For example, an HSM is used to manage a company's keys. Companies often have multiple HSMs to ensure reliability in case of individual unit failure
- Key Management System: A framework for managing cryptographic keys. Often using a centralised manager.
- Secure Enclave: Similar to a TPM, but is typically found in Apple machines and has different use cases. Secure Enclaves are great for secure code execution and data privacy, protecting data even from the operating system itself.

### References

1. Towfiqu barbuiya, picture of lock on keyboard, [Unsplash](https://unsplash.com/photos/a-golden-padlock-sitting-on-top-of-a-keyboard-FnA5pAzqhMM)







