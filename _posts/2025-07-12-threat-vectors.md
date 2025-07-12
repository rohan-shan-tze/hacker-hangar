---
layout: single
title: Threat Vectors
date: 2025-07-12
author_profile: true
read_time: true
tags:
  - Security+
  - fundamentals
  - threat
  - vector
  - hacker
image: /assets/images/distorted-bust.png
excerpt: Examining the methods malicious actors often use to attack systems
---
{% include figure
  image_path="/assets/images/distorted-bust.png"
  alt="Image of a bust (sculpture of a head with shoulders) distorted behind a glass pane"
%}

### What Is a Threat Vector

**A method used by an attacker.** In this post we explore some common threat vectors, and the **attack surfaces** they exploit, used to break into systems.

---

#### Message-Based

One of the most common threat vectors.

- Links to malicious sites in email (classic **phishing**)

- SMS phishing (**smishing**) is also very common

- Scams that rely on fake stories

---
#### Image-Based

Malicious code can be embedded in image files.

- Example: SVG files, because SVG is XML, threat actors can **embed** code in the markup.

---
#### File-Based

- Zip archives often hide malicious files inside.

---
#### Voice Call

- **Vishing** (voice phishing), is common and can be automated.

- **War-dialing:** calling many numbers hoping to hit an exposed modem or system.

- Disrupting voice calls (denial-of-service).

---
#### Removable Device

- e.g. USB drives, effective against air-gapped or heavily firewalled networks.

---
#### Vulnerable Software

- **Client-based:** infected executables; known or unknown vulnerabilities. Patch consistently for safety.

- **Agentless:** a compromised server spreads malware to every connecting user.

---

### Unsupported Systems and Applications

When a product stops receiving patches, it becomes a soft target.  
Know which parts of your stack are unsupported and treat them as higher-risk.

---

### Unsecure Networks

- **Wireless:** Use current protocols like WPA3, avoid outdated ones like WEP, WPA, WPA2.

- **Wired:** Enable 802.1X to block unauthorised access.

- **Bluetooth:** Attackers can scan for and exploit vulnerable Bluetooth devices.

---

### Open Service Ports

Every open port is a potential entry point, especially if misconfigured.  
Firewalls help reduce the attack surface.

---

### Default Credentials

Leaving the factory username/password in place makes you an easy target.

---

### Supply Chain

Attackers may compromise a partner first, then pivot to you.

- **Managed Service Providers (MSPs)**

- **Vendors/Contractors**

- **Suppliers:** e.g., counterfeit hardware

---

### References

1. Point Normal, Image of a bust (sculpture of a head with shoulders) distorted behind a glass pane [Unsplash](https://unsplash.com/photos/a-bust-appears-distorted-behind-a-glass-pane-Ij0b3QZaBB0)
