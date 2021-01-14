+++
title = "Version control"
author = ["Robert Clay"]
date = 2021-01-17
lastmod = 2021-01-14T22:00:55+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-01-17 Sun]</span></span>,#git


## What is version control? {#what-is-version-control}

There are lots of pieces of software that work this way now, but it's rare
enough that I feel a few words on it might help those less familiar with it. I am
talking about the ability to save your work and not worry about it, knowing you
can always get what you just saved some day if you really need to. Some software
calls it backups, some software calls it states, I like the way git calls it.

Imagine you are writing a really simple book. Let's call it "My book".

-   My-book.txt

Great. Now you write a section. Let's call it A.

-   My-book.txt
    -   A

Once you save your work, you have lost the blank version of My\_book.txt. You
only have one current and correct version of My\_book.txt. In most cases this is
fine. But it can be really nice to have multiple versions of the same document.
Let's say this is a story and in A the main character learn to fly. So in B you
want to have him fly somewhere; B.

-   My-book.txt
    -   A
    -   B

Hmn... no that's no good. B is ****SUPER**** interesting. He flew to the moon.
Let's make him a pilot. Let's change A to "intro".

-   My-book.txt
    -   Intro
    -   B

Now if you don't work with versions you might be tempted to make something like
the following:

-   My-book\_old.txt
    -   A
    -   B

-   My-book\_new.txt
    -   Intro
    -   B

Now you have two files. Once has "A", the other has "intro". If you don't keep
these two files you stand to loose "A". What if you didn't like A yesterday,
but you want to bring A back tomorrow? What if you already hit save on
My-book.txt after you deleted A? What do you do now? Well if you have an "old"
and "new" version, you still have A, but now you have another problem. You have
two files to keep track of, and know what to do with these words can get kind of
confusing when you open you folder with 50 files and open up
"My-book-with-the-cool-ending.txt" to see if this is the one you were looking for.


## There has to be a better way {#there-has-to-be-a-better-way}

..and there is. It's called version control. If the software you have supports
it, please use it. It's really nice. And if you are into code, use git. Git is
hard and complicated, and frustrating, and so so worth it.

I didn't set out learning git because I wanted to learn to code. I set out to
learn git because I wanted to learn what this "magit" thing built into spacemacs
was. But what I discovered was a revelation that makes Org mode and Emacs my
idea of an ideal text environment.

Git is very complicated software, but on the surface you can say it works be
recording the changes made to a file rather than saving copies every time you hit
save. By only saving he changes since the files was saved last, you can keep all
those changes in order and go back to any of those "save points" without needing
to make lots and lots of copies of the same information.

So while a traditional file might look like this

-   save-1:  A,
-   save-2:  A,B,
-   save-3:  A,B,C
-   save-4:  A,B,C,D

git would store it as something more like:

-   save-1:  A
-   save-2:    B
-   save-3:      C
-   save-4:        D

And if you were to ask git for the current state of your file, it would give you
the culmination of all four saves, or A,B,C, and D. But if you asked for save\_2,
you could just be handed A and B. Pretty cool. The only trouble is git is ****SO****
flexible, it can be really hard to wrap you head around.


## You want me to "push" to a "remote"? {#you-want-me-to-push-to-a-remote}

Git terminology drove me nuts the first few months I started using it. I had no
idea what it all meant, and running git commands in the terminal made it all
very frustrating. But after I started using it from Emacs using Magit, I found
it much more approachable. And git "saved my behind" the other day.

I keep my work related notes in a running document where I track things I need
to remember. The other day I went to go look up some information in a line of
this several thousand line long text document. Unfortunately that line no longer
existed. The information I had kept in the document had been accidentally
deleted. It was gone, the file had been saved. But I had the file under version
control.

I just pulled up the git repository where all my previous versions of th file
were, and started going through older and older versions till I found one where
the data hadn't been deleted yet. Turns out I ended up needing to go back a
month worth of versions before I found it, but after copying that text back into
the most recent version of the doc, I was back in business. It's like I had
never lost it.

So if you have an easy way to use version control, I highly recommend it. If you
are interested in version control for the extremely patient, consider learning
git in the terminal. And if you get tired of that, try Emacs and Magit. I feels
now like I haven't really "saved" my work if it's not committed to at least some
branch in git.
