---
layout: post
title: Cooma Secure Programming Language
permalink: /projects/cooma/
---

The Cooma project is investigating secure programming language design based on a pure functional core language and fine-grained object capabilities.

## Participants

* [Anthony Sloane](https://inkytonik.github.io)
* Nicholas Weston (2021-2022)
* Diego Ocampo Herrera (2019-2020)
* Cameron Pappas (2019-2020)

## Funding

![Oracle](/assets/img/Oracle Red Badge.png)

## Status

* Functional core with tail call optimisation
* Row-based record and variant data types (literals, selection, concatenation, simple matching)
* Object capabilities as records
* File, database and web server command-line capabilities
* Single shared frontend (parsing, semantic analysis, compilation to continuation-based IR)
* Two IR back-ends (reference and Truffle/GraalVM)
* File-based execution and read-eval-print loop (REPL)

See the [Cooma Project on GitHub](https://github.com/inkytonik/cooma) for details, including examples.

## Software

The Cooma source code can be found on [GitHub](https://github.com/inkytonik/cooma).

Cooma uses the following libraries and tools:

* [Kiama Language Processing Library](/projects/kiama)
* [sbt-rats parser generator](/projects/sbtrats)
* [GraalVM](https://www.graalvm.org/) with Truffle
