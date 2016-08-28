---
layout: post
title: "POST Endianess of your PC"
date: 2016-08-28 14:54:27
image: '/assets/img/'
description: 'How to check the endianess of your computer using a cpp code'
tags:
- networks
- c++
- tricks
categories:
- byte ordering in the network layer
twitter_text:
---

While studying networks for my job interviews I came across a two system calls namely
- ntoh(s/l)
- hton(s/l)
Both of the above are related to byte ordering done in the network layer

## ntoh(s/l)
It is used by host to convert a packet from network byte order to host byte order.
(s for short and l for long).

## hton(s/l)
It is used by host before sending a packet to the network.
This function converts a packet in host byte order to network byte order.
(s for short and l for long).


I am not writing the example syntaxes of the above functions because you can easilly get them
in the internet.

## What will happen if I do not use the above functions?
Well this depends upon the endianess of  your machine.
If your machine follows Big Endian then you can do away with the functions,
but if your pc follows little endian then you may get erroneous results.
This is beacuse almost all network protocols follow big endian.

## How to check endianness of your pc
- You can either use the following command

{% highlight bash %}
lscpu
{% endhighlight %}

and check the endianness of your pc

- You can also use the following cpp code to check the endianness of your pc

{% highlight bash %}
 #include <stdio.h>
int main(void) 
{
   unsigned long i = 1;
   int *c = (int*)&i;
   if (c[0]==1)    
       printf("Little endian\n");
   else if(c[1]==1)
       printf("Big endian\n");
   else
    printf("Unknown Endianness\n"); 
   
}
{% endhighlight %}

## Questions

Please feel free to ask questions in the comment section below.