+++
title = "Portable Linux"
author = ["Robert Clay"]
date = 2022-11-02
lastmod = 2022-11-01T08:30:34+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2022-11-02 Wed]</span></span>,#programming


## Raspberry Pis are pretty cool {#raspberry-pis-are-pretty-cool}

Recently I purchased a small Raspberry pi Zero 2w. I put it in this little case, and now I have a small quad core computer the size of the thumb drive that I can bring along with me anywhere on my keychain. I was going to leave it at home to be like my own cloud server without needing to pay for a cloud, but it looks like my ISP won’t let me host a web sever without paying more money. If it’s going to cost me more money, I would just as soon give the money to a cloud provider. Thinking of what else I could use the pi for, I realized I could pair it with my iPad for a rather interesting combination of portable devices.

I also recently purchased an iPad. It’s compatible to my old iPad in that the size and model are similar, but this one has Apple’s new M1 chip in it, and it’s crazy powerful. But despite all that power, I can’t run Emacs on it. Sad right? All that power, and I can’t run the software I want to run. Having tasted the possibilities of what can be done when you have full control over your device, it’s hard to just let a device like an iPad be relegated to what is offered in Apple’s App Store. 

Thankfully, someone made an app for SSHing into servers, and if I carry around both my iPad and my Pi, I can use the iPad as a screen for the Pi and do a surprising amount to things with just those two. I will most likely end up bringing my keyboard too, but it’s an interesting kind of portable that my laptop is not.

I have a laptop too. It’s a great machine. It’s also running Appple’s new silicon, but I do find it a bit heavy and wouldn’t want to haul it all over the place if I am going to be moving around a lot. The iPad on the other hand is small and light. It’s easy to plop into whatever bag I am carrying and be off and on the move. Add a small keychain that is a little screen-less computer, and keyboard, and I have re-assembled the 3 things that make a laptop what it is, but having chosen each on my own.

The iPad works really well as a second display for the laptop. That’s actually the primary reason I bought it. At my current workplace I may not have access to the company owned external monitor for very much longer. So I wanted a way to be able to have and use my own. And as long as it’s an iPad, I can also use it as my “lounging on the couch” computer. And by just adding a keychain and keyboard, it’s also a surprisingly capable development environment. 

## The walled garden can be nice {#the-walled-garden-can-be-nice}

iOS does have a lot of nice apps built for it. I can’t deny that the reason I use an iPhone in the first is for the apps it runs. Take the app I am writing this blog post on. iA Writer is a nice markdown app the just feels nice to type in. Being able to use quality apps like this make computing fun. But I also want to be able to fire up a Elixir REPL with iex, or a Clojure REPL. And that is where the Linux box, my little Pi is going to come in.

## But FOSS wins when it comes to making software {#but-foss-wins-when-it-comes-to-making-software}

Emacs is something I use everyday. It won’t run on my iPad. Git is a great way to version control files. I can only use it on my iPad with a git client. Elixir is a fantastic programming language. It won’t just install on my iPad. So if I want to run an Elixir app as I am building it, I am going to need something to let me do that on my iPad. And that is what I have found with this Pi zero.