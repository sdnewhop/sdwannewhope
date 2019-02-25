# SD-WAN Security Assessment: The First Hours

## Introduction

Suppose you need to perform a security assessment for an SD-WAN solution.
There are several reasons for this: one of them is selecting SD-WAN provider and product.

A traditional SD-WAN system consists of many technologies, planes, services, and features.
It has distributed and multylayered architecture...
So where should you start?

This document is based on the JP Aumasson's approach described in series of auditing crypto articles
([[1](https://research.kudelskisecurity.com/2019/02/07/auditing-rust-crypto-the-first-hours/)],
[[2](https://research.kudelskisecurity.com/2017/04/24/auditing-code-for-crypto-flaws-the-first-30-minutes/)]).

The main idea is to list basic sanity checks that can be used when investigating SD-WAN.
We will follow this idea and consider checks that can be applied to any SD-WAN system.

## SD-WAN Security Assessment Checklist

### Common

1. What third-party components and libraries are used? How secure are these? Are the components using their latest versions?
2. Run [lynis](https://github.com/CISOfy/lynis) tool on each node and assess the hardening level.
3. Run a host-based vulnerability scanner ([vulners](https://github.com/videns/vulners-scanner), [LibScanner](https://github.com/DanBeard/LibScanner), etc.) and assess

### Cryptography

1. Which cryptographic protocols and implementations are used on the dataplane?
2. Are AEAD primitives are supported?
3. How key management is implemented?
4. How consistent are the security levels of the various protocols and primitives?
5. Look for legacy primitives like DES, TripleDES, RC4, MD5, SHA1 or custom primitives.

### Secure Communications

1. Which protocols are used between orchestrator, controller, and edge devices? Are they secured?
2. How SD-WAN entities are authenticated?
3. Run WhireShark on ochestrator and controller nodes, review traffic and check whether unencrypted packets are sent.
4. Do the chosen protocols and primitives provide the security required by your threat model?
5. Is RSA key exchange is used?
6. Where and how secrets are stored?
7. Check whether the same hardcoded certificate is used on different deployments.
8. Is a key renewal mechanism is supported on control channels?

### Web Management Interface

1. Protection against CSRF attacks.
2. HTTPS supporting and hardening.
3. Protection against Slow HTTP DoS attacks.
4. Are cryptography secrets accessible via the Web interface?
