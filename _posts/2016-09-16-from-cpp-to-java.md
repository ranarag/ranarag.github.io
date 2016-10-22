---
layout: post
title: "from CPP to Java"
date: 2016-09-16 16:08:49
image: '/assets/img/'
description:
tags:
- coding
- C
- CPP
- Java

categories:
- cpp to java cheatsheet
twitter_text:
---

Some differences between c++ and java:


1. Java compiled code is platform independent whereas c++ compiled code is
  platform dependent

2. Java interpreter reports the run-time error that caused the execution to halt
  unlike in c/c++ programs which may simply crash

3. c/c++ do not have strict sizes for the fundamental datatypes(varies from
  machine to machine) whereas Java defines strict sizes for their datatypes

4. Java has additional positive and negative zeros, positive and neagtive infinites and "nan"(not a number values)

5. c/c++ has functions while Java has methods.In c/c++ functions can be defined outside a class
Java doesnot allow methods to be defined outside a class.

6. Unlike c++  arrays, Java arrays are objects.

7. Unlike c++, strings are immutable in Java.

8. While in c++ classes "public", "private" and "protected" are labels , in Java they are modifiers. Each member has its own access modifier. Java also has a no-modifier(a.k.a package-private) option which makes
the member visible only within its own package.

9. Unlike c++, Java method definitions do not have
semicolon at the end of their closing brackets.

10. Java uses the "extends" keyword while inherting features of a class to specify the superclass.

11. Java [does not support multiple inheritance but supports multiple interfaces](http://www.programmerinterview.com/index.php/java-questions/multiple-inheritance/).


12. Unlike c++ Java has [interfaces which is a bit different from abstract class](www.javatpoint.com/difference-between-abstract-class-and-interface).


13. In Java superclass constructors are callled using the keyword "super".

14. Unlike c++ Java has class hierarchy. The  "Object" class is the root of this hierarchy.
All classes are subclasses of this root class.


### There are many other differences also but these basic differences will help you get your hands dirty with Java !! :)
