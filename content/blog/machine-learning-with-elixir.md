+++
title = "Machine Learning with Elixir"
author = ["Robert Clay"]
date = 2022-12-30
lastmod = 2022-12-30T08:28:14+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2022-12-30 Fri]</span></span>,#programming


## Who would have thought Elixir would lead me to ML?

In a few blog posts before I have mentioned I haven’t really figured out what I want to make. I learned Python and it enabled me to make a few handy scripts at work. I learned how to make formulas in Org-mode and they have helped me avoid using as many spreadsheets by getting as good if not better functionality without them. 

I took some time away from my study of Elixir and even tried some JavaScript and got some server-less JavaScript running on the Google cloud to help make Google spreadsheets even more powerful. But that quickly gave way to me transpiring ClojureScript to JS allowing me to write Lisp instead of JS. Clojure is amazing. If I had a big project to tackle and needed to go full-stack, JVM on the back and CLJS on the front would make me very happy. 

But despite how nice Clojure has been, I keep getting drawn back to Elixir and LFE. I even found out the other day how to call Elixir standard library functions from LFE. By requiring the beam files of Elixir, the LFE REPL can call out to those functions just like it calls out to Erlang. I have also recently gotten myself an iPad and I wanted a way to code on it on the go. Since I carry around a little Linux server with me (Raspberry Pi zero 2w), I learned I can host a Livebook on the Pi, and interact with it in a browser on my iPad. So that’s a cell based coding environment where I can run Elixir almost like how I work in Org-mode, but without needing Emacs. Nothing against Emacs. Emacs is still my preferred editor. But in terms of a place to work with Elixir code, Livebooks offer a lot less fuss to run Elixir code. And the fact I can get it working so well I can run in on my iPad on the go almost as well as on my laptop means it’s how I am bound to be doing a lot more of my computing moving forward. 

And while I was exploring Livebooks, I discovered an update the Livebook team pushed up recently that makes downloading and calling out to ML models really simple. Just name the kind, select the model, and it downloads and sets it up. Then just makes calls to it.

## GPT3 Chat is all the rage right now

I must say I am very impressed with it myself. Being able to use plain English to get machine learning to do so much is really exciting. I was intrigued by the hype around NFTS when they first came out, but as I saw what they ended up making and community around them, I realized they weren’t were I want to be spending my time. ML on the other hands, it enables all kinds of things I use. I don’s use it all the time, but RX from iZotoupe uses ML. Even Microtonic (made by the wonderful developer Magnus Lidström from Soniccharge) now has a neural network based beat generator. And if I can learn how to make things remotely close to GPT3 chat, that is a fascinating way to make a user interface. 

So I think I have found where I want to focus my coding study for the time being. Elixir, LFE, and ML.

## Wait… not python for ML?!

Yeah crazy right? Why go to Elixir for ML when hands down the top language for ML is also a language I already know and don’t mind using. Well I won’t ignore Python. But Livebooks mean I don’t need Jypiter notebooks. And being able to use a functional language instead of Python is too good not to pass up. Nx from Elixir even allows pluggable backends meaning I could make a model and get it running on all kinds of platforms. Plus it can mostly just import PyTorch and TensorFlow models.

And that just about wraps up what I wanted to say about the start of my journey with ML, and also marks the end of my blogging for 2022.

I’ve been busy with all kinds of stuff recently and haven’t written much in this blog. But now that I know I don’t want to focus as much on getting Phoenix under my belt, I think I will be a bit more focused in my study and might even have more to write about here. 
