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


[1.] Strong source code analyzers like [valgrind]( http://valgrind.org)

[2.] debuggers like gdb

[3.] stable compilers

[4.] Test support tools


Following are the 10 rules the author wants to emphasize upon:


[1.] > Rule: Restrict all code to very simple control flow constructs – do not use goto
   > statements, setjmp or longjmp constructs, and direct or indirect recursion.


The author says to restrict all code to very simple control flow constructs because
it enhances code clarity. Now asking not to use recursion might look suprising but
this is also used to improve code clarity.(Remember that every recursive solution has an
equivalent iterative solution.)


[2.] >  Rule: All loops must have a fixed upper-bound. It must be trivially possible for a
   > checking tool to prove statically that a preset upper-bound on the number of iterations
   > of a loop cannot be exceeded. If the loop-bound cannot be proven statically, the rule
   > is considered violated.

I think this rule does not need any explanations except for the fact that this rule is not applicable to iterations that
are non-terminating(e.g. in a  process scheduler).In those cases we need to statistically prove that no upper-bound exists for such a problem.


[3.] > Rule: Do not use dynamic memory allocation after initialization.

This rule is given because memory allocators and garbage collectors often have unpredictable behaviour which might cause a coding error.

[4.] > Rule: No function should be longer than what can be printed on a single sheet of
     > paper in a standard reference format with one line per statement and one line per
     > declaration. Typically, this means no more than about 60 lines of code per function.

[5.] > Rule: The assertion density of the code should average to a minimum of two
     > assertions per function. Assertions are used to check for anomalous conditions that
     > should never happen in real-life executions. Assertions must always be side-effect
     > free and should be defined as Boolean tests. When an assertion fails, an explicit
     > recovery action must be taken, e.g., by returning an error condition to the caller of the
     > function that executes the failing assertion. Any assertion for which a static checking
     > tool can prove that it can never fail or never hold violates this rule. (I.e., it is not
     > possible to satisfy the rule by adding unhelpful “assert(true)” statements.)

[6.] > Rule: Data objects must be declared at the smallest possible level of scope.

[7.] > Rule: The return value of non-void functions must be checked by each calling
     > function, and the validity of parameters must be checked inside each function.

[8.] > Rule: The use of the preprocessor must be limited to the inclusion of header files and
     > simple macro definitions. Token pasting, variable argument lists (ellipses), and
     > recursive macro calls are not allowed. All macros must expand into complete
     > syntactic units. The use of conditional compilation directives is often also dubious,
     > but cannot always be avoided. This means that there should rarely be justification for
     > more than one or two conditional compilation directives even in large software
     > development efforts, beyond the standard boilerplate that avoids multiple inclusion of
     > the same header file. Each such use should be flagged by a tool-based checker and
     > justified in the code.

[9.] >  Rule: The use of pointers should be restricted. Specifically, no more than one level of
     > dereferencing is allowed. Pointer dereference operations may not be hidden in macro
     > definitions or inside typedef declarations. Function pointers are not permitted.

[10.] > Rule: All code must be compiled, from the first day of development, with all
      > compiler warnings enabled at the compiler’s most pedantic setting. All code must
      > compile with these setting without any warnings. All code must be checked daily with
      > at least one, but preferably more than one, state-of-the-art static source code analyzer
      > and should pass the analyses with zero warnings.
### please pardon me for my incomplete work; will complete it soon ###
