+++
title = "MaxMSP hold switch"
author = ["Robert Clay"]
date = 2021-01-03
lastmod = 2024-08-14T08:52:56+09:00
categories = ["topic"]
draft = false
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-01-03 Sun]</span></span>,#MaxMSP


## Making your own tools can be a rewarding challenge {#making-your-own-tools-can-be-a-rewarding-challenge}

Being a computer musician, I appreciate the ability to work with data as it suits me. I don't need to just accept a stream of midi and ask a software synthesizer to make sounds for me. I can manipulate that stream of data in interesting ways before I put it to use. One such use I found for this manipulation is replicating a feature of a keyboard I sold a few years back.

I used to own a Roland JD-XA. It was a real analogue synth with some modern and cool features. Sadly, my audio recording set up was not up to doing it justice, and I ended up using it mostly as a controller. I sold it to get a Roli Seaboard instead and I am very happy with it. But I did miss a button on its front panel; the "hold" switch that went with the arpeggiator. The switch when used with the arpeggiator let you hold out the notes in a sequence even when you took your hands off the keys, but I liked the fact it wasn't tied to the arpeggiator itself. When it wasn't used with the arpeggiator, it acted like an "auto-sustain-pedal". Notes played legato were all sustained, and a new "set" of notes would trigger a re-pedal and the next set of notes would sustain while the old notes would stop. It was super fun to use in conjunction with a two tier keyboard set up. I could play a piano like patch in my lower keyboard while the top board would be set to some sustaining patch that I could play a few notes on without needing to stand on a sustain pedal the whole time.

I was thinking I might be able to get something similar from other arpeggiators, so I didn't think much of it when I sold the board. But after a few attempts with a few arpeggiator plugins, I quickly realized that this wasn't how most arpeggiators worked. But I also knew I had Max4Live. I figured I could just make my own.


## What I wanted to make {#what-i-wanted-to-make}

Before I get into how I started trying to make this, I want to spell out exactly how it was supposed to work.

-   A "mode" needed to be enabled and easy to turn off.
-   That mode needed to know when notes were still being played or not
-   All note offs needed to be captured and handled in a special way
-   If there were no notes being held, a list of note offs for the currently sustaining notes would be to be calculated and sent before the new note on.

On the surface it seemed to be a really simple problem. Very clear order of operations, nothing that was too complicated, I thought it would take me 30 minutes to whip something up. Boy was I wrong.


## The first few tries did not go well {#the-first-few-tries-did-not-go-well}

My first attempt quickly spiraled out of control into a mess of complexity.
Generating a list of notes that were currently being held down on a keyboard
connected to this utility proved really hard to make and deal with. I had
considered making a dictionary where I added note-on events as entries and
note-off events as a sign to remove the entry. But having worked with some
Clojure at this point I wanted a solution that didn't rely on something mutable like this "dictionary" I was planning on using. Writing the "state of the midi stream" with each new event lead to a huge mess of operation order. Do I read the dictionary before of after I compare the note coming in to the others to see if it's a note already in the list? Should the dictionary read be part of the clean up at the end of the chain? When does the note off list get generated? How I can generate that list without having the dictionary pass its contents all over the place? Do I need the contents of the dictionary in multiple places? It was a disaster.

Imagining the problem was Max, I proceeded to wire up Max and Node and ClojureScript, hoping that a different language would have better support for what I was trying to do. But after spending more time with Max, I found a better way forward.


## But then I found out Max had already solved the problem for me {#but-then-i-found-out-max-had-already-solved-the-problem-for-me}

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


## The MaxMSP object for those interested {#the-maxmsp-object-for-those-interested}

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
