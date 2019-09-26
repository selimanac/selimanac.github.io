---
title: "PCG Random Number Generator for Defold Released"
published: true
excerpt_separator: <!--more-->
repo: defold-random
tags: [defold, madewithdefold]
---

![PCG Random Number Generator](/assets/gfx/pcg-header-2000x666.png){: .fit-image}
  
  
This extension allow you to generate random numbers using minimal [C implementation of PCG](http://www.pcg-random.org/using-pcg-c-basic.html).


<!--more-->

It uses [entropy](https://github.com/imneme/pcg-c/blob/master/extras/entropy.c) seed internally with fallback to time based seed. You can switch to Time based seed and remove the entropy by uncommenting/commenting a few lines on the source code, but I don't think it is necessary.  


