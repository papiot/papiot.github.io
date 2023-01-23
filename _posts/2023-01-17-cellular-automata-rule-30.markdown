---
layout: post
title: Cellular Automata Rule 30
date: 2023-01-17
categories: AI
---

## Intro
I've discovered cellular automata while reading Stephen Wolfram's A New Kind of Science book. Although I was aware of Connway's Game of Life, which is also based on cellular automata, it was the first time I read indepth about this form of computation.

Cellular automata is a simple way of computation based on pre-defined rules. Nothing new here, however, what makes them unique is the ability to show that one can create emerging patterns from very simple rules.

### How they work
You start with a one dimentional grid of squares (a row of squares). The initial condition could be anything, but for simplicity reasons you can start with all white squares, except the middle one which is black.

Then each subsequent row (which goes underneath the original row) will take the colors based on the 3 cells above it. Each square can only have 2 colors: black or white.

Because we only take into account 3 cells, and each cell can be either black or white we have a total of 2<sup>3</sup> = 8 possible combinations. The combinations are as follows (0 is white 1 is black):

111, 110, 101, 100, 011, 010, 001, 000.

### Rule 30

Rule 30 is basically one of 256 rules which are possible to create using 3 cells. Each of the 3 cells will output 0 or 1, so if we look at the group of cells, we think of it as a binary number. Then rule 30 will mean 0 0 0 1 1 1 1 0 --> this is 30 in binary.

Let me re-write this in a few different ways:

111 --> 0<br>
110 --> 0<br>
101 --> 0<br>
100 --> 1<br>
011 --> 1<br>
010 --> 1<br>
001 --> 1<br>
000 --> 0<br>

And yet in another way to make it more clear:

<pre>
1 1 1
  0

1 1 0
  0

1 0 1
  0

1 0 0
  1

0 1 1
  1

0 1 0
  1

0 0 1
  1

0 0 0
  0
</pre>

Lastly, an image is 1000 words, so here is the same thing I have shown above, but with an image. 

![image-title-here](/assets/rule-30.svg)
{:class="img-responsive"}
*Source: wolfram.com https://mathworld.wolfram.com/Rule30.html*

The above image is generated after running 15 iterations (rows) using that rule. You can see that there seems to be some kind of random pattern. 

What happens if we run it for more iterations?
<br>
![image-title-here](/assets/Rule30Big.jpeg)
{:class="img-responsive"}
*Source: wolfram.com https://mathworld.wolfram.com/Rule30.html*

<br>

This last image shows the patter after it ran for 256 iterations. You can see that the left side of the pyramid has a constant or predictable pattern, but the right side has what seems like a random pattern with emerging triangles of different sizes.

Wolfram and other computer scientists and mathematicians have been studying these rules for a long time and it turns out that for this particular rule, the right side is really random.

This means that you cannot predict what the n<sup>th</sup> row will be like until you actually run through the entire computation.

### Implications
Wolfram has an entire book dedicated to this. He believes our universe is made up of similar rules. Simple rules that create everything around us. I will go into more details on that topic perhaps in a different post; I now want to focus on cellular automata.

I also believe that most of what we sense is an emergence of underlying simple rules. What are those rules? We don't know.

Some of these patterns are not just purely theoretical. They have been observed in real life. Here are some examples of cellular automata type of design found in nature:
<br>

### Rule 110 and Universal Computation (Turing Complete)
One of the craziest rules is rule 110, pictures below:
<br>

![image-title-here](/assets/rule110-small.png)
{:class="img-responsive"}
*Source: wikipedia.com https://en.wikipedia.org/wiki/Rule_110*
<br>

![image-title-here](/assets/rule110.png)
{:class="img-responsive"}
*Source: wikipedia.com https://en.wikipedia.org/wiki/Rule_110*
<br>

This rule has been proven to bee Turing Complete. This means that any computer program can be ran using only this rule. It would be pretty challenging to engineer it, but in theory it is possible.

If a Turing Complete emergence can happen from a very simple 1-D cellular automata, I wonder what else can emerge from more complex rules? Or perhaps the rules are supposed to be simple, and only the emergence complex. 

In order to understand this behaviour better, here's my implementation of these:

### My Own Implementation
I have created my own implementation of these rules and posted the video of making this on Youtube. 
You can watch it here:

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/7QxbsE0ozl0/0.jpg)](https://www.youtube.com/watch?v=7QxbsE0ozl0)
<br>