---
layout: page
title: GoLite Compiler
description: A lite compiler which is able to compile a custom portion of GoLang
img: 
importance: 1
category: course proj
---

In a team of two, Qi An and I implemented a multi-pass compiler for a subset of GoLang that we called "GoLite". With instructions and grammer provided from our professor, we built:
- a scanner to tokenize the input source code, 
- a recursive-descent parser to make syntax analysis based on GoLite's grammer, build abstract syntax tree (AST) and symbol table, 
- a semantic analyzer to ensure that the program conforms to the static semantics of the language, followed by a type checker
- an intermediate representation translator (we use ILOC as IR here) to convert validated AST to IRs, 
- code generator to convert ILOC to Assembly (Armv8).

Link to GitHub repo: <https://github.com/yuanheng-zhao/GoLite-Compiler>
