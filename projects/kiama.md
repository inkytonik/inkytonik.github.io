# Kiama Language Processing Library

The Kiama project is developing a language processing library in the Scala programming language.
Typical application domains for Kiama are compilers and interpreters for programming languages, code refactoring in integrated development environments, static code analysis, program transformation and natural language processing.

Language processing applications have often been approached using using automatic generation tools.
For example, lexing and parsing components are often generated from regular expressions or context-free grammars by tools such as Flex, YACC, Bison, ANTLR and JavaCC.
Using generators means that a correct implementation can be obtained easily from a problem description that is relatively close to the problem itself.
Unfortunately, generators imply a learning curve, don't solve the whole problem, and integrating them with the rest of the development process can be hard (e.g., for debugging).
Therefore, many developers resort to a hand-coding approach and thereby give up the benefits that higher-level approaches and tools can give.

The Kiama approach to this situation is to embed language processing facilities in a high-level language library.
By providing appropriate abstractions suitable for language processing, including grammars, rewriting rules and tree attribution, Kiama allows developers to concentrate on their problem, but still integrate easily with hand-written code. Scala is a powerful  language with a combination of object-oriented and functional features that are ideal for developing this kind of library.

## Participants

* [Anthony Sloane](https://inkytonik.github.io)
* Matthew Roberts
* Dominic Verity

## Publications

Sloane, A. M. and Roberts, M. 2015. [Oberon-0 in Kiama](https://www.sciencedirect.com/science/article/pii/S0167642315003032). Science of Computer Programming. 114, 20-32. [PDF](papers/scp15.pdf)

Sloane, A. M., Roberts, M., and Hamey, L. G. C. 2014. [Respect Your Parents: How Attribution and Rewriting Can Get Along](https://link.springer.com/chapter/10.1007/978-3-319-11245-9_11). International Conference on Software Language Engineering (SLE). 191-210. [PDF](papers/sle14.pdf)

Sloane, A. M. and Roberts, M. 2014. [Domain-specific program profiling and its application to attribute grammars and term rewriting](https://www.sciencedirect.com/science/article/pii/S0167642314000628). Science of Computer Programming. 96, 488-510. [PDF](papers/scp14.pdf)

Sloane, A. M., Kats, L. C. L., and Visser, E. 2013. [A pure embedding of attribute grammars](https://www.sciencedirect.com/science/article/pii/S016764231100205X). Science of Computer Programming. 78, 10, 1752-1769. [PDF](papers/scp13.pdf)

Premaratne, S., Sloane, A. M., and Hamey, L. G. C. 2013. [An Evaluation of a Pure Embedded Domain-Specific Language for Strategic Term Rewriting](https://www.igi-global.com/chapter/content/71817). In Formal and Practical Aspects of Domain-Specific Languages, IGI Global. [PDF](papers/chapter13.pdf)

Sloane, A. M. 2011. [Lightweight Language Processing in Kiama](https://link.springer.com/chapter/10.1007/978-3-642-18023-1_12). In Generative and Transformational Techniques in Software Engineering {III}, Springer. [PDF](papers/gttse09.pdf)

Kats, L. C. L., Sloane, A. M., and Visser, E. 2009. [Decorated Attribute Grammars: Attribute Evaluation Meets Strategic Programming](https://link.springer.com/chapter/10.1007/978-3-642-00722-4_11). International Conference on Compiler Construction. 142-157. [PDF](papers/cc09.pdf)

## Software

The Kiama software is released under the open source Mozilla public license. More information including documentation and source downloads can be found at the [Kiama project site](https://bitbucket.org/inkytonik/kiama).
Binary distributions of Kiama are available on Maven Central.
