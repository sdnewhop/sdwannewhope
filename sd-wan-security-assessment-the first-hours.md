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
We will follow this idea and consider checks that cen be applied to any SD-WAN system.

## SD-WAN Security Assessment Checklist
