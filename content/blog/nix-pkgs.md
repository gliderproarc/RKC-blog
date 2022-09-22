+++
title = "Nix packages"
author = ["Robert Clay"]
date = 2021-01-23
lastmod = 2022-09-23T08:27:43+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-01-23 Sat]</span></span>,#nix


## An alternative packaging system {#an-alternative-packaging-system}

I have been experimenting with a package system called
[Nix-packages](<https://nixos.org/>). It's very interesting as an alternative way
to install tools in a development environment without worrying about how it will
affect the rest of your system. I can't explain the intricacies nearly as well
as a blog post like
[this](<https://wickedchicken.github.io/post/macos-nix-setup/>) but I can share my
experience with trying it out.


## First off, why nix? {#first-off-why-nix}

Having tried to get Emacs, Python, Git, and various command line tools working
on WSL, I have felt the pain of installing something only to find the thing it
relied on broken after the installation was complete. I also realized the
benefit of working an environment like WSL. WSL is fairly small, and runs within
Windows. Meaning whenever I have installed something in the past the "broke" my
WSL install, I could just blow away the whole system and start again in a few
minute. Much easier than needing to re-install my whole Windows 10 installation.
And since I am considering a move back to Mac once my main tools are ready for
the new Arm architecture, I am looking for a way to install things without the
fear of breaking the rest of my machine.

Getting a virtual linux environment is bound to be handy, but getting tools like
Emacs where I can use them natively within MacOS is going to take a little more
work. Homebrew is one such way people install linux tools for native use on the
Mac, but it sounds like NixOS (or rather it's package system Nixpkgs) could be a
way to have my cake and eat it too; get the convenience of simple install and
the safety of a sandbox (sort of).


## Two examples {#two-examples}

Let's start with Emacs. I decided to test out installing Emacs in an Ubuntu
environment on WSL2. Having installed it **MANY** times before, I was already
familiar with the process, but I wanted to try it with Nix. So in a terminal:

1.  `curl -L https://nixos.org/nix/install | sh`
2.  `nix-env -iA nixpkgs.emacs`

Two terminal commands and some waiting and I was running Emacs. You could argue
that this would have been just one line installing from "apt", but I was now
able to remove Emacs with a simple

-   `nix-env -e emacs`

So with emacs installed so quickly (and after a normal additional install of
Doom), I decided to check out installing languages. I have been learning Python
and Clojure, and getting both to play nicely with Emacs has been rather
challenging. Not impossible, but difficult to get running at first.

-   `nix-env -iA nixpkgs.python3`
-   `nix-env -iA nixpkgs.clojure`

...open up a Org mode buffer, try to evaluate some code in with org-babel, and
what is this?! It just works? I was very impressed.

Now Nix is far from perfect. As I understand it is going to take some time
before it's really ready for ARM based macs, and the packages it contains will
most likely be x_86 complied for the time being. As things move forward I am
sure there will be better support. Side note: it never ceases to amaze me what
some free and open source software accomplishes while I pay hundreds of dollars
for my music software.

My second experiment was with the Nyxt browser. It's a young project with web
browser that promises to be as extensible as Emacs, based in lisp, but with
modern web-rendering engines. Not an easy task, and the project is still being
developed. I have been wanting to try it our for a LONG time, but could never
get the installer to work on WSL. Then I found there is a nix package!

1.  `nix-channel --add https://channels.nixos.org/nixpkgs-unstable/ unstable`
2.  `nix-channel --update`
3.  `nix-env -iA nixpkgs.nyxt`

That was the smoothest experience I had ever had trying to install this browser.
But as I suspected, it wasn't working very smoothly on WSL. And it installed a
**bunch** of stuff to get it working. I spotted Python 2 and 3 in the list of
things getting pulled in. Uninstalling was a breeze.

-   `nix-env -e nyxt`

So while I am sure I will need to wait a bit before the experience with Nix and
installing tools like Emacs and Clojure is so smooth on the newest macs, I am
very happy to see how well it functions as a package manage in WSL on Windows.