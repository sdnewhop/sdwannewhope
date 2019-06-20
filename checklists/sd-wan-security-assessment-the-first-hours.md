# SD-WAN Security Assessment: The First Hours

## Introduction

Suppose you need to perform a security assessment of an SD-WAN solution.
There are several reasons for this: one of them is selecting SD-WAN provider or product.

A traditional SD-WAN system involves many planes, technologies, mechanismsa, services, and features.
It has distributed and multilayered architecture. So where should you start?

This document is based on the JP Aumasson's approach described in series of auditing crypto articles
([[1](https://research.kudelskisecurity.com/2019/02/07/auditing-rust-crypto-the-first-hours/)],
[[2](https://research.kudelskisecurity.com/2017/04/24/auditing-code-for-crypto-flaws-the-first-30-minutes/)]).

The main goal of this document is to list basic sanity checks that can be used when investigating SD-WAN.
We will consider general checks that can be applied to any SD-WAN system.

## SD-WAN Security Assessment Checklist

### Common

1. What third-party components and libraries are used? How secure are these? Are the components using their latest versions?
2. Run [lynis](https://github.com/CISOfy/lynis) tool on each node and assess the hardening level.
3. Run a host-based vulnerability scanner ([vulners](https://github.com/videns/vulners-scanner), [LibScanner](https://github.com/DanBeard/LibScanner), etc.) and assess the patch management level.

### Architecture
1. Is a vendor-controlled cloud management interface used within the architecture?

### Zero Touch Provisioning
1. How does a network device get its initial configuration?
2. How does a network device discover controller, orchestrator and other entities?
3. How do network devices, the controller and the orchestrator authenticate each other?
4. How trust is provisioned and what mechanisms are used? One-time tokens, X.509 certificates, login and password, pre-shared keys?

### Cryptography

1. Which cryptographic protocols and implementations are used on the dataplane?
2. Are AEAD ciphers supported?
3. How key management is implemented?
4. How consistent are the security levels of the various protocols and primitives?
5. Look for legacy primitives like DES, TripleDES, RC4, MD5, SHA1 or custom primitives.

### Secure Communications

1. Which protocols are used between orchestrator, controller, and edge devices? Are they secured?
2. How SD-WAN entities do authenticate each other?
3. Run WhireShark on ochestrator or controller nodes, review traffic and check whether unencrypted packets are sent.
4. Do the chosen protocols and primitives provide the security required by your threat model?
5. Is RSA key exchange used?
6. Where and how secrets (e.g., private keys, pre-shared keys, tokens) are stored?
7. Check whether the same hardcoded certificate is used on different deployments.
8. Is a key renewal mechanism supported on control channels?

### Web Management Interface

1. Protection against CSRF attacks.
2. HTTPS supporting and hardening.
3. Protection against Slow HTTP DoS attacks.
4. Are cryptography secrets accessible via the Web interface?