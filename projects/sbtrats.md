# sbt-rats Parser Generator

sbt-rats provides a plugin that enables the [Rats! parser generator](https://cs.nyu.edu/rgrimm/xtc/rats.html) to be used in Scala projects.

The plugin enables you to use the Rats! parser generator with Scala projects that are built using the [Scala build tool sbt](https://www.scala-sbt.org/).
The parser can be specified directly using a Rats! specification or using a simplified syntactic notation.
The syntactic notation can also be translated into a Scala implementation of abstract syntax trees and a pretty printer for those trees.
Pretty-printing support is provided by the [Kiama language processing library](projects/kiama).

## Participants

* Anthony Sloane
* Franck Cassez
* Scott Buckley

## Publications

Sloane, A. M., Cassez, F., and Buckley, S. 2016. [The sbt-rats parser generator plugin for Scala](https://dl.acm.org/citation.cfm?id=3001580). Symposium on Scala. 110-113. [PDF](papers/scala16.pdf)

## Software

The sbt-rats software is released under the open source Mozilla public license. More information including documentation and source downloads can be found at the [sbt-rats project site](https://bitbucket.org/inkytonik/sbt-rats).
Binary distributions of sbt-rats are available on bintray.
