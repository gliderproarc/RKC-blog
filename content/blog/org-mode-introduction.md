+++
title = "Org mode introduction"
author = ["Robert Clay"]
date = 2020-12-17
lastmod = 2024-08-14T08:52:56+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2020-12-17 Thu]</span></span>,#Org-mode

  This topic deserves more than a post or two, but it's a nice short introduction to
what it is and how it works might help you understand why I have come to rely
on Org mode for most of my note taking and task tracking needs.

<https://orgmode.org/manual/>

  Let me start with why I went looking for and found Org mode. I was making
really complicated spreadsheets at work. I was trying to program in a
spreadsheet, and even convinced my company to get adopt a no-code tool. It was
great. Lots of the power I wanted from a program but with the flexibility of a
spreadsheet. I was so happy using it, I wondered it if might be nice to try
and use it for my personal data management, and then I ran into a problem


## It cost a monthly subscription fee {#it-cost-a-monthly-subscription-fee}

Not that a monthly fee is all bad. The excellent company who made the
software need to make money too. But I could not afford to be paying a
monthly fee for software that I could do more or less with what I
already had. I was much more interested in spending money on music
software.

So I went online and started looking for software. I found a few text
editors that did some of what I wanted, I tired Atom and thought it was
pretty cool. But what I really wanted was something that would:

-   Tie in data in a spreadsheet with my words in my notes
-   Help me make notes, tasks, and track appointments without needing to use
    something like Google calendars
-   Approach code in terms of flexibility and let me make tools for what ever
    else I wanted it to do for me.


## I don't remember the forum where someone suggested Org-mode, but I will forever be grateful for the advice I got {#i-don-t-remember-the-forum-where-someone-suggested-org-mode-but-i-will-forever-be-grateful-for-the-advice-i-got}

I was warned that Org was hard to get set up, but that once you had it
working it would do all those things I was looking to do and more.

So let me get into what Org mode is. It's a "mode" for a  text editor
called Emacs, and it's a markup language that has a few extra
functionalities. Once of them is tables. While HTML tables are notoriously
hard to type, format, and work with, Org mode makes them very easy and even
provides most of what you would expect from a basic spreadsheet
application... with one ****very**** big difference. Org mode also provides
facilities for literate programming, meaning you can have cells in you
spreadsheet that don't have to use the less than ideal "language" of
spreadsheet formulas. You can write a Python function and have the result
fill out into a column in your table. Something like this:

```text
  #+TBLNAME: data_for_testing
  | number | Python |
  |--------+--------|
  |      1 |      2 |
  |      2 |      3 |
  |      3 |      4 |
  |      4 |      5 |
  #+TBLFM: $1='(org-sbe "Add_1_to_me" (num $1))

#+name:Add_1_to_me
#+begin_src python :python python3 :var num=1
return(num+1)
#+end_src
```

Now any spreadsheet can add a number to the next cell's value, but the fact
it can be written in a programming language as simple and powerful as
python is one of the things that keeps me from looking anywhere else to do
this sort of thing.

I'll touch on the way the Python code is represented there later. Let me
keep going on what I originally needed Org to do for me. I also wanted a
way to write and keep notes. I had used Atom basic .md files, but Org did
more than just give me a way to write notes. Because it is implemented in a
Lisp interpreter, there are many things you can ask code to do for you
based on what you write in your notes. Things like a special syntax to make
something a "task" or a special syntax to make things a date which can be
recognized else where to place notes and tasks relative to each other like
a planner, it's really quite amazing how many things are in this software.
And what really struck me was that fact it was basically all plain text
and lisp code.

I've mentioned lisp and code a few times, and while my intention was not to
learn how to write code when I started using Org mode, I decided to try a
little bit here and there and found that it wasn't as bad as the last time
I had tried my hand at coding, and the "literate programming" style of
writing prose with bits of code interspersed around the file was really
nice. So I am teaching my slef a few languages, and one of them is elisp.

```text
    #+name:example-code
    #+begin_src elisp
(cdr '(a b c d))
    #+end_src

    #+RESULTS: exmaple-code
    | b | c | d |
```

I won't bore you with a lisp tutorial, but suffice to say Org mode has made
writing little bits of code that work together with words really easy. And
surprisingly, you can mix languages. Because these blocks of code are
independent in your document, you can define what they "see" from each other
and string them together into a program with several languages in it.

My short introduction here hardly does the program justice, but if you want
to know more, the link above can take you to the Org mode manual, which will
tell most of what there is to know about it. If you are willing to learn how
to use Emacs, Org mode is an amazing tool that made Emacs worth it for me.
And after a while I started to find just how interesting Emacs it's self is
too, but that is a topic for another day.
