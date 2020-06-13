# Skink Software Verification Tool

Computer software routinely contains bugs and in many cases these bugs can be exploited to cause it to malfunction, including to reveal security issues.
Skink belongs to a growing collection of tools that can automatically analyse the software code to diagnose and report bugs.

Skink is a new tool that combines existing trace abstraction refinement techniques with a new implementation approach based on programming language specifications and tools.

We have entered Skink in the [International Competition on Software Verification (SV-COMP)](https://sv-comp.sosy-lab.org) in 2016-2018.

## Participants

* Anthony Sloane
* [Franck Cassez](https://au.linkedin.com/in/franck-cassez-b775807)

## Publications

Cassez, F., Sloane, A. M., Roberts, M., Pigram, M., Suvanpong, P., and de Aledo, P. G. 2017. [Skink: Static Analysis of Programs in {LLVM} Intermediate Representation](https://link.springer.com/chapter/10.1007/978-3-662-54580-5_27). International Conference on Tools and Algorithms for the Construction and Analysis of Systems. 380-384.  [PDF](papers/tacas17.pdf)

Cassez, F. and Sloane, A. M. 2017. [ScalaSMT: satisfiability modulo theory in Scala](https://dl.acm.org/citation.cfm?id=3136004). International Symposium on Scala. 51-55. [PDF](papers/scala17.pdf)

## Software

The Skink source code is not currently released.
Binary versions that were used in the International Competition on Software Verification can be found via the [competition website](https://sv-comp.sosy-lab.org).

Skink uses the following libraries and tools:

* [Kiama Language Processing Library](projects/kiama)
* [sbt-rats parser generator](projects/sbtrats)
* [ScalaSMT SMT solver library](https://bitbucket.org/franck44/scalasmt/src/master/)
