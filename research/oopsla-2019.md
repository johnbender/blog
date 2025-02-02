---
layout: post
title: A Formalization of Java's Concurrent Access Modes
tags:
  - OOPSLA
date: 2019-10-20
authors:
  - John Bender
  - Jens Palsberg
---

Java’s memory model was recently updated and expanded with new access modes. The
accompanying documentation for these access modes is intended to make strong
guarantees about program behavior that the Java compiler must enforce, yet the
documentation is frequently unclear. This makes the intended program behavior
ambiguous, impedes discussion of key design decisions, and makes it impossible
to prove general properties about the semantics of the access modes. In this
paper we present the first formalization of Java’s access modes. We have
constructed an axiomatic model for all of the modes using the Herd modeling
tool. This allows us to give precise answers to questions about the behavior of
example programs, called litmus tests. We have validated our model using a large
suite of litmus tests from existing research which helps to shed light on the
relationship with other memory models. We have also modeled the semantics in Coq
and proven several general theorems including a DRF guarantee, which says that
if a program is properly synchronized then it will exhibit sequentially
consistent behavior. Finally, we use our model to prove that the unusual design
choice of a partial order among writes to the same location is unobservable in
any program.

- [Preprint](/assets/oopsla-2019.pdf) (accepted)
- [Project: Herd and Coq formalizations](https://bitbucket.org/ucla-pls/jam)
