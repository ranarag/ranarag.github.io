---
layout: post
title: "Sampling Theory and Distributions"
date: 2019-11-05 19:50:36
image: '/assets/img/'
description:
tags:
- statistics
- hypthesis testing
- samples
categories: 
- statistics
- mathematics
- probability

twitter_text:
---


<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
# Sampling Theory

Data scientists are required to draw conclusions about a group, a.k.a *population* from a few *samples* of it because
 getting the entire population is intractable.
This process of drawing samples is called *sampling*. There are different kinds of sampling , few of which are:
- Random sampling
- Clustered sampling
- Stratified sampling
- Systematic sampling
You can read about them over [here](https://medcraveonline.com/BBIJ/BBIJ-05-00149.pdf)
The drawing of conclusions or *inference* about the population from the samples is called *statistical inference*.

In this section we will consider two different types of samples:
- Sampling with Replacement
- Sampling without Replacement

## Random Sampling with Replacement
As the name suggests, this is a type of sampling where each member of the population may be included more than once.
It's like picking a ball from an urn and then putting it back into the urn.

## Random Sampling without Replacement
In this type of sampling, each member of the population can be included atmost once.
A similar example for this type of sampling would be picking a ball from the urn and not putting it back inside the urn.

## Sampling statistics
A quantity obtained from the sample for the purpose estimating a population parameter is called a *sample statistic* or briefly *statistic*.
Mathematically, a sample statistic for a sample of size $$n$$ can be defined as a function of the random variables $$X_1, X_2,...,X_n$$ i.e., $$g(X_1, X_2,...,X_n)$$.
The function $$g(X_1, X_2,...,X_n)$$ is another random variable whose values can be represented by $$g(x_1, x_2,...,x_n)$$.

## Sampling Distributions





#### Note: This chapter has sections taken from the book and Statistical Methods course offered at IIT Kharagpur