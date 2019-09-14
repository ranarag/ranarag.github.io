---
layout: post
title: "How to Install Packages Locally in Linux"
date: 2019-09-12 20:41:53
image: '/assets/img/'
description: "How to Install Packages Locally in Linux"
tags:
- Linux
- systems
- server accounts
- hacks
categories:
- Systems
twitter_text:
---

## Some Prerequisites

### What is a variable?

A  variable is a storage location for a value. Linux has environment variables. It can store strings, numbers , etc. just like the variables in C, C++, python, or any other programming language. It even has a scope, just like the variables in other programming languages! Based on scopes Linux environments variables can be classified into 2 different categories:

1. Local Variables
2. Global Variable


#### Local Variables
Local variables are set by typing  \<variable_name\>= \<variable_value\> (i.e without the export command).
Local variables can only be accessed by the terminal where it is declared and not by any program even if it is run from the terminal itself.

#### Global Variables
Global variables are set by typing export  \<variable_name\>= \<variable_value\>. The export command ensures that the variable be exported to any child process forked from that terminal. In short, it ensure that the variable set is global.


#### Understanding the Difference

There is a simple way to understand the difference between local and global environmnent variables.

Open a terminal
{% highlight bash %}
export global_var="This is a global variable"
local_var = "This is a local variable"
echo $global_var
echo $local_var
{% endhighlight %}
Now open tmuxa tmux session. Inside the session, type:
{% highlight bash %}
echo $global_var
echo $local_var
{% endhighlight %}

You would notice that the local variable inside the tmux session contains no value whereas the global variable outputs the value that it has been assigned.
You can see all the variables defined using the command 'env'.
A variable is unset by typing unset \<variable_name\>


#### Some Important Paths in Linux:
In this journey of learning how to install  packages locally in linux, we need to about two very important global environment variables:
1. PATH
2. LD_LIBRARY_PATH

(Not yet Finished!! :P)