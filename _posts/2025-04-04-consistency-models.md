---
layout: single
title:  "Consistency models and their interplay"
date: 2025-04-4
permalink: /posts/2025/04/consistency-models/
tags:
  - Consistency models
  - Distributed systems
  - Transactions
  - Concurrency systems
---

Consistency models are difficult to explain and even more difficult to understand. At the time of writing, there is about 40 consistency levels that I know of, each with its own set of assumptions and implications which in a lot of cases are only subtly different between different consistency levels. Adding to this complexity is the fact that different communities refer to different things with the same name. Take Snapshot Isolation(SI) for example. To a relational database practitioner, SI means concurrent snapshots that remain isolated from each other. It is not really a consistency level but rather the Isolation property in the ACID mode. But for a distributed systems practitioner, SI means something completely different. 

In an attempt to make these definitions clear for myself and hopefully for you, dear reader; I am writing this post. 
It is mostly based on the definitions from the following sources. 
1. [Consistency in Non-Transactional Distributed Storage Systems](https://arxiv.org/pdf/1512.00168)
2. [Highly Available Transactions: Virtues and Limitations](https://www.vldb.org/pvldb/vol7/p181-bailis.pdf)
3. [Consistency Models](https://jepsen.io/consistency/models)
  


![Consistency models](/images/consistency-models.svg){:width=70%}
*source: Jepsen.io*

Fundamentally, a consistency level is a set of predicates, evaluated over a history. The evaluation result of the predicates dictates if the history adheres to that consistency level i.e. that history is "legal" or "valid".

The more restrictive the consistency level (towards the top in the hierarchy of consistency levels), the stronger it is.

### Read Uncommitted
As the name suggests, it allows a transaction to read uncommitted updates from other transactions. Ergo, it can read concurrent uncommitted updates, perform a computation based on those updates. Meanwhile, the transaction whose update was observed might fail, causing an inconsistent data state. 

This is probably the weakest consistency level which is guaranteed by all databases. 

There is one caveat though, this definition is according to the ANSI SQL 1999 spec. In the distributed systems community, we prefer the definition laid down by Adya in his [thesis](https://pmg.csail.mit.edu/papers/adya-phd.pdf), which prevents dirty writes. 