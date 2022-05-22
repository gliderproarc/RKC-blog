+++
title = "A look back at Racket"
author = ["Robert Clay"]
date = 2022-05-22
lastmod = 2022-05-22T16:50:04+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2022-05-22 Sun]</span></span>,#programming


## So I took a little journey while on my way back to Python {#so-i-took-a-little-journey-while-on-my-way-back-to-python}

Working through the practice problems in that programming textbook I bought has
given me a lot to think about.

<https://www.goodreads.com/book/show/42103309-classic-computer-science-problems-in-python>

Not only has it gotten me to really try and see what I can make code do, it also
made me search to see if I really was learning the right languages. I knew C and
C++ would be a nice tool to have in the bag because of how universal they are
and how Python in built on C, but I didn't really have a use for it at the
moment.

I took a few of the more fundamental problems and did a bit in C just to see how
fast it could be. And sure enough C is blazing fast. But I still have a really
hard time writing C.

Python the other hand has continued to be the easiest language for me to get the
things I want done in code running.


## So how about those other languages? {#so-how-about-those-other-languages}

Python is great, and I hope to make it Job in the not too distant future, but I
also know Python has a few places it doesn't work very well. One of them is
speed. If you need computation heavy number crunching, Python is not the way to
go. You end up needing to reach out to C and C++, or Numba or running stuff on a
GPU. Python is not known for being fast. Or multi-threaded.

So as I was going through the problems I decided to write some in different
languages to see how they were to work with. And as I was going through things,
I realized... I really like Lisp.

I haven't gotten into Macros just yet, but I do like how the parenthesis help to
keep the syntax really minimal. Python is also pretty minimal with syntax, and
Lisp just goes that extra step and makes just about everything a lisp and heads
and tails.

I'll write about Elixir and LFE later, because I actually intend to use them
more. But Racket was also on my radar for a bit, and it's certainly a nice Lisp.
I might even go so far as to say it sounds like it is the most lispy-lisp in use
these days, but it's also bound to not make as much sense as my other options at
the moment. Maybe one day Racket will change and it will make more sense for me
to learn and use more, but I am going to put it aside for the time being.


## Racket is great at what it does {#racket-is-great-at-what-it-does}

From what I have read, Racket is amazing at making DSLs. It's incredibly
flexible, it has recently (at the time of writing this) been moved to a Chez
scheme backend. And the libraries are very well done and cover a lot of ground

<https://racket-lang.org/>

It was also a very nice experience when compared to LFE which has very minimal
tooling and support in Emacs. Racket support if Emacs is also a but minimal, but
Dr. Racket was a very convenient place to de-bug and it helped me track down a
few mistakes I had made a long the way.

If I were to find my self on a project where I need a DSL, or to make DSLs, or
to make a DSL to write DSLs, Racket will be where I turn. But for the time
being, that is not actually what I want to do.


## Compared to Clojure {#compared-to-clojure}

Clojure is still on my radar of languages to learn. If I found myself on a Java
project and could squeeze in another package, writing Java is Clojure is bound
to be more bearable than writing straight Java


## Compared to Erlang {#compared-to-erlang}

Erlang strikes me as being kind on unique as having a great solution to the
distributed computing problem. In the age of cloud computing, having a system
that is built to run in many places all at the same time makes a lot of sense.
Erlang might be a fairly esoteric language these days, but Elixir has more
attention from the hip young kids, and it has Phoenix as their answer to how to
get on the web. And much to my delight there is also a Lisp built on the Erlang
VM. I hear there is another language called Gleam which brings static types. LFE
is even more esoteric than Erlang, but it's well maintained, and I managed a
small maze solver in it. Calling libraries from Erlang in LFE was really simple,
and it made working in LFE feel like what Hy feels like in Python.


## So where does that leave me? {#so-where-does-that-leave-me}

I am wrapping up the problems at the end of unit 3, but I am now slightly
refining the languages I focus to just:

-   Python / Hy
-   Elixir / LFE
-   Clojure / Clojurescript

I could throw another name up there, but really this is 6 languages and not 3.
So while I was shooting for 4, these will keep me plenty busy for a while. And I
think the all cover some nice territory. I am going to shy away from anything
too low-level like C or Rust, but I might end up needing to add one of those at
some point.