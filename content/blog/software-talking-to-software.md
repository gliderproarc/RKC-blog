+++
title = "Software talking to software"
author = ["Robert Clay"]
date = 2020-12-27
lastmod = 2020-12-27T10:41:20+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2020-12-27 Sun]</span></span>,#software
This post is going to be a little less focused than other posts on the same
subject, but I feel I have a unique perspective to share from someone who is
just getting into this space. Sometimes it's hard to see further down the rabbit
hole to see how far down it goes, and it can be hard to see above you and how far
down you have come. A lucid moment to reflect on where you are can be nice not
only to redirect yourself, but maybe also to help others decide if this rabbit
hole they are heading down is really worth it.


## A long chain of software {#a-long-chain-of-software}

I am a computer musician. I used to think of the synthesizer as my instrument of
choice, but after using a few real hardware synthesizers I realized that I am
more interested in what computers afford me as far as sound possibilities and
music structure manipulation goes. As a computer musician I have played with and
used a variety of software over the years, but find myself constantly
gravitating to the software that is the most extensible. I was a big Logic Pro
user for many years, and I was very happy to have the complicated (but powerful)
"environment" available to me if I needed Logic to behave in a way that wasn't
the standard that most users expected.

Eventually I moved to Ableton Live, and the user experience is not so far
removed from Logic (they are both modern and capable DAWS), but Live provides me
with an API. There is a similar (but far less extensive API) connection in Logic
now that lets you write Javascript to control Midi information, but Live decided
to open up their software to "talk" to a program called MaxMSP made by cycling
'74. Having recently discovered how nice it is to work with text, I also found a
way to "talk" to MaxMSP via Node. And since I don't particularly want to learn
Javascript, I found a way to write node application in a language I DO want to
learn, Clojurescript. The resulting string of connections looks like so:

|   | Software      | functionality            |
|---|---------------|--------------------------|
| 1 | Live          | Music creation           |
| 2 | MaxMSP        | Visual programming       |
| 3 | Node          | Javascript Runtime       |
| 4 | Clojurescript | Functional LISP language |
| 5 | Emacs         | Text editor              |


## Why all this complexity? {#why-all-this-complexity}

Most people are happy to simply make music in Live, or write code in a text
editor. Why go through the trouble of connecting the two? In my case, it's
because I like to use my tools for more than one purpose. If I am going to go
out of my way to learn something, I want it to be useful for more than just one
thing. Knowing how to use a computer is useful for more than just one thing. I
can use lots of other tools better by knowing how to use a computer. But if I
were to lean how to use a platform like say... Evernote, I would need to learn
how it works for basically only one thing, making and manipulating Evernote
files. Evernote can do all kinds of things, but it's a lot more closed off to
integrating with other tools than say the way a sound file made in your audio
recorder app could plug into any other piece of software that can read standard
audio file formats. Evernote files are basically only useful to Evernote.

These bits of software all provide for a way to work with them from the outside.
This means I can turn to external solutions if the tool at hand can't handle it.
If I have a bit of midi information in Live that I want to say... change based
on the number of files in a folder, I can tell Live to ask Max. Max can take the
bit of Midi and handle the request, but it's not very good at working with the
file system. Thankfully Node can talk to my computer's file system just fine, so
I use Emacs to write some Clojurescript that tells Node how to tell Max how
many files are present so Live can give me the result I was looking for. Could I
have done this without all this work? Sure. I can count files. I can give Live a
number and have it give me my sound. But I can't be bothered to do that several
hundred times in a row.


## Is it worth it? {#is-it-worth-it}

The million dollar question to be sure. Just because it's possible to make all
these things talk together doesn't make it a good idea. Just because a piece of
music can be influenced by the number of files in a folder doesn't mean it will
make for good music. But in my case there is another reason for wanting to
connect all these tools together.

-   All these tools I would use on their own for their own use cases whether they
    could talk to each other or not.
-   Learning each tool on their own not only benefits my use of that tool, but
    also makes it easier to pass that along to the rest of the chain.
-   The ends of the chain make things I have more than one use for. Being able to
    connect them makes spending time at either end that much more useful to the
    opposite end.

Code is useless if it doesn't do something useful. And if the code I learn to
make for work can benefit my music making, I want to see where that leads me.
The music I make in Ableton Live might be fun to make, but it's also my way of
giving my music back through my volunteering at church. Having a direction to go
with my code, having a useful thing to do with my code besides work makes it
that much easier to find the energy on my days off, on my own time, to learn a
lot of complicated ...stuff.


## Software talking to software is very powerful {#software-talking-to-software-is-very-powerful}

Having used computers for the majority of my schooling and all thought out my
still evolving professional career, I see how the line between people talking to
software and software talking to software is a space I wish I had learned more
about sooner. I spent many many hours learning how to use software as an
end-user. That was fun, but user interfaces change, and eventually all that work
can end up being lost time if that software no longer exists, or doesn't run on
your current system. But once you take yourself out of the equation and get
software talking to software, you get something really special.

I had an issue at work. I needed to look at a bunch of Json data all at once not
because I had a program to write, but because a service we use at work will
only give me Json files. I was using Emacs to look at the files (which was a lot
better than using notepad) but I ended up saving my self the most time once I
taught a piece of software to do it for me. I still need to connect the Json to
the software I wrote, but the result is a LOT of simple tasks done over and over
in a way that means I only need to download some files, press a few buttons and
wait a few seconds.

There was a situation I had playing music at church one day. I only had one
sustain pedal for my keyboard, and I needed another one. The church service was
starting in 45 min, and I needed to figure out what to do with what I had. So I
coded one in MaxMSP. It was crude, it was fickle, but it got me through the
church service. Being able to tell software how to behave like a sustain pedal
and having it do that for me was invaluable in that moment. But if I had only
ever gone as far as being a end-user of software like Ableton Live, I would have
been stuck.


## ...as long as you can manage the complexity {#dot-dot-dot-as-long-as-you-can-manage-the-complexity}

Yes, these tools are great, and I like them partly for the fact that they talk
to each other so well. But I do pay for it; in complexity. These tools are not
simple, and the interfaces that they use to talk to each other have each
frustrated me to no end in their own way. But to me I feel it's worth it.
Because I can deal with the complexity given enough time. I don't need this
music for my work. I don't even need to use code at work. But both happened to be
things I enjoy learning about and using. So while I wouldn't say the average
user should go out and try to connect all their tools to each other, the synergy
that results can be really exciting. Just be careful which tools you try to
connect. Nothing against JavaScript, but there is a reason I decided to talk to
Node with Clojurescript and not JavaScript.
