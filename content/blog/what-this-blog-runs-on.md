+++
title = "What this Blog runs on"
author = ["Robert Clay"]
date = 2020-12-16
lastmod = 2022-09-23T08:27:26+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2020-12-16 Wed]</span></span>, #Emacs
This blog looks very simple on the surface, but what it is built on is
something I am particularly happy with, and it will introduce a few themes
and topics that I will write about more in the future.

Here is the loose chain of software and tech between my posts and the
internet:

-   Emacs and org-mode
-   ox-hugo
-   Hugo static site generation
-   .git file for version control
-   Hosting of that .git file on Github
-   Github api calls to Netlify that runs a CI routine to build the site push
    it to the web.

    The fact I was just learning what Emacs was a year ago still makes me wish
    I had tried to learn all of this sooner. The number of powerful tools out
    there for people willing to learn them is incredible. And if I had learned
    how to use all this sooner, I wonder what I might have made when I was
    younger with more time on my hands.. lol.

    Just Emacs and Git have been a journey to learn, but now I have so much
    respect for what they can do as tools and how they let me do my work. And
    of all the things I could say about them I think I am most interested in
    talking about text files.


## Text files? {#text-files}

Yeah, text files. You know, on your computer when you have a file that ends
in .txt. That is a text files. Text files are awesome. I didn't think they
were all that interesting until I learned what happened to files on a
computer that are 10+ years old.

I had a few laptops over the years, and I had never really given back-ups
much thought because I am (was?) an Apple guy. I just turned on time-machine and
called it a day. But these days when I try to get at ****really**** old files,
I find a lot of those files don't open anymore. The data is there, but I
can't use the program that made it. So even though I backed it up, the
backup is useless. I still can't get at what I made. But do you know what I
can still open? I had a diary app that let me do an export of my entire
list of entries as an .rtf or rich text file. These files I can open, and
they read just fine. That is because the .rtf file format is a widely
adopted standard that lots of program can read and write to. But all my
program that stored their information in proprietary formats are mostly
useless now.

So when I got to thinking about making this blog, I decided to make it here
with a Hugo back-end. Hugo is a static site generation frame work built on
Go, and while I don't know enough Go to be able to build it my self, have
access to most the inner working of this site is really quite fun and
interesting. To make a post, I just make a mark-down file, put it in the
right spot in my file structure and I have a new blog post. I'll talk about
Git and Emacs another day, but Org mode deserves some special mention.


## Org mode {#org-mode}

Org mode is it's own markup language specific to Emacs and has a lot of
support built into it for the lisp code (or elisp rather) it is built with.
I have had to learn a bit of lisp, but as far as programming languages go I
think it's not nearly as troublesome as languages like Javascript, but I
digress. Suffice to say Org is a markup language, but at the end of the day
it's also just text files. Meaning even if I needed to move away from Emacs
and Org mode one day, all the words in my blog and notes will all be just a
bunch of copy and paste of text to move somewhere else.

---
I would not recommend this platform to everyone. The amount of reading I had
to do to get it up and running was pretty substantial. And if you are
thinking of making a blog I am sure tools and platforms like Word-press are
much more approachable. But I really like what Hugo and Netlify and Emacs
have afforded me here. I save an Org file and commit to a Git repository and
I have posted a blog post. To me... that is the kind of powerful simplicity
I want to use.