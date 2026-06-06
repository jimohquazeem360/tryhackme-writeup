# TryHackMe Write-Up: CIA Triad

![TryHackMe](https://img.shields.io/badge/Platform-TryHackMe-red?style=flat-square&logo=tryhackme)
![Category](https://img.shields.io/badge/Category-Fundamentals-blue?style=flat-square)
![Difficulty](https://img.shields.io/badge/Difficulty-Easy-brightgreen?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completed-success?style=flat-square)

---
<img width="1920" height="1080" alt="Screenshot (1)" src="https://github.com/user-attachments/assets/f1452681-4b8d-4e11-8abb-7df364456571" />


## Overview

This room covers the CIA Triad — the three core principles that practically every security decision in the industry traces back to. Nothing groundbreaking at first glance, but spending focused time with it forced me to think about *why* controls exist rather than just *what* they do.

**Room:** CIA Triad — TryHackMe  
**Completed:** June 2026

---

## What I Actually Learned

Going in, I knew the three words. Coming out, I could reason about trade-offs between them — which is the part that matters on the job.

A few things that clicked:

- Confidentiality and availability constantly pull against each other. Locking everything down protects data but breaks workflows. Finding that balance is a real skill.
- Integrity is the most underappreciated of the three. People focus on encryption and uptime, but undetected data tampering can be worse than either a breach or an outage.
- Most security controls map to more than one pillar simultaneously, which is why understanding the *principle* matters more than memorising the control.

---

## The Three Pillars

**Confidentiality** — keeping data accessible only to those authorised to see it. Controls: encryption at rest and in transit, MFA, RBAC, least-privilege access.

**Integrity** — ensuring data hasn't been altered without authorisation. Controls: hashing (SHA-256, MD5 for verification), digital signatures, audit logs, file integrity monitoring.

**Availability** — keeping systems and data accessible when needed. Controls: redundancy, load balancing, backups, disaster recovery planning, DDoS mitigation.

---

## Controls Mapped to Pillars

| Control | Confidentiality | Integrity | Availability |
|---|:---:|:---:|:---:|
| Encryption | ✅ | | |
| MFA | ✅ | | |
| Hashing | | ✅ | |
| Digital Signatures | | ✅ | |
| RBAC | ✅ | ✅ | |
| Backups | | | ✅ |
| Load Balancing | | | ✅ |
| Disaster Recovery | | | ✅ |
| Audit Logs | | ✅ | |

---

## Real-World Context

These aren't abstract ideas. Every incident you'll work as a SOC analyst maps back here:

- Ransomware → attacks all three simultaneously (encrypts data, corrupts integrity, destroys availability)
- Insider threat → confidentiality and integrity failure
- DDoS → pure availability attack
- SQL injection → confidentiality breach, potential integrity violation

Understanding the triad lets you categorise an incident fast and communicate impact clearly to non-technical stakeholders — which is a core SOC skill.

---

## Skills This Reinforced

- Security fundamentals and terminology
- Threat classification by CIA impact<img width="1920" height="1080" alt="Screenshot (1)" src="https://github.com/user-attachments/assets/cd4c5a8b-9f96-4b22-a98e-eda07ee93b5b" />

- Security control reasoning
- Risk communication

---

## Takeaway

The CIA Triad is one of those things that sounds like entry-level content but keeps showing up at every level of the field. The room is a good forcing function to make sure you can actually explain and apply the concepts, not just name them.

---    and here is the link to view the activity shared to linkedin from tryhackme :::::    https://www.linkedin.com/posts/jimoh-quazeem-629715345_the-cia-triad-share-7468806157550411776-_cdt/?utm_source=social_share_send&utm_medium=member_desktop_web&rcm=ACoAAFZs2kEBu-zwYDsp-ymWfysvlm7q-roomoI

## Disclaimer

This write-up reflects my own understanding and notes. No flags, room answers, or proprietary TryHackMe content are disclosed. Written for portfolio and learning documentation purposes only.
