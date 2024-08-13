+++
title = "The curse of lisp"
author = ["Robert Clay"]
date = 2022-06-11
lastmod = 2024-08-14T08:52:57+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2022-06-11 Sat]</span></span>,#programming


## What is the curse of lisp? {#what-is-the-curse-of-lisp}

I have only really heard about it from this Lisper named Eric Normand (he runs a
great podcast and YouTube channel you should totally check out), and I am not
really sure if he made the term up or not, but I have my own take on what
learning Lisp has done for me as I am learning to program.

As I wrap up the chapter in m textbook on constraint satisfaction problems, I am
coming back to the differences between what my solutions look like between the
languages I have chosen to try out.

I wrote a simple maze solver in LFE, and it was made a bit more challenging than
it needed to be partly because of how much I tried to do with straight tuples
and only a basic understanding of the Erlang standard library. But it got the
job done, and it was simple enough to wrap my head around how I wanted to do it.

I then wrote a solution to the "Cannibals and Missionaries" problem in Racket,
and was happy to see a lot of how I was working looked almost identical in
Racket, with the additional benefits of a languages with a bigger standard
library and more support all around both in my editor and it's own supplied IDE
Dr. Racket.

And what I have found to be the curse of Lisp to be is; going back to Python.


## It's so hard to go back {#it-s-so-hard-to-go-back}

I am writing a generalized CSP solver that need to be able to tackle a few
different kinds of CSP problems and I am trying to build the same process of
steps I wrote in these two lisps in Python. Sadly, I have been spoiled. Maybe
it's partly my fault for thinking of the steps of this problem as lists, but I
feel like Python doesn't really support the way I am trying to solve this
problem.

At the same time, I wrote a little script for work the other day too. I needed
to do something complicated in an Excel file, and Pandas made more sense than
making a complicated spreadsheet formula. And Python was great for that. But by
the time I get out to something the size of a CSP solver, I think my naive
attempts at using Python like it was a lisp is starting to bump into Python's
philosophy that there should be preferably one way to do things. And I am
thinking my textbook's OO based system of classes and methods is the way that
Python WANTS me to solve this. That's all well and good, but seriously, why on
earth should I need methods attached to the data moving around a CSP solver? Why
can't I model the state of the problem as a data structure that I just pass
through a series of functions? It feels like Python isn't making it impossible,
but it's not giving me much help either.


## What am I really trying to learn? {#what-am-i-really-trying-to-learn}

I was talking to a co-worker the other day and they asked me, "What are you
learning programming for?". I thought for a bit, and while I do hope to be able
to do this professionally, I don't think I would enjoy working on a code base
that looked like the code in my textbook. I want to be able to write code that
looks more like the Lisp I have been writing.

So I was toying with the idea of adding Common lisp to my set of languages.. but
I am already kind of spreading my self a bit thin. So I wanted a way to sort of
reduce the languages I am learning while also focusing more on Lisps in general.
And that is what leaves me thinking I actually should keep with Racket for the
time being.


## The niche Racket fills {#the-niche-racket-fills}

So I still think Clojure makes sense for a CPU hungry program that can utilize
the power of the JVM. I think LFE (and Elixir) are great for a distributed
system, or a situation where speed and efficiency are not as important as
reliability and robustness. Common Lisp would be another language that is
powerfully, and able to reach deep into how the program is running do crazy
things like give me a REPL at a place in the call stack to debug what is going
on. But at the moment, I don't need to do that either. I would rather a platform
that is light, that boots quickly, that let's me write these small programs in a
fairly pain-free way as I write this stuff in the evenings after my other Job.

So Racket stands to be a good middle ground between how quickly and easily I
could get something done with a small Python script vs the power that a
industry-ready lisp like Clojure is. I don't need the power of the JVM to do
homework problems. I don't need distributed computing to compare rows in a Excel
file. And something tells me Racket is going to be a nicer way to do some of
this than reaching all the way back into Python to use Hy.

So let me try to list these out again (a list that seems to change as quickly as
the weather... haha)

1.  Racket
2.  LFE
3.  Clojure
4.  Hy

I am not giving up on Hy. And I think I can get away with writing most of
what I do in Python in Hy. But I think Racket is a better place to place my
focus. Partly because it is also going to be a great place to learn the rest of
the programming I need to get through in this textbook, and also because all
these Lisps are not so different from each other. Progress in one will pretty
readily translate to the others. So if I can get these under my belt that will
mean I can write code that is at home on these platforms:

-   Chez scheme (very easy to embed form what I hear)
-   Erlang virtual machine (OTP is open source, and a good target for distributed systems)
-   The JVM (arguably the fastest VM in this list)
-   Node/Ecmascript (not as big a priority for me right now)
-   Python (where I have the most practical experience)

Let's give Racket another shot and see where this takes me.
