---
layout: post
title: Compiling Volatile Correctly in Java
tags:
  - ECOOP
authors:
  - Shuyang Liu
  - John Bender
  - Jens Palsberg
date: 2022-02-25
---

The compilation scheme for Volatile accesses in the OpenJDK 9 HotSpot Java Virtual Machine has a major problem that persists despite a recent bug report and a long discussion. One of the suggested fixes is to let Java compile Volatile accesses in the same way as C/C++11. However, we show that this approach is invalid for Java. Indeed, we show a set of optimizations that is valid for C/C++11 but invalid for Java, while the compilation scheme is similar. We prove the correctness of the compilation scheme to Power and x86 and a suite of valid optimizations in Java. Our proofs are based on a language model that we validate by proving key properties such as the DRF-SC theorem and by running litmus tests via our implementation of Java in Herd7

- [Preprint](/assets/ecoop-2022.pdf) (accepted ECOOP'22)
- [Project: Herd and Coq formalizations](https://github.com/ShuyangLiu/ECOOP22-Supplementary-Material)
