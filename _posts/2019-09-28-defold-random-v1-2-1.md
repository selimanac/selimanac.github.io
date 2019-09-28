---
title: "Defold - PCG Random Updated v1.2.1"
published: true
excerpt_separator: <!--more-->
repo: defold-random
tags: [defold, madewithdefold]
---

PCG Random Number Generator Native Extension for the Defold updated to version 1.2.1

<!--more-->

### Added static seed

#### rnd.seed(`init_state, init_seq`)

Seeds the random number generator.   
Random number generator is always initialized by using entropy seed. You don't need to call this method unless you want to control the seed.


`init_state` is the starting state for the RNG, you can pass any 64-bit value.  
`init_seq` selects the output sequence for the RNG, you can pass any 64-bit value, although only the low 63 bits are significant.
 
**Caution:** I don't recommend using of 64-bit integers. Consider using 32-bit integers instead. 

#### rnd.seed()

Re-seed the random number generator by using entropy seed.  
Random number generator is always initialized by using entropy seed. You don’t need to call this method unless you want to re-seed.
