+++
title = "Doom Emacs"
author = ["Robert Clay"]
date = 2021-03-14
lastmod = 2021-09-20T09:20:13+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-03-14 Sun]</span></span>,#emacs


## Emacs configurations {#emacs-configurations}

It's crazy to think that it's been only just over a year that I have been using
Emacs. I found the software thanks to org-mode and searches on the net for a
option for notes with power beyond simple words or reliance on an external
company's server time. But I was warned when getting into Emacs that it was not
for the faint-of-heart. I knew Emacs was going to be the hardest part of getting
into org-mode, so I decided to use something to help me get up and running.
Rather than trying to add the learning curve of Emacs onto org-mode, I decided
to use Spacemacs.


## Spacemacs is REALLY nice {#spacemacs-is-really-nice}

[spacemacs](<https://www.spacemacs.org/>) is something I wrote about on this blog
before, so I won't go into it too much. Suffice to say it is a great "welcome"
into the world of Emacs for those coming from other software like Vim
(especially nice for people coming from Vim). There is also an episode in a
podcast called [EmacsCast](<https://emacscast.org/episode%5F4/>) that goes into the
differences between Emacs and what I really want to talk about today which is
Doom. Please take a listen to that episode of you want to hear from someone who
REALLY knows Emacs and not just a neophyte like myself.


## Doom Emacs is an unfortunate name in my opinion {#doom-emacs-is-an-unfortunate-name-in-my-opinion}

...but as a configuration it's really nice. I am not a fan of the game, and the
splash screen was not my favorite, but Emacs isn't a tool people pick because of
how it looks. I moved to Doom emacs for one reason: Speed.

Spacemacs is great. It can do so much. In fact, there are things I wish Doom
could do that I miss from Spacemacs. But Doom has the advantage of speed. It
loads wicked fast, and in that sense I do think the name is rather fitting. Doom
might not be the most pleasant place, but if you want to go brutally fast in
Emacs, Doom is a great place to start.

I am not quite ready to roll my own Emacs configuration from vanilla Emacs just
yet. But until I am, Doom is a really nice way to keep Emacs simpler while also
affording me much snappier responce overall than what I was getting from
Spacemacs.

Doom and Spacemacs do a lot of the same things. Doom is harder to learn and
there are fewer places you can go to get help. But you DO have the advantage of
being able to use more general Emacs knowledge to help you get things working.
Spacemacs I found to be so far abstracted from vanilla Emacs that I didn't
bother reading too much about how other people configured Emacs. I focused my
reading online to people working with Spacemacs. But with Doom, I find things
online, and they fit into my Doom configuration much more readily.


## To be honest, I like the Spacemacs bindings better {#to-be-honest-i-like-the-spacemacs-bindings-better}

Doom doesn't have bad default keybindings. I just like Spacemacs' bindings
better. What was one I was using all the time before? Oh yeah, [spc f j]. To me
that makes all the sense in the world. I want to work with FILES and JUMP to
another file with dired mode, so I hit my leader key and the two mnemonics to get
there. I was really comfortable getting from place to place and getting at
functionality I wanted in spacemacs. Things just took a bit to load after I
asked for something. And when something didn't work, I resigned myself to
needing to wait till the development branch pushed a fix before I would get it
working again.

In Doom it's [spc .], which is just harder to remember. I need to know that if I
want dired, I hit leader and period. Why? Because that's the doom binding. Could
I re-map it? Sure, but that's a lot of work and I am kind of fighting against
the whole point of a configuration like Doom. I am using Dooom because I trust
Henrick. If I thought I knew better I would make my own configuration. And until
I learn enough to make anything like this, I would rather learn why he thinks
[spc .] is better. And I bet you anything it's because it's faster. And it is.
It's just speed at the cost of the mnemonic logic in Spacemacs.


## If you want a fast Emacs configuration and don't mind Spacemacs, try Doom {#if-you-want-a-fast-emacs-configuration-and-don-t-mind-spacemacs-try-doom}

If you are a vanilla Emacs user, you probably have a configuration that already
works for you. You can probably fix your config if it breaks, and like the
flexibility of a system you made. Doom might not be for you. If you are new to
Emacs and don't know what I am talking about, Doom might also not be for you. I
feel like Doom has a lot less hand-holding when compared with Spacemacs. But if
you are looking for a good Emacs configuration for using Evil-mode EVERYWHERE
you will most likely find something to like in Doom Emacs.

If you are not an Evil-mode kind of person, I found the Spacemacs support for
turning Evil mode off better. In fact, that is another something I miss from
Spacemacs. In Spacemacs, you can turn your Evil-insert-mode into Emacs-mode.
Meaning while inserting text you can call Emacs binding as if you were using
normal Emacs. But when you escape out if it, you are back in Evil-normal mode
and can edit and move text with Evil's wonderful navigation, selection, and the
fantastic leader key (space).

I hope Spacemacs learns how to speed up it's load times and maybe take advantage
of things like the new dumper being built into new versions of Emacs to cut down
on start up time. I might be tempted to go back.
