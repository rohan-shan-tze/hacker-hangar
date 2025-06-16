---
layout: post
title: The CIA and the Forms of Security Control
date: 2025-06-16
author_profile: true
read_time: true
tags:
  - Security+
  - fundamentals
  - CIA
excerpt: An introduction for beginners to the forms of security controls and the CIA triad; complete with real world examples.
---

In this post, I’ll break down the forms of control according to CompTIA as well as the ubiquitous CIA triad.

___

### Security Controls

Security controls work to stop, mitigate, or recover from security breaches.

There are four main **categories** of security controls: Technical, Managerial, Operational, and Physical.

Technical controls involve technical systems. Encryption and firewalls are examples of technical controls

Managerial controls are administrative in nature. Examples include standard operating procedures and guidelines.

Operational controls use people to implement security. An every-day-life example is a security guard, and a more out-of-the-box example is a penetration tester.

Physical controls exist in the physical space. Examples include a locked door, or a lift that can only go to certain floors with an electronic pass.

Those were the categories of controls, now let's look at the **types** of control.

We have preventive, deterrent, detective, corrective, compensating, and directive

Preventative involves preventing the security breach. For example via a password.

Deterrent involves deterring the attack. This can bed done using warnings and threats.

Detective involves detecting the breach. For example by having someone checking the system logs regularly.

Corrective involves "fixing" the breach. For example if the system's data is destroyed in an attack, recovering the data from a cold copy is a corrective measure

Compensating controls are the miscellaneous controls if the others aren't sufficient. They may be temporary. For example if it has been detected that the API that one part of the website uses has been compromised, cutting of access to that section of the website while the API is fixed is a compensating control.

There are also directive controls, which are a weak measure that just "nudges" potential attackers away. For example instead of having a locked door, having a sign that says do not enter would be a directive measure.

How all of this comes together is that a particular example of a control measure will be in an least one control category and be at least one control type.

For example a firewall is a technical preventative control.

A guideline is a managerial directive measure, but may also be a managerial preventative measure if workers following the guidelines would prevent an attacker from breaching the system.

___

### CIA Triad

The CIA triad is a set of three core principles for security to follow when designing a system.

It may also be known as the AIC triad to differentiate it from the other very famous CIA.

C - Confidentiality, a system should not expose its data to an outside party

I - Integrity, ensuring the data in the system has not been tampered with or modified by an outside party; non-repudiation 

A - Ensuring the system is always accessible and usable by the parties that should have these privileges  

___

### Non-repudiation

Non-repudiation ensures that communication is by the intended parties and that the content of the communication has not been altered by an outside party. This mirrors integrity in the CIA.

One implementation of non-repudiation is verification using a digital signature, outlined below.

Sender has a private and public key pair. The private key is known only to the sender, but the public key can be known by anyone. This public-private key method of encryption is ubiquitous and involves a smart mathematical trick that we will not get into now.

Sender uses known hashing algorithm to produce a hash from the message, then uses private key to encrypt the hash. This is the digital signature. 

Then sender sends the plain-text message and the digital signature to the recipient.

Recipient decrypts the signature using the sender's public key. This produces the hash.

We then apply the same hashing algorithm as the sender used, to the plain-text message to again produce the hash.

If the two hashes the recipient generated are equal to one another, then we know we have the uncompromised message from the intended sender.