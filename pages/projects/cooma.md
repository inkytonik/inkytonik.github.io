---
layout: post
title: Cooma Secure Programming Language
permalink: /projects/cooma/
---

The Cooma project is investigating secure programming language design based on a pure functional core language and fine-grained object capabilities.

## Participants

* [Anthony Sloane](https://inkytonik.github.io)
* Nicholas Weston (2021-)
* Diego Ocampo Herrera (2019-2020)
* Cameron Pappas (2019-2020)

## Funding

![Oracle](/assets/img/Oracle Red Badge.png)

## Planned Features

* Functional core compiled to a continuation-passing intermediate representation (["Compiling with continuations, continued", Kennedy, ICFP 2007](https://doi.org/10.1145/1291151.1291179))

* Row-based data types capable of encoding record types with variants and object-oriented style extension (["Abstracting extensible data types: or, rows by any other name", Morris and McKinna, POPL 2019](https://doi.org/10.1145/3290325))

* Fine-grained object capability-based effects (["A Study of Capability-Based Effect Systems", Liu, EPFL, 2016](https://github.com/liufengyun/stoic))

* Resource capabilities checked and provided by runtime system

* Implicit argument resolution to avoid passing many capability parameters (["COCHIS: Stable and coherent implicits", Schrijvers, Oliveira, Wadler and Mantirosian, JFP, 2019](http://dx.doi.org/10.1017/s0956796818000242))

## Status

Specification and reference implementation is under way.

* Functional core with tail call optimisation
* Row-based record and variant data types (literals, selection, concatenation, simple matching)
* Object capabilities via records
* Runtime-provided resource capabilities (I/O operations only)
* Implicit argument resolution (not started)
* Single shared frontend (parsing, semantic analysis, compilation to continuation-based IR)
* Two IR back-ends (reference and Truffle/GraalVM)
* File-based execution and read-eval-print loop (REPL)

## Blocks (value and function definitions)

```scala
{
    val x = 10
    val y = 20
    y
}
```

evaluates to `20`.

```scala
{
    def f (x : Int) : Int = x
    def g (y : Int) : Int = f(y)
    g(10)
}
```

evaluates to `10`.

## Records

```scala
{
    val r = {x = 10, y = 20}
    val s = {a = "Hi"}
    {r & s}.x
}
```

evaluates to `10`.

## Variants

```scala
{
    val Boolean = <false : Unit, true : Unit>
    val false = <false = {}>
    val true = <true = {}>

    def f (b : Boolean) : Int =
        b match {
            case false x =
                1
            case true x =
                2
        }

    {a = f(false), b = f(true)}
}
```

evaluates to `{a = 1, b = 2}`.

## I/O capabilities

Command-line arguments can be typed as built-in capabilities such as `Writer` and `Reader`.
The corresponding argument value is checked and, if ok, provides a capability record to access the named file.
These capabilities cannot be created directly, so other files cannot be accessed even if the user has permissions to access.

```scala
fun (w : Writer, r : Reader) = w.write(r.read())
```

Sample execution from Scala Build Tool:

```shell
run - /some/file.txt
```

If the user has read permission on `/some/file.txt`, this program writes the content of that file to standard output.
Otherwise, it fails with `cooma: Reader capability unavailable: can't read /some/file.txt`.

## Software

The Cooma source code can be found on [github](https://github.com/inkytonik/cooma).

Cooma uses the following libraries and tools:

* [Kiama Language Processing Library](/projects/kiama)
* [sbt-rats parser generator](/projects/sbtrats)
* [GraalVM](https://www.graalvm.org/) with Truffle
