---
layout: single
title: "Certificates: How We Trust Strangers"
date: 2025-07-10
author_profile: true
read_time: true
tags:
  - Security+
  - fundamentals
  - certificates
image: /assets/images/certificate.png
excerpt: Examining certificates in cybersecurity
---

{% include figure
  image_path="/assets/images/certificate.png"
  alt="Person signing a certificate"
%}

In a world where we are forced to interact with strangers behind computer screens, how do we know we are not talking to an imposter? Certificates are the first-layer of proof.

---
### What is a Certificate and Who Issues Them?

A certificate is something that binds a public key to an identity letting people know that the entity is really who they say they are. Your browser would typically warn or block you from accessing websites without trusted certificates.

Generally trusted certificate authorities (CAs) are responsible for validating (signing) certificates. 

We can think of CAs being the **root of trust** where the **chain of trust** originates from. As the CA is trusted, and entities that are trusted by the CA are also trusted.

An entity (e.g. a website) would submit a certificate signing request (CSR) to the CA together with some identifying information, then the CA will conduct its validation process and sign the certificate if it passes. 

Our browsers maintain a list of CAs that it trusts by default, so if a website has a certificate from a CA on the list, the website will be trusted.

Generally certificates follow the X.509 standard.

---
### Private Certificate Authorities

Some organisations wish to make their own (private) certificate authorities.

Reasons for this include:

- Issuing certificates for internal hostnames, e.g.  \*.corp.local, that public CAs are forbidden to sign 
- Tighter security
- Complete control over trust.

These CAs can be built using tools like Windows Certificate Services.

---
### Wildcard Certificates

Extending X.509 certificates, we can allow subdomains to also be included efficiently by using Subject Alternative Names (SANs)

e.g. \*.example.com

Would allow any string not including "." followed by .example.com to be trusted.

e.g. hello.example.com would be trusted

Note that hello.world.example.com would be not trusted due to "hello.world" as that subdomain would have too many levels.

---
### Key Revocation

Sometimes a website that used to be trusted becomes compromised. We now need to revoke the trust we once placed on that website.

**Methods:**

- Certificate Revocation List (CRL): CA maintains a list of all revoked certificates, browser retrieves this list at regular intervals. A certificate that is on the CRL is not trusted.
- OCSP: Browser queries OCSP responder for a certificate's status. If the OCSP response is "revoked" the certificate is not trusted. Downside is that this query takes time. 
- OCSP Stapling: Server staples a time-stamped OCSP response so that the OCSP status is ready without added latency during TLS handshake 
- Short-lived Certificates: Discard certificates and renew every ≤10 days, allowing browsers to skip CRLs and OCSP.

---
### Final Thoughts

Certificates are a clever way to build trust over the internet, a necessity in modern times. 

---
### References

1. Milos Lopusina, picture of woman signing a certificate [Unsplash](https://unsplash.com/photos/a-woman-writing-on-a-piece-of-paper-Oe8Q-mzNUT4)






