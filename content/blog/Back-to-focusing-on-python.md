+++
title = "Back to focusing on Python"
author = ["Robert Clay"]
date = 2022-08-21
lastmod = 2022-08-21T15:40:22+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2022-08-21 Sun]</span></span>,#programming


## Python is not perfect but it what I need to focus on for a bit {#python-is-not-perfect-but-it-what-i-need-to-focus-on-for-a-bit}

Wow, looks like the last post I put here was back in June. Time sure does fly
when you are... grinding LeetCode problems?

I was doing more problems in Elixir, and really liking the syntax and the
built-in functions. Not to mention all the Erlang stuff that can be called
for free too. But I also ran into a friend and as I was talking about coding
in Elixir, I realized that finding a job in Elixir is going to be... really
hard here in Japan.

I was reminded of this video I watched on Youtube the other day:
Why Elixir Matters: A Genealogy of Functional Programming
By: Osayame Gaius-Obaseki
<https://youtu.be/cWAHpvkh8Vs>

In the talk he recalls talking to a guy in coding boot camp who wants to get
a job. I might not be in coding boot camp, but I DO want a job doing this
one day. And I realized that I do love Elixir more than I enjoy writing in
Python. But if I am going to have any shot at landing any kind of job
writing code in the next few years, my chances of landing on my feet are
much better if I can write decent Python than if I were a master at Elixir.


## Why Elixir is so nice to write {#why-elixir-is-so-nice-to-write}

In previous posts I have mentioned LFE (Lisp Flavored Erlang). And it's
Erlang, but in Lisp syntax. And it's great. But Elixir has a few modern
affordances and a bigger community that make it that much easier to get
things done. Elixir has lazy sequences built in. LFE would make me roll my
own. Elixir has a Language server that works in Emacs and other
text-editors. I am lucky to get Syntax highlighting for LFE and luck out in
Emacs that Lisps in general get a lot of stuff for free. But what these two
languages have in common is something I really liked about Clojure,
immutable values bu default. The assumption is that you aren't going to
change things and use pure functions all over the place. And that's what I
want to do.

Python assumes you are going to be pragmatic. Maybe make a class or two,
maybe call map on a collection, and avoid needless mutation or raw loops.
But it won't support you trying to avoid mutating the way
Erlang/Elixir/LFE/Clojure do.

When I write Python, I feel like I am trying to bend it to be functional,
and find myself fighting against the Pythonic way till I give up and
side-step the Functional way and just get close enough. It's not wrong. The
code still gets the right answer. It just feels like I am fighting an uphill battle.


## But Python is getting used {#but-python-is-getting-used}

Another talk I watched recently was from CCP North:
Software Engineering Languages
By: Titus Winters at CppNorth 2022
<https://youtu.be/yA_wUiNuhSc>

Smart guy, works at Google, has so many more years under his belt doing this
stuff than me that it's not even funny. And when he talks about the world of
languages and what it getting used, Functional languages don't even get an
honorable mention in his talk. He talks about C++, Go, Python, and Rust.
Sure, there are other languages getting used in the world. Java isn't on
that list the the world of Java is massive. But to hear this guy who
obviously knows a thing or two and not hear him name drop a single
functional-first language, it made me pause.

Maybe I am getting ahead of myself a bit. Maybe I should try to get a job
first, then find a job that will let me code in a functional language.

So I am going to take a break from the Elixir book I bought, and head back
to learning some more Python. It's sure to come in handy one day, and it
remains just about the only language that is getting work done at my job now
(despite me not getting paid to code).