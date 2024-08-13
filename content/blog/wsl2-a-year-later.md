+++
title = "WSL2 a year or so later"
author = ["Robert Clay"]
date = 2021-04-19
lastmod = 2024-08-14T08:52:57+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-04-19 Mon]</span></span>,#wsl


## WSL2 has been really fun to work with {#wsl2-has-been-really-fun-to-work-with}

Before this post ends up looking like a rant or complaint against Microsoft, let
me say that I am so happy that Microsoft built this. If it were not for the hard
work of the people who built WSL, I would never have found the joys of working
with linux at the command line. I am extremely grateful, and use WSL everyday to
run Emacs. It's incredible to think I use a Windows laptop but spend most of my
time in Linux.

But I have been running into an issue or two over the past few months, and I
feel like they might be useful to someone else who is searching the web trying
to find information about their issue. I might be having your problem too, and I
will post if and when I find a solution.

I have two issues that are ailing me.

1.  CPU spikes when running WSL2
2.  File read-write permissions when working between Windows and WSL


## I am sure some of these issues are just growing pains for WSL {#i-am-sure-some-of-these-issues-are-just-growing-pains-for-wsl}

I am really stumped by these CPU spikes. Because for all the problems I seem to
get at work, when using the same computer at home WSL and Emacs seems to run
just fine. It looks like it could be a network issue, or it's a issue with using
an external display (as my network connection at work is less than ideal and I
don't use an external monitor at home). I think the CPU spikes will go away
either with an update further down the road or when I figure what is causing the
problems externally. But it's frustrating nonetheless to find a tool so useful,
and periodically need to wait several seconds while the CPU spikes, fans kick
in, and the application doesn't respind till things calm down.

The file read write issue might also be my fault but I think it could just be
part of how WSL works. What I am trying to do is write to a Scheme file while
MaxMSP watches the file for changes. As the file is updated, I want Max to read
the file again. The problem I am running into is permission to write to the file
while Max is watching it. If I just try to read and write the file from WSL, I
seem to be okay. But if I try to write to it while Max is using it, I get an
error telling me the WSL program doesn't have permission to write to the file.

I can understand why you would ordinarily want to restrict a program from reading
and writting a program being used by another program. You could have data change
out from underneath you and all kinds of things seem like they could break. But
that is kind of what I am trying to do. I want to hot-reload code while the
program is running. If I can't write to the file while Max is running it defeats
the purpose of using an external editor.


## I could just look for another way to get information into Max {#i-could-just-look-for-another-way-to-get-information-into-max}

I've written about Max on this blog before, and ultimately my goal is so make
some sound (or image) with Max. If I can use coda to help me do that better,
Emacs is where I write code these days. But needing to start and stop Max every
time I want to put code into Max, or needing to copy and paste snippets of code
from Emacs into Max every time I want to move things back and forth sounds like a
lot more work than it needs to be.

Node and some way of getting into a Node instance is still a possibility, and I
DID get Clojurescript to write a node script for me. But the steps involved feel
needlessly complicated and I am having trouble using CLojurescript only in Emacs
with Org-babel. I have given up on getting Clojurescript to work for the time
being hopping that I will be able to pick it back up once I get a Mac and I can
figure out how to install Planck.
