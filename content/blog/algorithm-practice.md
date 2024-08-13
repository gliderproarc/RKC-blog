+++
title = "Algorithm practice"
author = ["Robert Clay"]
date = 2021-04-05
lastmod = 2024-08-14T08:34:03+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-04-05 Mon]</span></span>,#coding


## Thinking in algorithms is hard {#thinking-in-algorithms-is-hard}

For the coders out there reading this, maybe you have forgotten what it is like
to first wrap your head around some really basic ideas and concepts when it
comes to talking to computers, but I am in the middle of learning about different
programming languages, styles, and algorithms. As much as I think I have a
handle on things, I find that I still have a ways to go, especially when it
comes to algorithms.

I remember watching a talk called C++ seasoning, or something like that. It is
apparently a rather famous C++ talk about not reinventing the wheel and using the
algorithms that your language provides. I don't intend to teach my self and C++,
and I don't think I will ever need to go that deep into a computer. But I DID
find what he said to be very interesting and it helped me think about how I
work with my languages.

Right now I am teaching myself Lisp and Python. Technically it's more like;
Elisp, Hylang, Clojure, and Python, but Hylang is just a Clojure like lisp
syntax for Python, and Clojure is modern lisp while Elisp is an older lisp used
almost exclusively for talking to Emacs, so I really only think of those three
lisps and "just learning lisp". And with Lisp and these dynamic higher level
languages, I don't need to re-invent the wheel. Clojure and Python have amazing
standard libraries, and I don't need to make a sorting algorithms in most cases.
It's usually made for me. And they have usually implemented it in a way that is
faster than I could make it myself.

Take NumPy for example. A lot of NumPy calls to C, and can run a lot of math
much faster than I can tell the Python run-time to do it. So rather than trying
to make it from scratch, I can get a lot of performance simply by using the
tools in NumPy or even the standard library.


## But I could stand to learn about algorithms too {#but-i-could-stand-to-learn-about-algorithms-too}

...so I found a few websites with algorithms that beginner coders can learn. I
have recently made a binary search, a greatest common denominator, and today I
WAS going to try to make a bubble sort, but ran into the limitations of my
understanding of algorithms.

Coding is like a muscle. The more you use it, the stringer it gets. And I am
beginning to see how I have a long ways to go. Bubble sorts are apparently
rather inefficient and mostly used just for teaching people like me, but I took
the problem and made a bit of a mes of it.

Having learned about functional programming, I decided I would try to make a
bubble sort that was sort-of functional. Not a good idea. The whole mechanism of
the sort is swapping elements in an array, that is a mutation of state. I was
trying to make some recursive calls to local variables in Elisp to get it all
working, and ended up making something that took hours to type and didn't look
neat, clean, elegant, or fast.

And when I think back on how I got there, I see how I just don't have a lot of
practice breaking a problem down into parts I can handle with built in
algorithms. "car" "cdr" and "cons" were serving me well, but I also could have
been done in a few seconds with a standard library call to a sort function.
Learning how to express these ideas in code is a nice tool in the tool belt to
have. I also see how much work things like a standard library can save me if I can
learn to use it well. And if I find a problem is turning into something like
this, it could be that I am just overlooking a built-in that could save me some time.
