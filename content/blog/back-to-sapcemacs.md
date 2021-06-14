+++
title = "Back to Spacemacs"
author = ["Robert Clay"]
date = 2021-06-14T11:05:00+09:00
lastmod = 2021-06-14T11:12:34+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-06-14 Mon]</span></span>,#emacs


## Doom is still really nice for what it does. {#doom-is-still-really-nice-for-what-it-does-dot}

I needed to start this off with that, because I feel like I really did like
Doom when I was using it. But it was in a strange sort of way even more
closed off to me changing how it worked than Spacemacs. People are right
when they say Spacemacs has more layers of stuff between you and Emacs.
But I have had a lot of success with customizing it from the use
configuration section of the .init.el file. However, I found Doom to be
less cooperative when it came to one important area: Evil.

Love it or hate it, Evil is a big part of Doom Emacs. It is really hard to
fully turn off, and for the most part I don't mind Evil as long as it will
step aside when I need to "talk to Emacs" more directly. In Spacemacs there
is a handy option to turn the vim insert mode into Emacs mode, or allow
nearly all the Emacs bindings when inserting text. It feels really seamless
to me and I can't really go back to the normal insert mode. I also don't
like giving up visual mode for editing text which I find Emacs to be less
comfortable when compared with things lie [ d d ] for deleting a whole
line.

So what really made me switch back to Spacemacs?

1.  [leader o a t] broke
    I am a heavy org-mode user. More so than a coder. I use Emacs for
    Org-mode and occasionally code. To have the list of all tasks that are
    open in my agenda files not working was hard to deal with. I need to be
    able to see those. I tried a few things to fix it, but it appeared to be
    a package update that broke it. I didn't see other people on the net
    complaining about it so I assumed it was just the right combination of
    packages, the "perfect storm" that caused it to break on my machine. I
    watched (heard?) an interview with the maker of Doom Emacs and he was
    talking about managing packages and which packages made it into Doom a
    big part of what was taking up his time. So rather then go online and
    ask someone to fix it, I just switch back to Spacemacs.

2.  I didn't mind the boot time that much
    After spending time in Doom where things are WICKED fast, I thought I
    would miss the quick start times. But like a lot of Emacs users, I don't
    boot the software many times a day. Once is usually enough. And there
    were always packages in Spacemacs I wanted in Doom that I could never
    exactly fine or replicate in behavior. Take completion. I can start
    typing a file path in an orgmode file and get completion for file paths
    on my system. That never "just worked" in Doom. And I do lost of my work
    with Org and babel blocks. I need to define where files are on my system
    for the programs to work.

3.  "Holy mode"
    When I first started using Emacs, I remember finding Spacemacs and the
    tagline, "The best editor is not Vim or Emacs. It's Vim AND Emacs". And
    I must say I find it really nice to just have my mind working in Emacs
    bindings while inputting, and then switch it off to visual mode when I
    hit escape.


## Spacemacs has it's issues too {#spacemacs-has-it-s-issues-too}

I was looking back over my notes while getting Spacemacs up and running the
first time last year, and I was kind of laughing to myself as I remember
all the frustration of learning how to re-compile all the elpa .elc files.
And the boot time is quite long. But I have weighed the costs, and I am
back to Spacemacs. And I think it's where I will stay for a good while.

In closing, here is random Org-table formula I made:

```text
   | Name(val)  | val   |
   |------------+-------|
   | Bill(big)  | big   |
   | Ann(tall)  | tall  |
   | Tom(short) | short |
#+TBLFM: $2='(substring (car(cdr(split-string $1 "(")))0 -1)
```

So what is this? it's a handy org-table you can use to do all sorts of things.
String manipulation is possible in things like Google spreadsheets and Excel,
but neither of them approach what the table above is doing. You can make
formulas that do exactly what this does in other spreadsheets, but this is so
simple and clean. You could copy any list of text separated by newlines and
re-format them table, run one function and get it all calculated in one go.

The Elisp function below the table does this: "Take a substring that is the
(first of the second item in a list) and from the first parenthesis to the
second to last character of the string.

If you have different delimiters, you can just edit the code to match, and if
you need some validation before you run the extraction, you could add a 3rd
column that checks if the text can be processed before being passed to the
sub-string function. I hope you find it useful someday.
