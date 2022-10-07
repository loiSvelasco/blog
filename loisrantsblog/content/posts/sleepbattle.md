+++ 
draft = false
date = 2022-10-06T20:39:37+08:00
title = "Go to sleep with no lingering thoughts"
description = ""
slug = ""
authors = ["Louis Velasco"]
tags = ["self", "programming"]
categories = []
externalLink = ""
series = []
disableComments = true
+++

### It's a pain.

>Disclaimer:
>
>I’m writing this while under the influence of alcohol. I’m tired and wanted to get the most of my Friday night.

Last night, I was doing some work on a raffle-draw system with thousands of participants. It had around ~5k + people. With less than 24 hours left to finish the job and being confident with the work I’ve done (around 70% of the code), I went to sleep, which was a mistake.

Here was my ideal scenario:

{{< mermaid >}}
flowchart LR
    1(Go to bed) --> 2(Close my eyes) --> 3(Magically fall asleep)
{{< /mermaid >}}


But what happened was, 

{{< mermaid >}}
flowchart LR
    1(Go to bed) --> 2(Close my eyes) --> 3(Discover an error)
    3 --> 4(Think of a solution) --> 5{Problem solved?}
    5 --no--> 4
    5 --yes--> 3
{{< /mermaid >}}


Yes, I slept with an endless loop on my mind last night. Fortunately, I was able to resolve all the issues with plenty of time for testing. I really was tempted to just get out of bed and work on it just to have decent sleep. and I was really amazed at how much thinking about coding hinders sleep.


The event went smoothly, and there were hiccups with the system, but mostly because of the lack of internet connection. AJAX requests took too long to respond, which made the system look slow, but when operating under normal conditions with a decent connection, it works flawlessly.


The infinite errors I found while pondering it on my bed the other night were really simple to solve when I woke up. Maybe this is a lesson too, that you don’t think of solutions when tired. I'm not sure, but I discovered I work well with code when I’m focused and sharp. That goes for all of us who work in software engineering though, but meh, at least now I know it works for me.
