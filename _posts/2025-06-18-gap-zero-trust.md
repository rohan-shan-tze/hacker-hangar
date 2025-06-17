---
layout: single
title: Analysing GAPS and Trusting Zero
date: 2025-06-18
author_profile: true
read_time: true
tags:
  - Security+
  - fundamentals
  - GAP
  - Zero Trust
excerpt: A brief introduction to GAP analysis and an outline of the zero trust framework with a real-world example.
---
This post briefly introduces GAP analysis and outlines the zero trust framework with a real-world example.

---

### GAP Analysis

An analysis comparing where the organisation is at with where it wants to be.

For example, how the organisation's security system compares with a chosen security framework or industry standard (though the standard can be self-defined as well).

The analysis typically consists of three stages:

1. Picking the standard to evaluate with
2. Performing the comparison
3. Writing the report, stating how each component of the system compares with the standard

---

### Data and Control Planes

We can often separate networks into a data plane and a control plane.

We consider the data plane to be the plane where user data is transmitted and received.

The control plane makes decisions for the network.

---
### Zero Trust

A natural tendency for designing networks is to have strong security checks at entry points, but weak checks internally.

This network would allow authorised individuals to move easily while inside the network, but it would also allow unauthorised individuals who breached the security layer to move around with the same freedom, being able to access critical resources.

The zero trust framework proposes that we continue having security layers even within the network itself. Every access request is checked rather than automatically trusted.

Let's examine the data and control planes of a zero trust network.

**Data Plane:**

- **Subject/System** — The entity trying to move around the network. The subject may be the user and the system may be the machine used by the user.
- **Implicit-Trust Zones** — If the subject/system is in the zone then automatically trust it. For example, if the machine is in the company office then trust it. (Non-zero trust systems may also employ these zones)
- **Policy Enforcement Point (PEP)** — We have a policy to trust or not trust certain subjects/systems. This is where requests are accepted or rejected based on the policy

**Control Plane:**

- **Adaptive Identity** — Dynamically adjust trust of the subject/system based on factors like location, resources requested, time of day, etc. Lower trust may lead to stricter authentication.
- **Threat Scope Reduction** — Reduce possible damage by restricting entry points as well as accessible resources 
- **Policy-Driven Access Control** — Use policies to determine if a subject/system is to be trusted.
- **Policy Administrator** — Passes information to and from the PEP and Policy Engine. Also generates access tokens.
- **Policy Engine** — Evaluates the subject/system based on the policy. Together with the Policy Administrator, it forms the Policy Decision Point (PDP)

**Real world example:**

- Subject/system requests resource
- PEP (data plane) receives a request and digital certificate from a user
- PEP sends data to PDP (control plane)
- Policy Engine examines the certificate and makes a decision to allow the user to access the resource or not
- If decision was "yes", the Policy Administrator generates an access token and sends this back to PEP
- PEP sends the resource from the resource server to the requesting subject/system
- If decision was "no" the policy administrator passes this to the PEP
- PEP blocks the user

Zero trust reinforces the idea that trust must be continuously earned and checked, rather than assumed — even within a network.
