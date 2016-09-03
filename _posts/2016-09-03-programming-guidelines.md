---
layout: post
title: "Programming Guidelines"
date: 2016-09-03 10:04:25
image: '/assets/img/'
description: 'How to write good code'
tags:
- coding
- C
- techniques
categories:
- coding guidelines by NASA programmer
twitter_text:
---

In the paper [The Power of Ten-Rules for Developing Safety Critical Code](http://spinroot.com/gerard/pdf/P10.pdf)
the author has stated 10 rules adhering to which will make one a good programmer.

The author chosed C as the language for writing safety critical code because of the extensive tool support for this language including:


1. Strong source code analyzers like [valgrind]( http://valgrind.org)

2. debuggers like gdb

3. stable compilers

4. Test support tools


Following are the 10 rules the author wants to emphasize upon:


1. > Rule: Restrict all code to very simple control flow constructs – do not use goto
   > statements, setjmp or longjmp constructs, and direct or indirect recursion.


The author says to restrict all code to very simple control flow constructs because
it enhances code clarity. Now asking not to use recursion might look suprising but
this is also used to improve code clarity.(Remember that every recursive solution has an
equivalent iterative solution.)


2. >  Rule: All loops must have a fixed upper-bound. It must be trivially possible for a
   > checking tool to prove statically that a preset upper-bound on the number of iterations
   > of a loop cannot be exceeded. If the loop-bound cannot be proven statically, the rule
   > is considered violated.


### please pardon me for my incomplete work; will complete it soon ###
