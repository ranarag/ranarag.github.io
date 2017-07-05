---
layout: post
title: "Tensorflow Basics"
date: 2017-07-05 21:25:58
image: '/assets/img/'
description: "Getting Started With Tensorflow"
tags:
- Tensorflow
- Python
- Deep learning
- Neural Networks
categories:
- Deep Learning
twitter_text:
---

## What is Tensorflow?

Tensorflow is an open source software for machine learning developed by Google.Tensorflow's, as one can get from its name, mainly handles matrices(or tensors), its mathematical operations and differentiation efficiently.It is just like Theano but with some extra features like  it can be used on distributed systems.


## Installing Tensorflow

Installing tensorflow >= 1.1.0 can be done using python-pip
{% highlight bash %}
pip install --upgrade tensorflow # for the CPU only version
pip install --upgrade tensorflow-gpu # for the GPU version
{% endhighlight %}

## Key-Components
Tensorflow works by first creating a computational graph resembling the model we wish to run and then executing it.
A program written using tensorflow must consist of the following components:
> 1.Variables: variables in tensorflow are in memory buffers containing tensors,but unlike normal tensors that live only for a single execution of a graph, variables values live as long as the session exists.Variables value cease to exist after the session is closed. Tensorflow has the option of saving variables' value to disk and restoring them for later use.Variables must be initialized before executing a graph for first time.
During training operation variables get updated by default.We can keep a variable unchanged by explicitly setting its trainable parameter to false.
{% highlight python %}
>>> import tensorflow as tf
>>> # Declaring a tensoflow Variable
>>> W = tf.Variable(tf.random_uniform([2,3],stddev=0.5), # same a numpy.random.uniform
name='weight') # name of the variable in the computational graph
>>> # Setting variable b to non -trainable
>>> b = tf.Variable(tf.zeros([1]), # same as numpy.zeros
name='b', trainable=False)
>>> s = tf.Session() # session created
>>> s.run(tf.initialize_all_variables()) # To initialize all the variables present in the current session
>>> s.run(tf.initialize_variables(W)) # To only initialize W and not b
{% endhighlight %}

### More to add :)
## comments

Please feel free to comment in the comment section below
