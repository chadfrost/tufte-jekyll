---
layout: post
title: Why is my DSL so slooooooow?
date: '2008-12-11T18:27:00.000-08:00'
author: BikeBoy
tags:
- technology
- numbers
modified_time: '2008-12-11T23:15:34.848-08:00'
blogger_id: tag:blogger.com,1999:blog-5444398.post-2799628142214310027
---

Our house is a bit far from the switch, so the speed's never been great, but lately it's really bad: 

[<img border=0 src="http://www.dslreports.com/im/62755719/8689.png">](http://speedtest.dslreports.com) 

Curiously, Speakeasy.net's own speed test gives very different results: 
[http://www.speakeasy.net/speedtest/](http://www.speakeasy.net/speedtest/) 

<!--more-->

To SF 

> Download Speed: 1293 kbps (161.6 KB/sec transfer rate)  
> Upload Speed: 330 kbps (41.3 KB/sec transfer rate) 

To LA 

> Download Speed: 1087 kbps (135.9 KB/sec transfer rate)  
> Upload Speed: 331 kbps (41.4 KB/sec transfer rate) 

To DC 

> Download Speed: 580 kbps (72.5 KB/sec transfer rate)  
> Upload Speed: 326 kbps (40.8 KB/sec transfer rate) 

A perhaps more reliable (or non-biased) tool: 
[http://netspeed.stanford.edu/](http://netspeed.stanford.edu)  

>  TCP/Web100 Network Diagnostic Tool v5.4.12  
>  click START to begin  
>  Connected to: netspeed.stanford.edu  --  Using IPv4 address  
>  Another client is currently being served, your test will begin within 45 seconds  
>  Checking for Middleboxes . . . . . . . . . . . . . . . . . .  Done  
>  checking for firewalls . . . . . . . . . . . . . . . . . . .  Done  
>  running 10s outbound test (client-to-server [C2S]) . . . . . 327.0kb/s  
>  running 10s inbound test (server-to-client [S2C]) . . . . . . 896.72kb/s  
>  Your PC is connected to a Cable/DSL modem  
>  Information: Other network traffic is congesting the link  
>  [S2C]: Packet queuing detected 

Running it again gives:

>  running 10s outbound test (client-to-server [C2S]) . . . . . 327.0kb/s  
>  running 10s inbound test (server-to-client [S2C]) . . . . . . 251.51kb/s 

...I generally seem to be getting ~800-900kb/s inbound on this test, with 
repeated attempts. 

From [http://members.cavtel.net/speed/](http://members.cavtel.net/speed/)

> Your line speed is: 172.89 kbps 
