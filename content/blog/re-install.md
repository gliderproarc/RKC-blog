+++
title = "The nice feeling after a reinstall"
author = ["Robert Clay"]
date = 2021-03-28
lastmod = 2024-08-14T08:52:57+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-03-28 Sun]</span></span>,#WSL2


## No, I didn't reinstall Windows {#no-i-didn-t-reinstall-windows}

Windows is not something I want to think about ever needing to reinstall, but I
was starting to get some weird behavior from WSL2. I don't know what was causing
it, and I still don't, but I think a reinstall has helped. If you ise WSL2 and
have had:

1.  Random CPU spikes
2.  Problems when an exteral display is connected
3.  Slow Emacs boot times (haha)

    ...you might find a fresh install of your linux distro can help. Of course,
    reinstalling everything can be a lot of work. So I offer a brief looks at
    what things were easy, and what things proved to be a bit of a pain.


## Git is great {#git-is-great}

All my projects in Git were simple enough to clone back into the distro after
wiping the old one. Setting up some SSH keys got me authenticated, and a few git
commands later and my old files were back in place, including my Doom-emacs
configuration files.


## Nix is not so great {#nix-is-not-so-great}

Nix is supprisingly one of the most reliable ways I have found for installing
Emacs 27 on WSL. I need to install he dependencies for Vterm from apt, but Emacs
installs from Nix really well. I was hoping to also use Nix for Python, Java,
and CLojure tooling, but I ran into more than a few snags.

Python installed just fine, but getting packages was proving to be a pain. In
the end I just installed Python from apt and went with pyenv for virtual
environments. Nice intergation in Emacs too. Clojure wasn't finding the Java
pulled in when installing from Nix, so I ended up installing SDKman and running
the clojure installer script from their website.

I really want Nix to replace all my packaging needs. I am thinking abot heading
back to a Mac soon, and I would love to be using Nix for package management over
something like home-brew.


## Emacs was up and running pretty quickly {#emacs-was-up-and-running-pretty-quickly}

Some of the older things I use like skk mode for Japanese text entry gave me
some problems re-installing, but it didn't take that long. I am still ironing
out some road-bumps when it comes to upstream branches and maggit. Doom emacs
was easy to reinstall, and my config got me up back to my old setting very
nicely.


## Clearing out old unused software makes the whole thing "feel" faster {#clearing-out-old-unused-software-makes-the-whole-thing-feel-faster}

I haven't done any tests, but it feels faster. The load times on the Doom emacs
dashboard say my load times are faster, but I don't hold that a re-install
always make things faster. But I do think that it's nice to clear out old config
files that don't need to be there any more, and generally help you see what you
were really using.


## If you are scared to reinstall, something is wrong {#if-you-are-scared-to-reinstall-something-is-wrong}

Computers crash, software breaks. If something went critically wrong on your
computer, how hard woudl it be to get it working again? Have you gone through
the steps of what it would take to get everything back? Do you know you would
have evrything back?

It's like spring cleaning. It doesn't need to be everyday, but once in a great
while wiping everything and seeing if you can really put it all back together
can help you learn a lot about your system and how it works.
