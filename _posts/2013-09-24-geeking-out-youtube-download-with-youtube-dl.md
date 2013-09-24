---
layout: post
title: "Geeking out YouTube video download with youtube-dl"
date: 24 September 2013
comments: false
categories: Blogging
---

I bumped in to this utility when I updated my Homebrew formulas and found it's super easy to download YouTube videos without the help of any thirdpary browser plugins or website

This work in Windows, Linux and Mac; or in other words wherever you can run Python. You can [download it from Github for your platform](http://rg3.github.io/youtube-dl/). I go for Homebrew way with my Mac.

## Installation

`$ brew install youtube-dl`

## How to download 
It's simple two step process if you don't know the resolution code. and it's just a command if you can provide the resolution to download or just let it download in the SD  resolution.


```

$ youtube-dl -F <youtube url> # lists information about video

$ youtube-dl --console-title -f 37 <youtube url> # Download

```

Here's a complete output of a sample video

Saraths-MacBook-Air:Downloads sarat$ youtube-dl -F http://www.youtube.com/watch?v=vNJhTqh4cmo
[youtube] Setting language
[youtube] vNJhTqh4cmo: Downloading video webpage
[youtube] vNJhTqh4cmo: Downloading video info webpage
[youtube] vNJhTqh4cmo: Extracting video information
Available formats:
37	:	mp4	[1080x1920]
46	:	webm	[1080x1920]
22	:	mp4	[720x1280]
45	:	webm	[720x1280]
35	:	flv	[480x854]
44	:	webm	[480x854]
34	:	flv	[360x640]
18	:	mp4	[360x640]
43	:	webm	[360x640]
5	:	flv	[240x400]
36	:	3gp	[240x320]
17	:	3gp	[144x176]
137	:	mp4	[1080p] (DASH Video)
136	:	mp4	[720p] (DASH Video)
135	:	mp4	[480p] (DASH Video)
134	:	mp4	[360p] (DASH Video)
133	:	mp4	[240p] (DASH Video)
160	:	mp4	[192p] (DASH Video)
141	:	mp4	[256k] (DASH Audio)
140	:	mp4	[128k] (DASH Audio)
139	:	mp4	[48k] (DASH Audio)
Saraths-MacBook-Air:Downloads sarat$ youtube-dl --console-title -f 37 http://www.youtube.com/watch?v=vNJhTqh4cmo
[youtube] Setting language
[youtube] vNJhTqh4cmo: Downloading video webpage
[youtube] vNJhTqh4cmo: Downloading video info webpage
[youtube] vNJhTqh4cmo: Extracting video information
[download] Destination: Enthanu Bhai - Da Thadiya-vNJhTqh4cmo.mp4

```
