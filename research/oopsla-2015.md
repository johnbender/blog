---
layout: post
title: Declarative Fence Insertion
tags:
  - OOPSLA
date: 2015-10-28
authors:
  - John Bender
  - Jens Palsberg
---

Previous work has shown how to insert fences that enforce sequential consistency. However, for many concurrent algorithms, sequential consistency is unnecessarily strong and can lead to high execution overhead. The reason is that, often, correctness relies on the execution order of a few specific pairs of instructions. Algorithm designers can declare those execution orders and thereby enable memory-modelindependent reasoning about correctness and also ease implementation of algorithms on multiple platforms. The literature has examples of such reasoning, while tool support for enforcing the orders has been lacking until now. In this paper we present a declarative approach to specify and enforce execution orders. Our fence insertion algorithm first identifies the execution orders that a given memory model enforces automatically, and then inserts fences that enforce the rest. Our benchmarks include three off-the-shelf transactional memory algorithms written in C/C++ for which we specify suitable execution orders. For those benchmarks, our experiments with the x86 and ARMv7 memory models show that our tool inserts fences that are competitive with those inserted by the original authors. Our tool is the first to insert fences into transactional memory algorithms and it solves the long-standing problem of how to easily port such algorithms to a novel memory model.

- [PDF](/assets/oopsla-2015.pdf)
- [Project: Parry](https://bitbucket.org/ucla-pls/parry)