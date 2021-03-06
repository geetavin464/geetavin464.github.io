---
layout: post
title:  "Languages"
date:   2015-03-28 18:08:44
categories: programming
description: semantics compiled vs interpreted, scoping
---

* __Compiled Language__
  * Source Code -> Checker/Compiler -> Object Code -> Interpreter -> Output
  * Compiled languages are more efficient
  * Examples: C, Java, Go, Haskell, Lisp
  * Faster but immutable, very close to the machine
  * OS & Native Applications use compiled code
  * These languages do not support meta programming

* __Interpreted Language__
  * Source Code -> Checker -> Interpreter -> Output
  * If something goes wrong, the error message is in the language of the source code
  * Examples: Ruby, Javascript, Perl, Python, PhP
  * Slower but more flexible
  * These languages support meta programming

* __Imperative Programming__
  * Telling the machine, how exactly do something, to derive your expected result
  * Ex: Writing your own iterator

* __Declarative Programming__
  * Telling the machine, what exactly is your expected result, and let it deal with the specifics
  * Ex: Using built-in methods for iteration etc

* __Static Semantics__
  * A good programming language has very good static sematics
  * Does not allow statements like 7/abc and tells us it wrong

* __Instruction Set__
  * are like ingredients
  * Combine the instructions in clever ways to complex things

* __Fixed Program Computers__
  * Circuits were designed to do specific things and thats what they did

* __Scoping__
  * Lexical - You search for the variable in the current function, the function where the current function is defined and so on
  * Dynamic - You search for the variable in the current function, the function where the current function is called and so on