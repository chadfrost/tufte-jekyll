---
layout: post
title: Making Trees
date: '2009-04-11T09:38:00.000-07:00'
author: BikeBoy
tags:
- art
- technology
- software
- coding
- visualization
modified_time: '2009-04-11T13:02:02.728-07:00'
thumbnail: http://1.bp.blogspot.com/_I4PygacntFw/SeDzT8zTTnI/AAAAAAAABAQ/NVrap72m6BI/s72-c/trees.png
blogger_id: tag:blogger.com,1999:blog-5444398.post-6263454217461741804
blogger_orig_url: http://blog.chadfrost.com/2009/04/making-trees.html
---
{% maincolumn 'assets/img/trees.png' 'Generative trees' %}

I've been making trees this morning. 

Some years ago, I bought an intriguing book: The Algorithmic Beauty of Plants, 
by Prusinkiewicz and Lindenmayer. I occasionally pick it up and read pieces, 
and always find it fascinating. The book does a great job describing the 
concept of L-systems, named for the second author, in which a few very simple 
rules can generate incredibly complex patterns. Studying how plants grow, the 
authors realized that the rules governing plant growth can be approximated 
with algorithms, producing very realistic-looking results. 
<!--more-->

I recently came across a piece of software that reminded me of the book, and 
led me back to re-examine it. [Context Free 
Art](http://www.contextfreeart.org/) allows you to write little recursive 
programs that output graphics, suitable for implementing some of the 
algorithms described in the book. (You can make all sorts of amazingly 
beautiful things with Context Free, plant-like things being but one example.) 

Much to my delight, I found the [Algorithmic Botany 
website](http://algorithmicbotany.org/) on which  the book is now available 
[electronically](http://algorithmicbotany.org/papers/#abop)! 

There turn out to be several other programs that try to render L-systems and 
their kin. I found a few of them still lurking around on the web, but the Unix 
versions are old enough that getting them to compile on my Mac looks to be a 
chore and a half; I found a [Java 
applet](http://home.clara.net/niknak/fractal/) that is buggy, but works for 
the most part and I can still compile it. I'd most like to play with 
[fractint](http://www.fractint.org/) -- I remember it fondly from the DOS 
days, and it turns out that someone put L-system interpretation into it -- but 
the last port to the Mac was for OS 9. I may have to revisit this, and see if 
I can get it to run under DOSBox... If so, I'll post the outcome here. 
