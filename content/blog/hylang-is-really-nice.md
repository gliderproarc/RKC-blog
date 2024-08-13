+++
title = "Hylang is really nice"
author = ["Robert Clay"]
date = 2021-09-20
lastmod = 2024-08-14T08:34:03+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-09-20 Mon]</span></span>,#hylang


## Took a break from blogging {#took-a-break-from-blogging}

It's been a while since I have posted, but the summer gets rather busy at
my current workplace and I have been playing catch-up with a bunch of
stuff. Reason Studios (formerly Propellerhead software) released Reason 12,
and I have been very happily learning all about the new devices and playing
with Reason sounds as a VST. I hope to not just blog about that soon, but
also finish some music with it and show what has me so excited about that.

But today's post is not about Reason, it's about Hy. And the reason being I
have been learning more about Python and functional programming and I am
starting to see what makes Hy so cool.


## Hy can look and work A LOT like vanilla Python {#hy-can-look-and-work-a-lot-like-vanilla-python}

Consider the following:

<a id="code-snippet--Two-sum"></a>
```python
from itertools import combinations

problem_list = [0, 9, 2, 32, 4, 52, 3, 7]
problem_target = 6
my_gen = combinations(problem_list, 2)
current = next(my_gen)

while sum(current) != problem_target:
    current = next(my_gen)

print(list([problem_list.index(current[0]), problem_list.index(current[1])]))
```

And this:

<a id="code-snippet--two-sum-hy"></a>
```hy
(setv problem-list [0 9 2 32 4 52 3 7])
(setv problem-target 6)
(setv hy-gen (combinations problem-list 2))
(setv current (next hy-gen))

(while (!= (sum current) problem-target)
  (setv current (next hy-gen)))

(print [(.index problem-list (first current)) (.index problem-list (nth current 1))])
```

So it's not exactly the same. The second bit of code sure has a lot pore
parenthesis. But the way the code in each does the work is REALLY close. And for
those who don't recognize, this is an attempt I made at a Leet code problem
where you need to return the indecies of the two numbers in the list that add up
to the "target". The way I solved it was not efficient at all. This is about as
"brute force" as you can get. I just guess and check and stop when I get the
answer. But the problem was simple enough that I decided to do it in two
languages, and I was really surprised at how easy it was to take something I was
doing in Python and just write that out in a Lisp.


## Why would you want to do this? {#why-would-you-want-to-do-this}

I found a blog post online by this gentleman who was talking about CLojure
and Python. CLojure is still something I poke at, but can't really get my
head around the environment. I have always found Python to be pretty simple
to get running, and I found the comparison between the two to be very well
done. Clojure makes concurrent code easy and provides a very nice standard
library for writing functional code without needing to be like Haskel.
Python is a dynamic language that can look pretty function, and is very
quick to write, while tending to not be as speedy when running (compared
with things on the JVM).

Hy lets me use a lot of things that look A LOT like Clojure without
actually needing to run a JVM. And yes, I tried Clojurescript and Node was
not making things that much easier. I still want to get ClojureScript under
my belt for working with MaxMSP, but Hy is proving to be something that my
head has a very time getting a grasp on... despite the parenthesis.

The solution to the Leet Code problem I cam up with was not particularly
functional. Lots of variable assignment, and a less than ideal while loop.
But it showed me that if I needed to, I could use Hy to write Lisp that was
not so functional and easier to use along side other code that was written
in more OO or procedural style.
