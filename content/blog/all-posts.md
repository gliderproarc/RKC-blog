+++
author = ["Robert Clay"]
lastmod = 2021-09-20T09:23:23+09:00
draft = false
+++

## Pages {#pages}


### Main page {#main-page}

This will be on of the pages separate from the blog posts. It will be longer.


## Posts {#posts}


### Topic {#topic}


#### <span class="org-todo todo TODO">TODO</span> Post Title {#post-title}

-   State "TODO"       from "DONE"       <span class="timestamp-wrapper"><span class="timestamp">[2020-12-15 Tue 22:31]</span></span>

Content

More Content

{{< highlight 7ang "hl_lines=8" >}}
      echo 'Some source code content'
      echo 'This line will be highlighted'
      echo "This one won't"
{{< /highlight >}}

<!--list-separator-->

-  Post Sub-Heading

    This is another section within the post.


#### <span class="org-todo todo TODO">TODO</span> Draft Post Title {#draft-post-title}

This article **will** be exported but will be marked `draft = true` in the front matter.


#### <span class="org-todo done DONE">DONE</span> First post {#first-post}

<span class="timestamp-wrapper"><span class="timestamp">[2020-12-15 Tue]</span></span>, #first\_post

This is the first of many posts to come. I had never considered my self a
blogger type, but I have been learning some things recently and I feel like a
blog is a great way to share what I have been learning in an ...oddly
old fashioned manner. This past year I went from using Google docs to keep
notes at work, to today finding myself unwilling to use anything less than
Emacs and Org mode for a surprising amount of my day to day note taking and
organization. It was a lot to learn, but the journey was worth it, and I hope
to share not just what I have been learning about this past year (2020 was
one for the record books in more ways than one), but I haven't really felt
like I had a place to tell my story until now.

These days all the young kids in Japan want to grow up and be a YouTuber.
YouTube is a fascinating medium, and the amount of things you can learn and
see there is staggering. But I have found myself gravitating to text these
days and hope that a simple presentation can provide some counterpoint to the
rest of the world that seems to be happily consuming ever increasing amounts
of loud, noisy, colorful, and occasionally obnoxious video content in various
forms.

...wow, I started off this blog with a little "get off my lawn" soap-box
speech. This is going to be interesting.


#### <span class="org-todo done DONE">DONE</span> What this Blog runs on {#what-this-blog-runs-on}

<span class="timestamp-wrapper"><span class="timestamp">[2020-12-16 Wed]</span></span>, #Emacs
This blog looks very simple on the surface, but what it is built on is
something I am particularly happy with, and it will introduce a few themes
and topics that I will write about more in the future.

Here is the loose chain of software and tech between my posts and the
internet:

-   Emacs and org-mode
-   ox-hugo
-   Hugo static site generation
-   .git file for version control
-   Hosting of that .git file on Github
-   Github api calls to Netlify that runs a CI routine to build the site push
    it to the web.

    The fact I was just learning what Emacs was a year ago still makes me wish
    I had tried to learn all of this sooner. The number of powerful tools out
    there for people willing to learn them is incredible. And if I had learned
    how to use all this sooner, I wonder what I might have made when I was
    younger with more time on my hands.. lol.

    Just Emacs and Git have been a journey to learn, but now I have so much
    respect for what they can do as tools and how they let me do my work. And
    of all the things I could say about them I think I am most interested in
    talking about text files.

<!--list-separator-->

-  Text files?

    Yeah, text files. You know, on your computer when you have a file that ends
    in .txt. That is a text files. Text files are awesome. I didn't think they
    were all that interesting until I learned what happened to files on a
    computer that are 10+ years old.

    I had a few laptops over the years, and I had never really given back-ups
    much thought because I am (was?) an Apple guy. I just turned on time-machine and
    called it a day. But these days when I try to get at ****really**** old files,
    I find a lot of those files don't open anymore. The data is there, but I
    can't use the program that made it. So even though I backed it up, the
    backup is useless. I still can't get at what I made. But do you know what I
    can still open? I had a diary app that let me do an export of my entire
    list of entries as an .rtf or rich text file. These files I can open, and
    they read just fine. That is because the .rtf file format is a widely
    adopted standard that lots of program can read and write to. But all my
    program that stored their information in proprietary formats are mostly
    useless now.

    So when I got to thinking about making this blog, I decided to make it here
    with a Hugo back-end. Hugo is a static site generation frame work built on
    Go, and while I don't know enough Go to be able to build it my self, have
    access to most the inner working of this site is really quite fun and
    interesting. To make a post, I just make a mark-down file, put it in the
    right spot in my file structure and I have a new blog post. I'll talk about
    Git and Emacs another day, but Org mode deserves some special mention.

<!--list-separator-->

-  Org mode

    Org mode is it's own markup language specific to Emacs and has a lot of
    support built into it for the lisp code (or elisp rather) it is built with.
    I have had to learn a bit of lisp, but as far as programming languages go I
    think it's not nearly as troublesome as languages like Javascript, but I
    digress. Suffice to say Org is a markup language, but at the end of the day
    it's also just text files. Meaning even if I needed to move away from Emacs
    and Org mode one day, all the words in my blog and notes will all be just a
    bunch of copy and paste of text to move somewhere else.

    ---
    I would not recommend this platform to everyone. The amount of reading I had
    to do to get it up and running was pretty substantial. And if you are
    thinking of making a blog I am sure tools and platforms like Word-press are
    much more approachable. But I really like what Hugo and Netlify and Emacs
    have afforded me here. I save an Org file and commit to a Git repository and
    I have posted a blog post. To me... that is the kind of powerful simplicity
    I want to use.


#### <span class="org-todo done DONE">DONE</span> Org mode introduction {#org-mode-introduction}

<span class="timestamp-wrapper"><span class="timestamp">[2020-12-17 Thu]</span></span>,#Org-mode

  This topic deserves more than a post or two, but it's a nice short introduction to
what it is and how it works might help you understand why I have come to rely
on Org mode for most of my note taking and task tracking needs.

<https://orgmode.org/manual/>

  Let me start with why I went looking for and found Org mode. I was making
really complicated spreadsheets at work. I was trying to program in a
spreadsheet, and even convinced my company to get adopt a no-code tool. It was
great. Lots of the power I wanted from a program but with the flexibility of a
spreadsheet. I was so happy using it, I wondered it if might be nice to try
and use it for my personal data management, and then I ran into a problem

<!--list-separator-->

-  It cost a monthly subscription fee

    Not that a monthly fee is all bad. The excellent company who made the
    software need to make money too. But I could not afford to be paying a
    monthly fee for software that I could do more or less with what I
    already had. I was much more interested in spending money on music
    software.

    So I went online and started looking for software. I found a few text
    editors that did some of what I wanted, I tired Atom and thought it was
    pretty cool. But what I really wanted was something that would:

    -   Tie in data in a spreadsheet with my words in my notes
    -   Help me make notes, tasks, and track appointments without needing to use
        something like Google calendars
    -   Approach code in terms of flexibility and let me make tools for what ever
        else I wanted it to do for me.

<!--list-separator-->

-  I don't remember the forum where someone suggested Org-mode, but I will forever be grateful for the advice I got

    I was warned that Org was hard to get set up, but that once you had it
    working it would do all those things I was looking to do and more.

    So let me get into what Org mode is. It's a "mode" for a  text editor
    called Emacs, and it's a markup language that has a few extra
    functionalities. Once of them is tables. While HTML tables are notoriously
    hard to type, format, and work with, Org mode makes them very easy and even
    provides most of what you would expect from a basic spreadsheet
    application... with one ****very**** big difference. Org mode also provides
    facilities for literate programming, meaning you can have cells in you
    spreadsheet that don't have to use the less than ideal "language" of
    spreadsheet formulas. You can write a Python function and have the result
    fill out into a column in your table. Something like this:

    ```text
      #+TBLNAME: data_for_testing
      | number | Python |
      |--------+--------|
      |      1 |      2 |
      |      2 |      3 |
      |      3 |      4 |
      |      4 |      5 |
      #+TBLFM: $1='(org-sbe "Add_1_to_me" (num $1))

    #+name:Add_1_to_me
    #+begin_src python :python python3 :var num=1
    return(num+1)
    #+end_src
    ```

    Now any spreadsheet can add a number to the next cell's value, but the fact
    it can be written in a programming language as simple and powerful as
    python is one of the things that keeps me from looking anywhere else to do
    this sort of thing.

    I'll touch on the way the Python code is represented there later. Let me
    keep going on what I originally needed Org to do for me. I also wanted a
    way to write and keep notes. I had used Atom basic .md files, but Org did
    more than just give me a way to write notes. Because it is implemented in a
    Lisp interpreter, there are many things you can ask code to do for you
    based on what you write in your notes. Things like a special syntax to make
    something a "task" or a special syntax to make things a date which can be
    recognized else where to place notes and tasks relative to each other like
    a planner, it's really quite amazing how many things are in this software.
    And what really struck me was that fact it was basically all plain text
    and lisp code.

    I've mentioned lisp and code a few times, and while my intention was not to
    learn how to write code when I started using Org mode, I decided to try a
    little bit here and there and found that it wasn't as bad as the last time
    I had tried my hand at coding, and the "literate programming" style of
    writing prose with bits of code interspersed around the file was really
    nice. So I am teaching my slef a few languages, and one of them is elisp.

    ```text
        #+name:example-code
        #+begin_src elisp
    (cdr '(a b c d))
        #+end_src

        #+RESULTS: exmaple-code
        | b | c | d |
    ```

    I won't bore you with a lisp tutorial, but suffice to say Org mode has made
    writing little bits of code that work together with words really easy. And
    surprisingly, you can mix languages. Because these blocks of code are
    independent in your document, you can define what they "see" from each other
    and string them together into a program with several languages in it.

    My short introduction here hardly does the program justice, but if you want
    to know more, the link above can take you to the Org mode manual, which will
    tell most of what there is to know about it. If you are willing to learn how
    to use Emacs, Org mode is an amazing tool that made Emacs worth it for me.
    And after a while I started to find just how interesting Emacs it's self is
    too, but that is a topic for another day.


#### <span class="org-todo done DONE">DONE</span> Spacemacs {#spacemacs}

<span class="timestamp-wrapper"><span class="timestamp">[2020-12-21 Mon]</span></span>,#Emacs

Along with my search for an extensible note taking application and
discovering Emacs and Org-mode, I also discovered Spacemacs (a set of
configurations and settings for Emacs).

<https://www.spacemacs.org>

I didn't know what Vim was before I started reading the introduction on the
Spacemacs home page. And that got me reading all kind of interesting articles on Vim, and
how it's nice to know if you need to SSH into a sever you don't know and
can't install any software. "vi" is going to be on that server, and it can
run in a terminal session without any GUI. Modal text editing is not
something I can used before, but having used several music synthesizers
interfaces that have several function layers, I found the ideas of modes and
functions for keys to be really easy to work with. When I installed Emacs and
started playing with it, I didn't mind the use of "hjkl" for navigation.

What I did find really confusing was vanilla Emacs and it's keybinding. I am
slowly getting used to them now, and having something like Spacemacs
probably slowed my progress when it came to learning Emacs it's self. But
Spacemacs made Emacs really approachable with a lot of help along the way. I
would definitely recommend Spacemacs to anyone looking to get into on of the
deep text editors but doesn't feel they can handle vanilla Emacs right away.

I found an article online that talked about not trying to pile more than one
"learning curve" onto of another. If you don't know how to run a terminal and
are trying to get into terminal Emacs, you have two unfamiliar things you are
trying to learn at the same time. By only tackling them one at a time, you
get to deal with each problem one at a time.

In my case I was trying to juggle the following:

-   Widows
-   WSL (Windows subsystem for linux)
-   Building Emacs from source
-   Emacs
-   Org-mode

    It was a bit of a mess at first, and I can smile now as I think of all the
    things I had to go though to get it all working. When I was trying to get
    it set up there were a lot of issues that plagued just WSL, but now there
    are many guides you can find online to help you get started like this one:

    <https://github.com/hubisan/emacs-wsl>

    WSL was a great option for getting Emacs installed an running, but it
    created a lot of issues got me really confused about what was what. Emacs
    can run terminal emulators inside it... so if I can't run a program is it
    because it is only in Emacs? What is Python environment? What is a virtual
    environment? Why are some environment variables different in Emacs verses
    a bash shell? I had a lot of things to learn and one could argue that I
    took the hard way.

    ...but it was worth it. If you are at all interested in trying out Org mode
    and don't know if you can handle Emacs without help, I would heartily
    suggest you give Spacemacs a try. Personally I am looking to move to Doom
    in the next few weeks. Doom is like Spacemacs in that it is a pre-made
    configuration, but it's crazy fast, and while not as user friendly as
    Spacemacs, I think I can learn to work with it now.

    As I make the transition to Doom, I will be sure to post my thoughts and
    impressions here on this blog. One more resource on Emacs and Spacemacs
    before I wrap this post up:

    Spacemacs: Installation, Configuration, and Navigation Tutorial
    By: Jack of Some
    <https://www.youtube.com/watch?v=fdLCuJcS2Aw>

    This tutorial really got me set up and going. If there is one thing that
    struck me with Spacemacs, it was how nice and welcoming and helpful people
    were in helping me get up and going.


#### <span class="org-todo done DONE">DONE</span> Software talking to software {#software-talking-to-software}

<span class="timestamp-wrapper"><span class="timestamp">[2020-12-27 Sun]</span></span>,#software
This post is going to be a little less focused than other posts on the same
subject, but I feel I have a unique perspective to share from someone who is
just getting into this space. Sometimes it's hard to see further down the rabbit
hole to see how far down it goes, and it can be hard to see above you and how far
down you have come. A lucid moment to reflect on where you are can be nice not
only to redirect yourself, but maybe also to help others decide if this rabbit
hole they are heading down is really worth it.

<!--list-separator-->

-  A long chain of software

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

<!--list-separator-->

-  Why all this complexity?

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

<!--list-separator-->

-  Is it worth it?

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

<!--list-separator-->

-  Software talking to software is very powerful

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

<!--list-separator-->

-  ...as long as you can manage the complexity

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


#### <span class="org-todo done DONE">DONE</span> MaxMSP hold switch {#maxmsp-hold-switch}

<span class="timestamp-wrapper"><span class="timestamp">[2021-01-03 Sun]</span></span>,#MaxMSP

<!--list-separator-->

-  Making your own tools can be a rewarding challenge

    Being a computer musician, I appreciate the ability to work with data as it suits me. I don't need to just accept a stream of midi and ask a software synthesizer to make sounds for me. I can manipulate that stream of data in interesting ways before I put it to use. One such use I found for this manipulation is replicating a feature of a keyboard I sold a few years back.

    I used to own a Roland JD-XA. It was a real analogue synth with some modern and cool features. Sadly, my audio recording set up was not up to doing it justice, and I ended up using it mostly as a controller. I sold it to get a Roli Seaboard instead and I am very happy with it. But I did miss a button on its front panel; the "hold" switch that went with the arpeggiator. The switch when used with the arpeggiator let you hold out the notes in a sequence even when you took your hands off the keys, but I liked the fact it wasn't tied to the arpeggiator itself. When it wasn't used with the arpeggiator, it acted like an "auto-sustain-pedal". Notes played legato were all sustained, and a new "set" of notes would trigger a re-pedal and the next set of notes would sustain while the old notes would stop. It was super fun to use in conjunction with a two tier keyboard set up. I could play a piano like patch in my lower keyboard while the top board would be set to some sustaining patch that I could play a few notes on without needing to stand on a sustain pedal the whole time.

    I was thinking I might be able to get something similar from other arpeggiators, so I didn't think much of it when I sold the board. But after a few attempts with a few arpeggiator plugins, I quickly realized that this wasn't how most arpeggiators worked. But I also knew I had Max4Live. I figured I could just make my own.

<!--list-separator-->

-  What I wanted to make

    Before I get into how I started trying to make this, I want to spell out exactly how it was supposed to work.

    -   A "mode" needed to be enabled and easy to turn off.
    -   That mode needed to know when notes were still being played or not
    -   All note offs needed to be captured and handled in a special way
    -   If there were no notes being held, a list of note offs for the currently sustaining notes would be to be calculated and sent before the new note on.

    On the surface it seemed to be a really simple problem. Very clear order of operations, nothing that was too complicated, I thought it would take me 30 minutes to whip something up. Boy was I wrong.

<!--list-separator-->

-  The first few tries did not go well

    My first attempt quickly spiraled out of control into a mess of complexity.
    Generating a list of notes that were currently being held down on a keyboard
    connected to this utility proved really hard to make and deal with. I had
    considered making a dictionary where I added note-on events as entries and
    note-off events as a sign to remove the entry. But having worked with some
    Clojure at this point I wanted a solution that didn't rely on something mutable like this "dictionary" I was planning on using. Writing the "state of the midi stream" with each new event lead to a huge mess of operation order. Do I read the dictionary before of after I compare the note coming in to the others to see if it's a note already in the list? Should the dictionary read be part of the clean up at the end of the chain? When does the note off list get generated? How I can generate that list without having the dictionary pass its contents all over the place? Do I need the contents of the dictionary in multiple places? It was a disaster.

    Imagining the problem was Max, I proceeded to wire up Max and Node and ClojureScript, hoping that a different language would have better support for what I was trying to do. But after spending more time with Max, I found a better way forward.

<!--list-separator-->

-  But then I found out Max had already solved the problem for me

    Max has an object that simulates what a sustain pedal does. While the "pedal" is down, all note offs are kept back. And when you send it the right message, all the current notes are ended with their corresponding note-off messages. This object solved 50% of what I was trying to do. I no longer needed to handle the creation of the note off messages. It even gave me a set of configurations for working with note-on overlap. I had originally split the midi note messages into note-on and note-off messages because I assumed I needed to count them to know how many notes were being held down, but it turns out there was a Max object for that too. Borax is an interestingly named object that reports various things about the state of a stream of midi. One of those bits of information is how many notes are currently "being held" from the stream of data.

    So to wire it all up I only needed to:

    -   check to see the number of notes held now.
    -   If zero, open a gate
    -   Bang on the gate. If it's open send start the sequence to send the notes offs.
    -   The notes-off messages are send by controlling something like a sustain pedal, so using a delay I "lift" and "depress" the sustain pedal.
    -   Pass along the midi message to then "sustain object".

    Now that it's all finished, I can call up a bit of code that runs in Ableton
    Live with just a few keystrokes whenever I want to. It replicates what my old
    keyboard used to do, but with the flexibility of being implemented in MaxMSP
    coda rather than tied up in a piece of hardware. I learned a lot about Max and
    I hope this makes my next project that much easier to get started on.

<!--list-separator-->

-  The MaxMSP object for those interested

    ```text
    {
    	"boxes" : [ 		{
    			"box" : 			{
    				"maxclass" : "newobj",
    				"text" : "patcher hold-switch",
    				"numinlets" : 3,
    				"numoutlets" : 1,
    				"id" : "obj-46",
    				"outlettype" : [ "int" ],
    				"patching_rect" : [ 712.000016808509827, 413.666671216487885, 145.0, 24.0 ],
    				"patcher" : 				{
    					"fileversion" : 1,
    					"appversion" : 					{
    						"major" : 8,
    						"minor" : 1,
    						"revision" : 8,
    						"architecture" : "x64",
    						"modernui" : 1
    					}
    ,
    					"classnamespace" : "box",
    					"rect" : [ 1059.0, 84.0, 955.0, 1003.0 ],
    					"bglocked" : 0,
    					"openinpresentation" : 0,
    					"default_fontsize" : 12.0,
    					"default_fontface" : 0,
    					"default_fontname" : "Arial",
    					"gridonopen" : 1,
    					"gridsize" : [ 15.0, 15.0 ],
    					"gridsnaponopen" : 1,
    					"objectsnaponopen" : 1,
    					"statusbarvisible" : 2,
    					"toolbarvisible" : 1,
    					"lefttoolbarpinned" : 0,
    					"toptoolbarpinned" : 0,
    					"righttoolbarpinned" : 0,
    					"bottomtoolbarpinned" : 0,
    					"toolbars_unpinned_last_save" : 0,
    					"tallnewobj" : 0,
    					"boxanimatetime" : 200,
    					"enablehscroll" : 1,
    					"enablevscroll" : 1,
    					"devicewidth" : 0.0,
    					"description" : "",
    					"digest" : "",
    					"tags" : "",
    					"style" : "",
    					"subpatcher_template" : "Default Max 7",
    					"assistshowspatchername" : 0,
    					"boxes" : [ 						{
    							"box" : 							{
    								"maxclass" : "newobj",
    								"text" : "unpack",
    								"numinlets" : 1,
    								"numoutlets" : 2,
    								"id" : "obj-6",
    								"outlettype" : [ "int", "int" ],
    								"patching_rect" : [ 319.333338856697083, 340.0, 47.0, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "inlet",
    								"numinlets" : 0,
    								"numoutlets" : 1,
    								"id" : "obj-5",
    								"outlettype" : [ "bang" ],
    								"patching_rect" : [ 460.0, 30.0, 30.0, 30.0 ],
    								"comment" : "",
    								"index" : 3
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "button",
    								"numinlets" : 1,
    								"parameter_enable" : 0,
    								"numoutlets" : 1,
    								"id" : "obj-34",
    								"outlettype" : [ "bang" ],
    								"patching_rect" : [ 475.666665613651276, 107.333334505558014, 66.0, 66.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "newobj",
    								"text" : "route 0",
    								"numinlets" : 2,
    								"numoutlets" : 2,
    								"id" : "obj-32",
    								"outlettype" : [ "", "" ],
    								"patching_rect" : [ 371.666667461395264, 178.0, 46.0, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "newobj",
    								"text" : "pack",
    								"numinlets" : 2,
    								"numoutlets" : 1,
    								"id" : "obj-30",
    								"outlettype" : [ "" ],
    								"patching_rect" : [ 337.0, 732.0, 37.0, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "newobj",
    								"text" : "midiparse",
    								"numinlets" : 1,
    								"numoutlets" : 8,
    								"id" : "obj-28",
    								"outlettype" : [ "", "", "", "int", "int", "", "int", "" ],
    								"patching_rect" : [ 211.0, 200.0, 92.5, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "newobj",
    								"text" : "midiformat",
    								"numinlets" : 7,
    								"numoutlets" : 2,
    								"id" : "obj-25",
    								"outlettype" : [ "int", "" ],
    								"patching_rect" : [ 216.0, 785.0, 82.0, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "gswitch2",
    								"numinlets" : 2,
    								"parameter_enable" : 0,
    								"numoutlets" : 2,
    								"id" : "obj-40",
    								"outlettype" : [ "", "" ],
    								"patching_rect" : [ 191.0, 117.333334505558014, 39.0, 32.0 ],
    								"int" : 1
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "newobj",
    								"text" : "t l b",
    								"numinlets" : 1,
    								"numoutlets" : 2,
    								"id" : "obj-39",
    								"outlettype" : [ "", "bang" ],
    								"patching_rect" : [ 319.333338856697083, 295.00000274181366, 44.0, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "newobj",
    								"text" : "gate",
    								"numinlets" : 2,
    								"numoutlets" : 1,
    								"id" : "obj-27",
    								"outlettype" : [ "" ],
    								"patching_rect" : [ 496.666665613651276, 388.333338856697083, 37.0, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "button",
    								"numinlets" : 1,
    								"parameter_enable" : 0,
    								"numoutlets" : 1,
    								"id" : "obj-26",
    								"outlettype" : [ "bang" ],
    								"patching_rect" : [ 496.666665613651276, 423.000006556510925, 24.0, 24.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "message",
    								"text" : "1",
    								"numinlets" : 2,
    								"numoutlets" : 1,
    								"id" : "obj-24",
    								"outlettype" : [ "" ],
    								"patching_rect" : [ 453.333342850208282, 577.666677832603455, 29.5, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "message",
    								"text" : "0",
    								"numinlets" : 2,
    								"numoutlets" : 1,
    								"id" : "obj-22",
    								"outlettype" : [ "" ],
    								"patching_rect" : [ 413.666667520999908, 577.666677832603455, 29.5, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "newobj",
    								"text" : "delay 10",
    								"numinlets" : 2,
    								"numoutlets" : 1,
    								"id" : "obj-20",
    								"outlettype" : [ "bang" ],
    								"patching_rect" : [ 496.666665613651276, 468.000000536441803, 66.0, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "newobj",
    								"text" : "== 0",
    								"numinlets" : 2,
    								"numoutlets" : 1,
    								"id" : "obj-17",
    								"outlettype" : [ "int" ],
    								"patching_rect" : [ 496.666665613651276, 333.999996542930603, 37.0, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "newobj",
    								"text" : "borax",
    								"numinlets" : 3,
    								"numoutlets" : 9,
    								"id" : "obj-16",
    								"outlettype" : [ "int", "int", "int", "int", "int", "int", "int", "int", "int" ],
    								"patching_rect" : [ 371.666667461395264, 413.000005483627319, 103.0, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "toggle",
    								"numinlets" : 1,
    								"parameter_enable" : 0,
    								"numoutlets" : 1,
    								"id" : "obj-15",
    								"outlettype" : [ "int" ],
    								"patching_rect" : [ 360.999999284744263, 632.666671693325043, 24.0, 24.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "newobj",
    								"text" : "sustain",
    								"numinlets" : 3,
    								"numoutlets" : 2,
    								"id" : "obj-12",
    								"outlettype" : [ "int", "int" ],
    								"patching_rect" : [ 320.999999284744263, 669.666671335697174, 59.0, 22.0 ]
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "outlet",
    								"numinlets" : 1,
    								"numoutlets" : 0,
    								"id" : "obj-4",
    								"patching_rect" : [ 191.0, 860.0, 30.0, 30.0 ],
    								"comment" : "",
    								"index" : 1
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "inlet",
    								"numinlets" : 0,
    								"numoutlets" : 1,
    								"id" : "obj-3",
    								"outlettype" : [ "int" ],
    								"patching_rect" : [ 311.000009179115295, 24.0, 30.0, 30.0 ],
    								"comment" : "",
    								"index" : 2
    							}

    						}
    , 						{
    							"box" : 							{
    								"maxclass" : "inlet",
    								"numinlets" : 0,
    								"numoutlets" : 1,
    								"id" : "obj-2",
    								"outlettype" : [ "int" ],
    								"patching_rect" : [ 192.833338856697083, 24.0, 30.0, 30.0 ],
    								"comment" : "",
    								"index" : 1
    							}

    						}
     ],
    					"lines" : [ 						{
    							"patchline" : 							{
    								"source" : [ "obj-6", 0 ],
    								"destination" : [ "obj-16", 0 ],
    								"order" : 0
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-6", 1 ],
    								"destination" : [ "obj-16", 1 ],
    								"order" : 0
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-6", 0 ],
    								"destination" : [ "obj-12", 0 ],
    								"order" : 1
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-6", 1 ],
    								"destination" : [ "obj-12", 1 ],
    								"order" : 1
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-5", 0 ],
    								"destination" : [ "obj-34", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-40", 0 ],
    								"destination" : [ "obj-4", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-40", 1 ],
    								"destination" : [ "obj-28", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-39", 0 ],
    								"destination" : [ "obj-6", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-39", 1 ],
    								"destination" : [ "obj-27", 1 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-34", 0 ],
    								"destination" : [ "obj-26", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-32", 0 ],
    								"destination" : [ "obj-26", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-30", 0 ],
    								"destination" : [ "obj-25", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-3", 0 ],
    								"destination" : [ "obj-40", 0 ],
    								"order" : 1
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-3", 0 ],
    								"destination" : [ "obj-32", 0 ],
    								"order" : 0
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-28", 0 ],
    								"destination" : [ "obj-39", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-28", 1 ],
    								"destination" : [ "obj-25", 1 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-28", 2 ],
    								"destination" : [ "obj-25", 2 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-28", 3 ],
    								"destination" : [ "obj-25", 3 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-28", 4 ],
    								"destination" : [ "obj-25", 4 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-28", 5 ],
    								"destination" : [ "obj-25", 5 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-28", 6 ],
    								"destination" : [ "obj-25", 6 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-27", 0 ],
    								"destination" : [ "obj-26", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-26", 0 ],
    								"destination" : [ "obj-22", 0 ],
    								"order" : 1
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-26", 0 ],
    								"destination" : [ "obj-20", 0 ],
    								"order" : 0
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-25", 0 ],
    								"destination" : [ "obj-4", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-24", 0 ],
    								"destination" : [ "obj-15", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-22", 0 ],
    								"destination" : [ "obj-15", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-20", 0 ],
    								"destination" : [ "obj-24", 0 ],
    								"midpoints" : [ 506.166665613651276, 563.0, 462.833342850208282, 563.0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-2", 0 ],
    								"destination" : [ "obj-40", 1 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-17", 0 ],
    								"destination" : [ "obj-27", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-16", 2 ],
    								"destination" : [ "obj-17", 0 ],
    								"midpoints" : [ 402.166667461395264, 449.0, 481.999999284744263, 449.0, 481.999999284744263, 329.0, 506.166665613651276, 329.0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-15", 0 ],
    								"destination" : [ "obj-12", 2 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-12", 0 ],
    								"destination" : [ "obj-30", 0 ]
    							}

    						}
    , 						{
    							"patchline" : 							{
    								"source" : [ "obj-12", 1 ],
    								"destination" : [ "obj-30", 1 ]
    							}

    						}
     ],
    					"styles" : [ 						{
    							"name" : "Nord",
    							"default" : 							{
    								"color" : [ 0.56078431372549, 0.737254901960784, 0.733333333333333, 1.0 ],
    								"fontname" : [ "Source Code Pro" ],
    								"textcolor_inverse" : [ 0.925490196078431, 0.937254901960784, 0.956862745098039, 1.0 ],
    								"bgcolor" : [ 0.298039215686275, 0.337254901960784, 0.415686274509804, 1.0 ],
    								"locked_bgcolor" : [ 0.180392156862745, 0.203921568627451, 0.250980392156863, 1.0 ],
    								"clearcolor" : [ 0.180392156862745, 0.203921568627451, 0.250980392156863, 1.0 ],
    								"bgfillcolor" : 								{
    									"type" : "gradient",
    									"color1" : [ 0.376471, 0.384314, 0.4, 1.0 ],
    									"color2" : [ 0.290196, 0.309804, 0.301961, 1.0 ],
    									"color" : [ 0.290196, 0.309804, 0.301961, 1.0 ],
    									"angle" : 270.0,
    									"proportion" : 0.39
    								}
    ,
    								"stripecolor" : [ 0.180392156862745, 0.203921568627451, 0.250980392156863, 1.0 ],
    								"editing_bgcolor" : [ 0.231372549019608, 0.258823529411765, 0.32156862745098, 1.0 ],
    								"textcolor" : [ 0.847058823529412, 0.870588235294118, 0.913725490196078, 1.0 ],
    								"accentcolor" : [ 0.505882352941176, 0.631372549019608, 0.756862745098039, 1.0 ],
    								"elementcolor" : [ 1.0, 1.0, 1.0, 1.0 ],
    								"selectioncolor" : [ 0.92156862745098, 0.796078431372549, 0.545098039215686, 1.0 ]
    							}
    ,
    							"parentstyle" : "",
    							"multi" : 0
    						}
     ]
    				}
    ,
    				"saved_object_attributes" : 				{
    					"description" : "",
    					"digest" : "",
    					"globalpatchername" : "",
    					"tags" : ""
    				}

    			}

    		}
     ],
    	"appversion" : 	{
    		"major" : 8,
    		"minor" : 1,
    		"revision" : 8,
    		"architecture" : "x64",
    		"modernui" : 1
    	}
    ,
    	"styles" : [ 		{
    			"name" : "Nord",
    			"default" : 			{
    				"color" : [ 0.56078431372549, 0.737254901960784, 0.733333333333333, 1.0 ],
    				"fontname" : [ "Source Code Pro" ],
    				"textcolor_inverse" : [ 0.925490196078431, 0.937254901960784, 0.956862745098039, 1.0 ],
    				"bgcolor" : [ 0.298039215686275, 0.337254901960784, 0.415686274509804, 1.0 ],
    				"locked_bgcolor" : [ 0.180392156862745, 0.203921568627451, 0.250980392156863, 1.0 ],
    				"clearcolor" : [ 0.180392156862745, 0.203921568627451, 0.250980392156863, 1.0 ],
    				"bgfillcolor" : 				{
    					"type" : "gradient",
    					"color1" : [ 0.376471, 0.384314, 0.4, 1.0 ],
    					"color2" : [ 0.290196, 0.309804, 0.301961, 1.0 ],
    					"color" : [ 0.290196, 0.309804, 0.301961, 1.0 ],
    					"angle" : 270.0,
    					"proportion" : 0.39
    				}
    ,
    				"stripecolor" : [ 0.180392156862745, 0.203921568627451, 0.250980392156863, 1.0 ],
    				"editing_bgcolor" : [ 0.231372549019608, 0.258823529411765, 0.32156862745098, 1.0 ],
    				"textcolor" : [ 0.847058823529412, 0.870588235294118, 0.913725490196078, 1.0 ],
    				"accentcolor" : [ 0.505882352941176, 0.631372549019608, 0.756862745098039, 1.0 ],
    				"elementcolor" : [ 1.0, 1.0, 1.0, 1.0 ],
    				"selectioncolor" : [ 0.92156862745098, 0.796078431372549, 0.545098039215686, 1.0 ]
    			}
    ,
    			"parentstyle" : "",
    			"multi" : 0
    		}
     ],
    	"classnamespace" : "box"
    }
    ```


#### <span class="org-todo done DONE">DONE</span> Keyboard shortcuts {#keyboard-shortcuts}

<span class="timestamp-wrapper"><span class="timestamp">[2021-01-09 Sat]</span></span>,#keybindings

<!--list-separator-->

-  Keyboards are not the perfect input device

    ...but I sure do like them better than mice. I was listening to youtube talk by
    an amazing speaker who was using a story about the tech industry to make his
    point. He said that the mouse and the graphic user interface (GUI) democratized
    the computer. I think he made a good point. The fact people can work with a
    mouse and not need to interact with a computer in terms of text and code
    certainly opened the doors for myriads of people to harness the power of the
    computer. And I think that is great. But I also see how stopping at the mouse is
    missing a huge opportunity when it comes to interacting with a computer.

<!--list-separator-->

-  Using a keyboard is usually faster than a mouse

    If you do some searching online, you will see many people who argue that a
    keyboard driven paradigm for working with your computer is needlessly
    complicated. Their arguments tend to cover points like:

    1.  I need to reach for the mouse for my GUI only apps anyway.
    2.  Keyboard shortcuts aren't standardized. I can't remember them all.
    3.  The time you save really isn't that much.

    \#1 sure, I agree. One of the reasons I don't like the internet is because of how
    mouse-driven it is. There are ways around it (sometimes) but most of the
    internet seems to be built for those who only "click". I don't think this means
    it's worth abandoning keyboard-based interactions when they are available.

    \#2 Also true. This one bugs me to no end some days, but I have found that many
    of my favorite pieces of software also let me re-map keyboard short cuts to keep
    things more consistent.

    \#3 This one I disagree with. Many years ago I went to a (Apple's) Logic Pro
    music software training center in California. I went there to get a
    certification, which I passed. The other people I took the test with were
    professional music makers, and their time is money. Once gentleman put it this
    way:

    "...if you have a task you do a hundred times a day and you can save a second
    off the time it takes you to do it, that's 100 seconds a day. Multiply that over
    weeks and months and you are saving hours of time. Think of how long it takes
    you to move your hand from the keyboard to the mouse. That time is what you are
    saving by using a keyboard shortcut."

<!--list-separator-->

-  Shortcuts help because software is complicated

    If software were simpler, I don't think there would as much of a need for
    keyboard shortcuts. At some level, keyboard shortcuts are another way to access
    menus and configurations. If there were less things to configure or access
    through menus, I don't think shortcuts would be as effective. But software has a
    lot going on, and only so much can be shown with the visual. Some of the
    complexity is better hidden away where you can't see it. So let's look at
    something pretty simple. Saving a file:

    |   | mouse                  | keyboard shortcut         |
    |---|------------------------|---------------------------|
    | 1 | reach for mouse        | reach for keyboard        |
    | 2 | move mouse to menu-bar | [C-s] or equivalent       |
    | 3 | click on "file" menu   | confirm save with [enter] |
    | 4 | move mouse to "save"   |                           |
    | 5 | click on "save"        |                           |
    | 6 | move mouse to confirm  |                           |
    | 7 | click on confirm       |                           |

    This is only a fairly simple example. But simple changes from moving a mouse
    between elements of a GUI to moving you ringers between keys on a keyboard can
    make a big difference over many many repetitions of the same operation.

<!--list-separator-->

-  If your software has it, use a fuzzy-matching contextual menu

    While I can't use Emacs for most of what I do day in and day out on a computer,
    I have found an increasing fondness for a command it has called "Meta X" (or
    [M-x] in emacs binding notation). It pulls up a prompt allowing you to call
    items from the numerous menus in the program... by name. You might say it takes
    longer to type the name "calc-dispatch" than it does to move a mouse and click,
    but being able to call it by name means I don't need to remember where it's
    located. I just need to know the name. And because the command has been modified
    to use fuzzy matching, I don't need to write the whole name. I can start typing
    it and hit enter when it's the top result of commands with those letters in it.
    Which is why I have also decided to use the Vivaldi web browser.

    Many people will brag about how fast their browsers are. How quickly they can
    load web-pages. And by the same argument above (many repetitions of the same
    things make for big time savings in the long run) faster page load times should
    be king when it comes to web-browsing. Be that as it may, I like Vivaldi because
    it has something similar to the "Meta X" command in Emacs that lets me access
    nearly all the functionality of the browser without ever leaving the home row of
    my keyboard. If I know the exact keyboard shortcut I can use that instead, but
    being able to call menu items without needing to use my mouse (AND I can call
    menu items that have no shortcut assigned to them!) is very nice indeed.

<!--list-separator-->

-  ...and if you can configure and use key-bindings, they are totally worth it.

    It used to be that a highly keyboard centric text editor meant you needed to use
    Vim or Emacs. These are still both amazing pieces of software worth looking
    into, but you can get vim-like keybindings in many other text editors these
    days. VS-code, perhaps the most popular text-editor at the moment, even has a
    package called "VSpaceCode" <https://github.com/VSpaceCode/VSpaceCode> which
    provides many of the editor bindings that come with a highly popular Emacs
    distribution. Keyboard shortcuts don't only exist for complicated esoteric
    software. And while I feel Emacs is one of the best keyboard-centric interfaces
    I have ever used, I don't think it's for everyone. But VS Coda certainly DOES
    aim to be the text-editor for everyone. And while taking the time to learn how
    to do what you used to do with a mouse at the keyboard takes time I have found
    it makes a world of difference in how quickly, easily, and enjoyably I get to
    use my software.


#### <span class="org-todo done DONE">DONE</span> Version control {#version-control}

<span class="timestamp-wrapper"><span class="timestamp">[2021-01-14 Thu]</span></span>,#git

<!--list-separator-->

-  What is version control?

    There are lots of pieces of software that work this way now, but it's rare
    enough that I feel a few words on it might help those less familiar with it. I am
    talking about the ability to save your work and not worry about it, knowing you
    can always get what you just saved some day if you really need to. Some software
    calls it backups, some software calls it states, I like the way [git](<https://git-scm.com/>) calls it.

    Imagine you are writing a really simple book. Let's call it "My book".

    -   My-book.txt

    Great. Now you write a section. Let's call it A.

    -   My-book.txt
        -   A

    Once you save your work, you have lost the blank version of My-book.txt. You
    only have one current and correct version of My-book.txt. In most cases this is
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

<!--list-separator-->

-  There has to be a better way

    ..and there is. It's called version control. If the software you have supports
    it, please use it. It's really nice. And if you are into code, use git. Git is
    hard and complicated, and frustrating, and so so worth it.

    I didn't set out learning git because I wanted to learn to code. I set out to
    learn git because I wanted to learn what this "magit" thing built into [spacemacs](<https://www.spacemacs.org/>)
    was. But what I discovered was a revelation that makes [Org mode](<https://orgmode.org/>) and Emacs my
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

<!--list-separator-->

-  You want me to "push" to a "remote"?

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


#### <span class="org-todo done DONE">DONE</span> Nix packages {#nix-packages}

<span class="timestamp-wrapper"><span class="timestamp">[2021-01-23 Sat]</span></span>,#nix

<!--list-separator-->

-  An alternative packaging system

    I have been experimenting with a package system called
    [Nix-packages](<https://nixos.org/>). It's very interesting as an alternative way
    to install tools in a development environment without worrying about how it will
    affect the rest of your system. I can't explain the intricacies nearly as well
    as a blog post like
    [this](<https://wickedchicken.github.io/post/macos-nix-setup/>) but I can share my
    experience with trying it out.

<!--list-separator-->

-  First off, why nix?

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

<!--list-separator-->

-  Two examples

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
    most likely be x\_86 complied for the time being. As things move forward I am
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


#### <span class="org-todo done DONE">DONE</span> Unix layout Keyboards {#unix-layout-keyboards}

<span class="timestamp-wrapper"><span class="timestamp">[2021-01-30 Sat]</span></span>,#unix

<!--list-separator-->

-  Do you remember the last time you actually used your caps-lock key?

    I didn't really give it much thought until I started using Emacs, but I would
    love to have a control key where it is easier to use. I have been a fan of
    keyboard shortcuts for a ling time, but Emacs really was the tipping point that
    made me realize I could find a better use for my caps-lock key.

    A quick search online will pull up an article or two on "Emacs pinky" which
    apparently comes from using the control key usually found in the lower left of
    most keyboards. And considering of the more common commands in Emacs is [C-c C-c]
    or "Control-c Control-c", it makes sense that using a finger like your pinky
    that much could lead to problems. I was surprised to hear that a lot Emacs users
    used their caps-lock key in place of the normal control key...which they also
    use with their pinky.

    Then when I decided to try it (by heading into the registry settings of
    Windows 10) I realized what made the caps key easier on my pinky. It was the
    weight. When reaching down to the bottom of the keyboard to reach the normal control
    key, I was putting more of the weight of my entire hand into the gesture,
    and while holding the key down, I would tend to rest the weight of my hand on
    that pinky while I rotated the rest of my hand to connect the key to the next
    key.

<!--list-separator-->

-  Some keyboards have a UNIX layout where the usual caps key in a control key

    Late last year when I got a HHKB, I realized why keyboards like this don't
    keep their caps key in the normal place, and instead bury it in a function
    layer. Interestingly enough, so do Apple laptops in Japan. Japanese language
    input rarely needs a caps key (there is no concept of a "capital letter" in
    Japanese) so Apple decided to stick something more useful there. And since I
    started using a layout like this, I find myself using keyboard short cuts for
    more and more things.

    I read some differing opinions of people online who tired a control key where
    their caps-lock is, and found it didn't help them at all. I think it works for
    some people and not for others. But for me, I wish I had discovered it sooner.

    I was not big on the commands [C-a] for "move cursor to beginning of the line",
    or [C-e] to go to the end of the line... UNTIL I moved a control key to be right
    next to my left pinky. It's so easy now, that when I want to move my cursor back
    in a terminal to delete some text at the front of a command, I don't even think
    about it. My muscle memory pulls out command "a" and my cursor is where I want
    it to be. I use vim motions in Emacs now, but it's nice to be able to do some
    basic moves while still in insert mode.

<!--list-separator-->

-  Give it a try, you might be surprised

    If you don't want to fiddle with keybinding software or the Windows registry it
    might not be worth it for you. If you are on a Mac, there is an OS level setting
    you can use to turn your caps key into a control key (or at least there was in
    older versions of MacOS). Maybe one day the caps lock key will find a new home
    in a slightly less prominent place on the standard computer keyboard.


#### <span class="org-todo done DONE">DONE</span> Org-mode table alignment with non-latin characters {#org-mode-table-alignment-with-non-latin-characters}

<span class="timestamp-wrapper"><span class="timestamp">[2021-01-30 Sat]</span></span>,#org-mode

<!--list-separator-->

-  Org-mode tip

    This article won't mean much if you don't use or intent to use Org-mode, and it
    means even less for you if you only write in a language that uses latin
    characters. But if you do write things like おそれいれますが or 可能性 AND you
    want to put them in an Org mode table, then this is for you.

    I was using Org mode for a table at work, and I noticed that the alignment was
    off when Japanese characters were present in the table.

    ```text
    | Name | Age |
    |------+-----|
    | Bill |   3 |
    | Ann  |  30 |
    | John |  78 |
    ```

    That looks just fine, but you might see some alignment errors depending on your
    font for this next table

    ```text
    | 名前       | 年齢 |
    |------------+------|
    | ジョ       |    4 |
    | ココロ     |   29 |
    | ハビエルア |   43 |
    ```

    If that doesn't make a nice square, you might have a font that doesn't have a
    proper mono-space size for these asian characters. But there is hope for Emacs
    users. Emacs let's you set all kinds of things. Once of them is the face for
    fonts used in various places in Emacs. If you are using Doom Emacs, you can
    include something like this in your ".config.el":

    <a id="code-snippet--org-table-config"></a>
    ```elisp
    (custom-theme-set-faces
     'user
     '(org-table ((t :family "Inconsolata"))))
    ```

    Inconsolata might not be your favorite font, but this will get enough of the
    characters you need to use Japanese in an Org-mode table.

    > -   you need to view this in a mono-space font for it to look right but here goes
    >
    > ++ you may also find that you still have alignment issues if you mix characters
    > like か and "any english letter"


#### <span class="org-todo done DONE">DONE</span> Blogging {#blogging}

<span class="timestamp-wrapper"><span class="timestamp">[2021-02-13 Sat]</span></span>,#blog

<!--list-separator-->

-  Yeah I know... a blog post about blogging is kind of redundant

    ...but I do have something I feel like stands to be said again on the internet
    before someone forgets it again, or just in case someone hasn't heard it yet.
    There is gentleman by the name of Scott Hanselman who said a bunch of very interesting
    things is more than a few blog posts and a few youtube videos but one of his
    stories really stuck with me.
    I'll paraphrase what I remember from one of his talks: "If you are are going to
    give someone the **gift** of your keystrokes, don't send it in an email. Put is
    ANYTWHERE but an email. That person you emailed will read your message once and
    the information will forever be trapped on a mail server somewhere. Much better
    you put it somewhere online where someone else someday may find it. As long as
    one more person reads your words, two people for the benefit of what you typed,
    and your have doubled the effectiveness of your keystrokes."

<!--list-separator-->

-  A cool idea, and a huge motivation for this blog

    I can imagine one day someone may go looking on the interwebs for what I went
    searching for about a year and a half ago. I wish I had found a blog like the
    one I am writing now. I wish someone had told me Emacs and Org-mode was going to
    revolutionize how I work with computers and plain-text. So I am writing my
    thoughts on how I got here in the hope that one day someone if going to find this
    and have a slightly easier time finding their way than I did.

    If you are looking to get into a text editor and a markdown language that feels
    like "taking the red pill", consider giving Emacs and Org-mode a try. They are
    hard complicated tools, but they are so worth it. If you are a musician and you
    like the extensibility of software and want to manipulate data streams to make
    music, please check our MaxMSP, or at least Pure Data. And if you are typing on
    a laptop right now, please give a mechanical keyboard a shot one day. I don't
    think any of those are the perfect fit for everyone, but I would never go back
    to the way I did things before I found these tools.

    And consider putting your words out there for people to see. It's 2021 as of the
    writing of this post, and all the young kids want to be YouTubers. Nothing
    against youtube, but I can only imagine how long Google will keep all those
    videos up on their servers. But internet archives and plain text? I expect that
    information to be around for ages to come. It might take some digging to find
    what you said, but it's worth it if you can give the gift of your keystrokes to
    as many people as you can.


#### <span class="org-todo done DONE">DONE</span> Live 11 {#live-11}

<span class="timestamp-wrapper"><span class="timestamp">[2021-02-26 Fri]</span></span>,#music

<!--list-separator-->

-  Live 11 is really impressive

    I may have never mentioned it here, but I was a music major in college. Music is
    what I do, and will always be part of where most of my focus and energy in
    technology always tends towards. And last year after getting a used Roli Seabord
    I purchased repaired, I was looking forward to doing more with MPE.

    After spending my last year learning Python and working in terminals and with
    plain text, it has been really interesting getting back into a professional tool
    that is mostly a GUI. I guess you could say MaxMSP is something I have been
    working with recently that has a GUI, but it also feels like more of a coding
    tool, albeit a visual programming language.

<!--list-separator-->

-  MPE has been implemented really well

    There are still things here and there that I wish gave me a little more control,
    but I think it does a really good job of handling most of the complication you
    want it to and not force your to deal with all the configuration.

    Wavetable and the few VSTs that I own that are MPE capable work pretty well, and
    I think the fact that it feels like it's supposed to work that way instead of
    what I was doing before to fake MPE with multiple tracks on different midi
    channels.

    The new effects are nice too, and I like the sounds Spitfire Audio contributed
    to Live 11 Suite.

<!--list-separator-->

-  I appreciate it more having tired to make software myself

    I spend many days trying to get lists of things to fit into lists somewhere else,
    and to have a hardware midi controller talking to a DAW, which tells a
    synthesizer made by another company send audio back to a driver, running a
    hardware audio interface, and it all just works, I am very impressed... haha.

    It's not perfect, somethings don't work the way I would expect them to, but when
    it doesn't got right on the inside, I as the user rarely see a huge
    show-stopping complaint from my computer saying that something went wrong. MIDI
    is a stream of data, and usually a note-on message is always followed by a
    note-off message (unless something goes wrong). But sometimes things go wrong,
    and I am really happy with how well the whole system seems to handle less than
    perfect scenario.

<!--list-separator-->

-  I have a lot to learn about how to use it better

    I think when I was younger I spent more time with the software and felt I didn't
    have much to learn. Now that I spend less time with it, it feels like I need to
    work harder to get it under my fingers. But now that I think about it, I think
    when I was younger I just didn't really know how much I knew. Now that I have
    seen how deep the rabbit hole goes, I think I see a lot more depth in things
    that I thought were pretty finite and predictable.


#### <span class="org-todo done DONE">DONE</span> Fixing tools {#fixing-tools}

<span class="timestamp-wrapper"><span class="timestamp">[2021-03-07 Sun]</span></span>,#emacs

<!--list-separator-->

-  Tools are only as useful if they work the way you need them to

    Just yesterday I went to work on some Clojure code and practice some syntax I
    had just heard about, and I got an error. It wasn't a problem with my code. The
    code was fine. The problem was with my tool. The problem lied somewhere is the
    line of:

    Windows
    WSL2
    Pengwin
    Emacs
    Org-mode configuration
    Java
    Java configuration
    Clojure
    Project configuration

<!--list-separator-->

-  My Tools tend to give me issues like this quite a bit

    It's mostly due to the fact I like to use tools that are pretty cutting edge.
    Take Emacs. It might be old, but it's changing. I saw updates to packages that
    make up Emacs just a few weeks ago. All those changes invariably make for a
    problem for someone at some point down the line.

    Take a Violin by comparison. Your Violin might break a string, or need some bow
    wax, but you don't get too many problems with things like the number of strings
    changing on you. Which means you only need to worry about a few things and can
    mostly rely on your tool to work the way you expect it to.

<!--list-separator-->

-  Back to my broken Clojure code block

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

<!--list-separator-->

-  I wish more of my tools worked like this

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


#### <span class="org-todo done DONE">DONE</span> Doom Emacs {#doom-emacs}

<span class="timestamp-wrapper"><span class="timestamp">[2021-03-14 Sun]</span></span>,#emacs

<!--list-separator-->

-  Emacs configurations

    It's crazy to think that it's been only just over a year that I have been using
    Emacs. I found the software thanks to org-mode and searches on the net for a
    option for notes with power beyond simple words or reliance on an external
    company's server time. But I was warned when getting into Emacs that it was not
    for the faint-of-heart. I knew Emacs was going to be the hardest part of getting
    into org-mode, so I decided to use something to help me get up and running.
    Rather than trying to add the learning curve of Emacs onto org-mode, I decided
    to use Spacemacs.

<!--list-separator-->

-  Spacemacs is REALLY nice

    [spacemacs](<https://www.spacemacs.org/>) is something I wrote about on this blog
    before, so I won't go into it too much. Suffice to say it is a great "welcome"
    into the world of Emacs for those coming from other software like Vim
    (especially nice for people coming from Vim). There is also an episode in a
    podcast called [EmacsCast](<https://emacscast.org/episode%5F4/>) that goes into the
    differences between Emacs and what I really want to talk about today which is
    Doom. Please take a listen to that episode of you want to hear from someone who
    REALLY knows Emacs and not just a neophyte like myself.

<!--list-separator-->

-  Doom Emacs is an unfortunate name in my opinion

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

<!--list-separator-->

-  To be honest, I like the Spacemacs bindings better

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

<!--list-separator-->

-  If you want a fast Emacs configuration and don't mind Spacemacs, try Doom

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


#### <span class="org-todo done DONE">DONE</span> Hylang {#hylang}

<span class="timestamp-wrapper"><span class="timestamp">[2021-03-21 Sun]</span></span>,#python

<!--list-separator-->

-  Have you ever heard of Hy?

    Those of you who have tried a lisp, and gotten used to having things like
    multiple arguments for things like addition have probably wondered how you can
    write more lisp and less things that aren't lisp. Well as I started poking
    around the internet for Lisps that would get me close to Clojure without needing
    to deal with the JVM all the time, I came acres this language called Hy.

<!--list-separator-->

-  Lisp syntax for Python

    [Hylang](<https://docs.hylang.org/en/stable/>) is mostly just Python, but with a
    lisp syntax. It borrows bits and pieces from Clojure's flavor of lisp, and it's
    nice to see things like a Loop/recur macro for propper tail-call recursion
    despite the fact you are still running on Python. Hy can be installed as a
    python package to an existing Python run-time, and it affords some really nice
    inter-op with Python.

    Just yesterday, I decided to do a little practice and re-implemented a lowest
    common denominator function I had written in Python before:

    <a id="code-snippet--Hy-euc-lcd-tailcall"></a>
    ```hy
    (require [hy.contrib.loop [loop]])
    (defn greatest-common-demoninator [num1 num2] "Algorithm practice. Euclidean greatest common denominator."
        (if (> num2 num1) "The first number must be greater"
            (loop [[n1 num1] [n2 num2]]
              (if (= 0 n2) n1
                  (recur n2 (% n1 n2))))))

    (print (greatest-common-demoninator 259 37))
    ```

    That is what I ended up with in Hy, vesus a similar implementation in valilla
    python

    <a id="code-snippet--Euclidean-GCD-Python"></a>
    ```python
    def euclidean_GDC(num1, num2):
        """Euclidean greatest common denominator."""
        if num2 > num1:
            return "The first number must be greater"
        elif num2 == 0:
            return num1
        else:
            return euclidean_GDC(num2, (num1 % num2))


    print(euclidean_GDC(270, 195))
    ```

    They don't look that different, and to be fair the Python version is not that
    great considering it's recursive without any provision for what happens if you
    blow the stack. In a case like this, Hy doesn't provide very much that is
    different than vanilla python. It starts to become more apparent when you start
    to do more "lispy" things in your code.

<!--list-separator-->

-  So why use Hy at all?

    Well for, I don't write applications. I just write scripts. I need to call out
    to Python libraries to do stuff like parse CSV files or print out JSON into a
    format I can work within Org-mode. If I don't need to work about a team of
    people being able to read my code, Hy makes a lot of sense. I can even call
    straight python with in-line if I really need to. Maybe one day I will write
    production Python, and if that day comes I won't be able to get away with a
    Lowest-common denominator function like the one I have above.

    The way I see it, If I had a choice: use vanilla python, put up with some
    roughness and use Hy; I would rather use Hy. I don't do a whole lot with code.
    But the code I write I would love to be in the idiom that fits how I think the
    best. I quite like vanilla Python. But when I thought of how to make a function
    that calculates the lowest common denominator, this fairly function and
    recursive solution felt right.


#### <span class="org-todo done DONE">DONE</span> The nice feeling after a reinstall {#the-nice-feeling-after-a-reinstall}

<span class="timestamp-wrapper"><span class="timestamp">[2021-03-28 Sun]</span></span>,#WSL2

<!--list-separator-->

-  No, I didn't reinstall Windows

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

<!--list-separator-->

-  Git is great

    All my projects in Git were simple enough to clone back into the distro after
    wiping the old one. Setting up some SSH keys got me authenticated, and a few git
    commands later and my old files were back in place, including my Doom-emacs
    configuration files.

<!--list-separator-->

-  Nix is not so great

    Nix is supprisingly one of the most reliable ways I have found for installing
    Emacs 27 on WSL. I need to install he dependencies for Vterm from apt, but Emacs
    installs from Nix really well. I was hoping to also use Nix for Python, Java,
    and CLojure tooling, but I ran into a few snags.

    Python installed just fine, but getting packages was proving to be a pain. In
    the end I just installed Python from apt and went with pyenv for virtual
    environments. Nice intergation in Emacs too. Clojure wasn't finding the Java
    pulled in when installing from Nix, so I ended up installing SDKman and running
    the clojure installer script from their website.

    I really want Nix to replace all my packaging needs. I am thinking abot heading
    back to a Mac soon, and I would love to be using Nix for package management over
    something like home-brew.

<!--list-separator-->

-  Emacs was up and running pretty quickly

    Some of the older things I use like skk mode for Japanese text entry gave me
    some problems re-installing, but it didn't take that long. I am still ironing
    out some road-bumps when it comes to upstream branches and maggit. Doom emacs
    was easy to reinstall, and my config got me up back to my old setting very
    nicely.

<!--list-separator-->

-  Clearing out old unused software makes the whole thing "feel" faster

    I haven't done any tests, but it feels faster. The load times on the Doom emacs
    dashboard say my load times are faster, but I don't hold that a re-install
    always make things faster. But I do think that it's nice to clear out old config
    files that don't need to be there any more, and generally help you see what you
    were really using.

<!--list-separator-->

-  If you are scared to reinstall, something is wrong

    Computers crash, software breaks. If something went critically wrong on your
    computer, how hard woudl it be to get it working again? Have you gone through
    the steps of what it would take to get everything back? Do you know you would
    have evrything back?

    It's like spring cleaning. It doesn't need to be everyday, but once in a great
    while wiping everything and seeing if you can really put it all back together
    can help you learn a lot about your system and how it works.


#### <span class="org-todo done DONE">DONE</span> Algorithm practice {#algorithm-practice}

<span class="timestamp-wrapper"><span class="timestamp">[2021-04-05 Mon]</span></span>,#coding

<!--list-separator-->

-  Thinking in algorithms is hard

    For the coders out there reading this, maybe you have forgotten what it is like
    to first wrap your head around some really basic ideas and concepts when it
    comes to talking to computers, but I am in the middle of learning about different
    programming languages, styles, and algorithms. As much as I think I have a
    handle on things, I find that I still have a ways to go, especially when it
    comes to algorithms.

    I remember watching a talk called C++ seasoning, or something like that. It is
    apparently a rather famous C++ talk about not reinventing the wheel and using the
    algorithms that your language provides. I don't intend to teach my self and C++,
    and I don't think I will ever need to go that deep into a computer. But I DID
    find what he said to be very interesting and it helped me think about how I
    work with my languages.

    Right now I am teaching myself Lisp and Python. Technically it's more like;
    Elisp, Hylang, Clojure, and Python, but Hylang is just a Clojure like lisp
    syntax for Python, and Clojure is modern lisp while Elisp is an older lisp used
    almost exclusively for talking to Emacs, so I really only think of those three
    lisps and "just learning lisp". And with Lisp and these dynamic higher level
    languages, I don't need to re-invent the wheel. Clojure and Python have amazing
    standard libraries, and I don't need to make a sorting algorithms in most cases.
    It's usually made for me. And they have usually implemented it in a way that is
    faster than I could make it myself.

    Take NumPy for example. A lot of NumPy calls to C, and can run a lot of math
    much faster than I can tell the Python run-time to do it. So rather than trying
    to make it from scratch, I can get a lot of performance simply by using the
    tools in NumPy or even the standard library.

<!--list-separator-->

-  But I could stand to learn about algorithms too

    ...so I found a few websites with algorithms that beginner coders can learn. I
    have recently made a binary search, a greatest common denominator, and today I
    WAS going to try to make a bubble sort, but ran into the limitations of my
    understanding of algorithms.

    Coding is like a muscle. The more you use it, the stringer it gets. And I am
    beginning to see how I have a long ways to go. Bubble sorts are apparently
    rather inefficient and mostly used just for teaching people like me, but I took
    the problem and made a bit of a mes of it.

    Having learned about functional programming, I decided I would try to make a
    bubble sort that was sort-of functional. Not a good idea. The whole mechanism of
    the sort is swapping elements in an array, that is a mutation of state. I was
    trying to make some recursive calls to local variables in Elisp to get it all
    working, and ended up making something that took hours to type and didn't look
    neat, clean, elegant, or fast.

    And when I think back on how I got there, I see how I just don't have a lot of
    practice breaking a problem down into parts I can handle with built in
    algorithms. "car" "cdr" and "cons" were serving me well, but I also could have
    been done in a few seconds with a standard library call to a sort function.
    Learning how to express these ideas in code is a nice tool in the tool belt to
    have. I also see how much work things like a standard library can save me if I can
    learn to use it well. And if I find a problem is turning into something like
    this, it could be that I am just overlooking a built-in that could save me some time.


#### <span class="org-todo done DONE">DONE</span> A "forced technologist" {#a-forced-technologist}

<span class="timestamp-wrapper"><span class="timestamp">[2021-04-11 Sun]</span></span>,#coding

<!--list-separator-->

-  You know you aren't a coder when...

    ...you give up on a perfectly good languages because it doesn't work with
    Org-babel code blocks the way you want it to. Does that sound like you? Maybe
    not, and lots of people like Clojure just fine. I still think it is a great
    language that I would love to use more one day once the tooling catches up with
    what I want to do. I did get REALLY close to what I wanted, but Clojurescript,
    node, and other factors are making it hard to keep at Clojure. I think what
    really made me decide to shift my focus away from Clojure was the realization I
    was spending more time figuring out the tooling than I was programming. And
    without any projects written in Clojure, I have very little to get me to stick
    with the languages.

<!--list-separator-->

-  Python is a better fit

    Python is not perfect. The fact I am having so much fun in a language like Hy is
    a testament to the fact I didn't really need Clojure. I don't feel the need to
    write purely functional code, reach into the JVM or Javascript worlds, or live
    in the Clojure repl. I mostly make things with Org-babel blocks, and Python has
    been serving me well. I have two tools written in Python and some bash that help
    me get my day job done even though I am not a coder. And I could have written
    these in Clojure. But I wrote them in Python. And the reason I made them in
    Python is simply because Python was easier.

    I don't need fast code. In fact, I have been teaching my self about functional
    programming and writting things without loops (which can often be the faster
    way of dealing with iteration). And Hy is not about speed either. I am mostly
    writting small scripts. A performance hit only costs me a few seconds most runs.
    Maybe one day I will need code that is fast.

<!--list-separator-->

-  And I hear there are options for fast Python

    I have recently been hearing about things like Cython, Numba, and just the
    simple change of moving computation heavy math in Python to NumPy and how it can
    help speed up code that would other wise be slow in vanilla Python. But what is
    good about these tools is it's mostly still python. How nice to keep most of the
    flexibility I have learned to enjoy, and just contrain myself to some performant
    stuff when I know I am going to need it. And all the while getting to stick with
    a single language. Plus I get to use the one library that seems to creep up here
    and there: Pandas. So long as most of my work at work is given to me, and
    expected of me in tabular data, Pandas is a great way for me to start harnessing
    the power of code to not write as many cells in a google spreadsheet.

<!--list-separator-->

-  So long and thanks for all the fish

    It's not good-bye to Clojure. I do expect I might be able to get it working with
    Org-babel once I get homebrew and Planck on a Mac to work, but this is so long
    for now. I think after about a year of learning Python and trying to add
    another language because I think I need something fast, I think exploring
    options like Numba are a nice intermediate step, and probably as far as I need
    to go.

    Expect a blog post or two about Numba over the next month or so. If it turns out
    I can just write a block in Org babel with a @jit decorator and call that block
    from Hylang blocks with the rest of my code... I am going to be pretty stoked. I
    am not a technologist because I like technology, it's more like I see a problem,
    and the best way I know how to solve it requires a little bit of Python. So if
    Python is all I need, maybe I will leave Clojure to the lispers and stick to
    Hy.


#### <span class="org-todo done DONE">DONE</span> WSL2 a year or so later {#wsl2-a-year-or-so-later}

<span class="timestamp-wrapper"><span class="timestamp">[2021-04-19 Mon]</span></span>,#wsl

<!--list-separator-->

-  WSL2 has been really fun to work with

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

<!--list-separator-->

-  I am sure some of these issues are just growing pains for WSL

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

<!--list-separator-->

-  I could just look for another way to get information into Max

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


#### <span class="org-todo done DONE">DONE</span> Back to Spacemacs {#back-to-spacemacs}

<span class="timestamp-wrapper"><span class="timestamp">[2021-06-14 Mon]</span></span>,#emacs

<!--list-separator-->

-  Doom is still really nice for what it does.

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

<!--list-separator-->

-  Spacemacs has it's issues too

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
    sub-string function. I hope you find it useful someday. I am sure I will one day.


#### <span class="org-todo done DONE">DONE</span> Hylang is really nice {#hylang-is-really-nice}

<span class="timestamp-wrapper"><span class="timestamp">[2021-09-20 Mon]</span></span>,#hylang

<!--list-separator-->

-  Took a break from blogging

    It's been a while since I have posted, but the summer gets rather busy at
    my current workplace and I have been playing catch-up with a bunch of
    stuff. Reason Studios (formerly Propellerhead software) released Reason 12,
    and I have been very happily learning all about the new devices and playing
    with Reason sounds as a VST. I hope to not just blog about that soon, but
    also finish some music with it and show what has me so excited about that.

    But today's post is not about Reason, it's about Hy. And the reason being I
    have been learning more about Python and functional programming and I am
    starting to see what makes Hy so cool.

<!--list-separator-->

-  Hy can look and work A LOT like vanilla Python

    Consider the following:

    <a id="code-snippet--Two-sum"></a>
    ```python
    from itertools import combinations

    problem_list = [0, 9, 2, 32, 4, 52, 3, 7]
    problem_target = 6
    my_gen = combinations(problem_list, 2)
    current = next(my_gen)

    while sum(current) != problem_target:
        current = next(my_gen)

    print(list([problem_list.index(current[0]), problem_list.index(current[1])]))
    ```

    And this:

    <a id="code-snippet--two-sum-hy"></a>
    ```hy
    (setv problem-list [0 9 2 32 4 52 3 7])
    (setv problem-target 6)
    (setv hy-gen (combinations problem-list 2))
    (setv current (next hy-gen))

    (while (!= (sum current) problem-target)
      (setv current (next hy-gen)))

    (print [(.index problem-list (first current)) (.index problem-list (nth current 1))])
    ```

    So it's not exactly the same. The second bit of code sure has a lot pore
    parenthesis. But the way the code in each does the work is REALLY close. And for
    those who don't recognize, this is an attempt I made at a Leet code problem
    where you need to return the indecies of the two numbers in the list that add up
    to the "target". The way I solved it was not efficient at all. This is about as
    "brute force" as you can get. I just guess and check and stop when I get the
    answer. But the problem was simple enough that I decided to do it in two
    languages, and I was really surprised at how easy it was to take something I was
    doing in Python and just write that out in a Lisp.

<!--list-separator-->

-  Why would you want to do this?

    I found a blog post online by this gentleman who was talking about CLojure
    and Python. CLojure is still something I poke at, but can't really get my
    head around the environment. I have always found Python to be pretty simple
    to get running, and I found the comparison between the two to be very well
    done. Clojure makes concurrent code easy and provides a very nice standard
    library for writing functional code without needing to be like Haskel.
    Python is a dynamic language that can look pretty function, and is very
    quick to write, while tending to not be as speedy when running (compared
    with things on the JVM).

    Hy lets me use a lot of things that look A LOT like Clojure without
    actually needing to run a JVM. And yes, I tried Clojurescript and Node was
    not making things that much easier. I still want to get ClojureScript under
    my belt for working with MaxMSP, but Hy is proving to be something that my
    head has a very time getting a grasp on... despite the parenthesis.

    The solution to the Leet Code problem I cam up with was not particularly
    functional. Lots of variable assignment, and a less than ideal while loop.
    But it showed me that if I needed to, I could use Hy to write Lisp that was
    not so functional and easier to use along side other code that was written
    in more OO or procedural style.
