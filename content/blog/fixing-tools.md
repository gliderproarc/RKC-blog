+++
title = "Fixing tools"
author = ["Robert Clay"]
date = 2021-03-07
lastmod = 2021-03-08T08:43:19+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-03-07 Sun]</span></span>,#emacs


## Tools are only as useful if they work the way you need them to {#tools-are-only-as-useful-if-they-work-the-way-you-need-them-to}

Just yesterday I went to work on some Clojure code and practice some syntax I
had just heard about, and I got an error. It wasn't a problem with my code. The
code was fine. The problem was with my tool. The problem lied somewhere is the
line of:

-   Windows

~~+ WSL2
++~~ Pengwin
~~++~~ Emacs
~~~~+~~~~ Org-mode configuration
~~++~~ Java
~~~~+~~~~ Java configuration
~~++~~ Clojure
~~~~+~~~~ Project configuration


## My Tools tend to give me issues like this quite a bit {#my-tools-tend-to-give-me-issues-like-this-quite-a-bit}

It's mostly due to the fact I like to use tools that are pretty cutting edge.
Take Emacs. It might be old, but it's changing. I saw updates to packages that
make up Emacs just a few weeks ago. All those changes invariably make for a
problem for someone at some point down the line.

Take a Violin by comparison. Your Violin might break a string, or need some bow
wax, but you don't get too many problems with things like the number of strings
changing on you. Which means you only need to worry about a few things and can
mostly rely on your tool to work the way you expect it to.


## Back to my broken Clojure code block {#back-to-my-broken-clojure-code-block}

So in the past I solved problems like this by wiping the WSL install and trying
again. I know a little bit about Linux, but if something is wrong I have
resorted to starting over more often than digging into things to fix them. But
over the past year I have been slowly learning more and more about how the
different parts of my tools work. I have searched the internet for people
encountering similar problems before, but sadly the world of people who want to
use Org mode, and CLojure, and Literate programming are pretty few and far
between. I knew I was going to be mostly figuring this out on my own.

And this brings me to the things I really wanted to say with this post:

****A tool can be valued not just in what it can do, but how easy it is to fix.****

I did some digging, and I found that the files I was calling there Clojure code
blocks from had accidentally told Clojure that my home folder was a project
folder. After cleaning out the files it had made, it returned to working
normally. Thank goodness the files were somewhere I could get at them. And thank
goodness I knew what they were before I deleted them.


## I wish more of my tools worked like this {#i-wish-more-of-my-tools-worked-like-this}

Yes, it can be a paid to go about fixing a tool, or not being able to do the
things you wanted to with a tool because its not working. But at the same time,
if you choose tools that you know, and know so well that you can fix them, you
can minimize the risk of that hiccup throwing your whole flow our of wack.

-   note: For those interested, this is the bit of code I was learning about and
    trying to run. Fun stuff.

<!--listend-->

<a id="code-snippet--Thread last"></a>
```clojure
(->> (range 1 10)
     (map inc)
     (remove odd?))
```
