+++
title = """
  A "forced technologist"
  """
author = ["Robert Clay"]
date = 2021-04-11
lastmod = 2022-09-23T08:28:04+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-04-11 Sun]</span></span>,#coding


## You know you aren't a coder when... {#you-know-you-aren-t-a-coder-when-dot-dot-dot}

...you give up on a perfectly good languages because it doesn't work with
Org-babel code blocks the way you want it to. Does that sound like you? Maybe
not, and lots of people like Clojure just fine. I still think it is a great
language that I would love to use more one day once the tooling catches up with
what I want to do. I did get REALLY close to what I wanted, but Clojurescript,
node, and other factors are making it hard to keep at Clojure. I think what
really made me decide to shift my focus away from Clojure was the realization I
was spending more time figuring out the tooling than I was programming. And
without any projects written in Clojure, I have very little to get me to stick
with the languages.


## Python is a better fit {#python-is-a-better-fit}

Python is not perfect. The fact I am having so much fun in a language like Hy is
a testament to the fact I didn't really need Clojure. I don't feel the need to
write purely functional code, reach into the JVM or Javascript worlds, or live
in the Clojure repl. I mostly make things with Org-babel blocks, and Python has
been serving me well. I have two tools written in Python and some bash that help
me get my day job done even though I am not a coder. And I could have written
these in Clojure. But I wrote them in Python. And the reason I made them in
Python is simply because Python was easier.

I don't need fast code. In fact, I have been teaching my self about functional
programming and writting things without loops (which can often be the faster
way of dealing with iteration). And Hy is not about speed either. I am mostly
writting small scripts. A performance hit only costs me a few seconds most runs.
Maybe one day I will need code that is fast.


## And I hear there are options for fast Python {#and-i-hear-there-are-options-for-fast-python}

I have recently been hearing about things like Cython, Numba, and just the
simple change of moving computation heavy math in Python to NumPy and how it can
help speed up code that would other wise be slow in vanilla Python. But what is
good about these tools is it's mostly still python. How nice to keep most of the
flexibility I have learned to enjoy, and just contrain myself to some performant
stuff when I know I am going to need it. And all the while getting to stick with
a single language. Plus I get to use the one library that seems to creep up here
and there: Pandas. So long as most of my work at work is given to me, and
expected of me in tabular data, Pandas is a great way for me to start harnessing
the power of code to not write as many cells in a google spreadsheet.


## So long and thanks for all the fish {#so-long-and-thanks-for-all-the-fish}

It's not good-bye to Clojure. I do expect I might be able to get it working with
Org-babel once I get homebrew and Planck on a Mac to work, but this is so long
for now. I think after about a year of learning Python and trying to add
another language because I think I need something fast, I think exploring
options like Numba are a nice intermediate step, and probably as far as I need
to go.

Expect a blog post or two about Numba over the next month or so. If it turns out
I can just write a block in Org babel with a @jit decorator and call that block
from Hylang blocks with the rest of my code... I am going to be pretty stoked. I
am not a technologist because I like technology, it's more like I see a problem,
and the best way I know how to solve it requires a little bit of Python. So if
Python is all I need, maybe I will leave Clojure to the lispers and stick to
Hy.