---
layout: post
title: Raspberry Pi fun and games
date: '2014-08-29T22:24:00.000-07:00'
author: BikeBoy
tags: 
modified_time: '2014-08-29T22:24:10.777-07:00'
blogger_id: tag:blogger.com,1999:blog-5444398.post-835254108551583538
blogger_orig_url: http://blog.chadfrost.com/2014/08/raspberry-pi-fun-and-games.html
---

While I continue to find good uses for Arduinos and such small 
microcontrollers, lately I've been playing around quite a bit with the 
Raspberry Pi. I got one last year, and fairly quickly set it up to be my 
surrogate Dropbox, using BTSync. It has been happily chugging along in that 
role ever since, connected to a small 100GB hard drive and living on my 
workbench in the garage. 
<!--more-->
I also picked up a Pi at work, to drive a slideshow on a big screen in our 
lobby, and at trade shows and conferences. That's worked quite well, using 
'fbi' as a lightweight image display tool -- the Pi boots up, and immediately 
looks for a slideshow directory on a USB stick from which to display a 
sequence of images. For a recent conference, I added an open WiFi network that 
served up PDFs of our organization's papers -- anyone could connect to the 
network, and immediately download our papers, on the spot. 

The latest distribution of Raspbian (the most common variety of OS for the Pi) 
includes Wolfram's "language" and Mathematica -- which are great tools, but 
not inexpensive for the desktop versions. I thought it would be interesting to 
see how they run on the Pi, and set out to do an installation. I promptly ran 
into my need for a decent HDMI-driven display; the HDTV we have is an older 
CRT, progressive-scan model, and the image quality for computers is poor. I 
have a couple VGA and DVI monitors, but the HDMI-VGA converter I bought for 
the Pi doesn't play well with the monitor, and I don't have an HDMI-DVI 
converter. That leaves me stuck with the TV, which makes me squint and guess 
at what's on the screen. 

Add to that, the only keyboards I have around that have actual USB cables on 
them, have assorted non-functioning keys, as I discovered in the course of 
trying to use them to configure the Pi. Said keyboards are now in the pile 
destined for electronics recycling... 

I did eventually get things working, but found Mathematica's UI to be a bit 
too slow when running on the Pi. I'll have to go back and try it on the 
command line for comparison. 

That exercise led me to want some indication of what the Pi thought its IP 
address was, post-boot. It's hard to connect to something being recalcitrant 
on the network, without any idea of its address. Adafruit has a nice 
step-by-step for adding a 16x2 display, and I happened to have all the parts 
on hand, so I started breadboarding it. However - there are some software 
installations needed on the Pi, and in the present configuration I could 
_connect_ to the Pi, but it wasn't on the Web. 

Which led to figuring out how to share the wifi connection from my dev laptop 
(10+ years old, Pentium 4, running #! slowly but adequately) to the Pi over 
ethernet.... This turns out to be ridiculously easy on the Linux side, but 
requires the Pi to be set up with a static IP on boot in order to "just work", 
at least the way I went about it. But: success! I can plug the Pi into an 
ethernet cable, plug that into the laptop, and log into the Pi - which can now 
see the web, so I can easily install software onto it. 

So, having downloaded and installed a plethora of software libraries on the 
Pi, I could finally try making something display on the LCD. Since the 
[Adafruit 
tutorial](https://learn.adafruit.com/downloads/pdf/drive-a-16x2-lcd-directly-with-a-raspberry-pi.pdf) 
was written, though, their [library 
code](https://github.com/adafruit/Adafruit_Python_CharLCD) has changed; the 
wiring described in the tutorial doesn't work with the current examples 
packaged with the library, so the LCD shows signs of life, but never actually 
does anything useful unless you get the wiring sorted. I eventually figured 
this out, and now have it all happily working - the LCD displays time &amp; IP 
address, updated every 2 sec. Hoorah! 

For future reference, and in case anyone stumbles across this post having run 
into the same issue, the correct connections between the LCD and Pi are (for a 
Pi model B): 

    LCD pin 4 = Register Select = lcd_rs = GPIO pin 27 
    LCD pin 5 = Read/Write = ground (so we don't inadvertently put 5V into the Pi's GPIO!) 
    LCD pin 6 = Enable = lcd_en = GPIO pin 22 
    LCD pin 11 = Data bit 4 = lcd_d4 = GPIO pin 25 
    LCD pin 12 = Data bit 5 = lcd_d5 = GPIO pin 24 
    LCD pin 13 = Data bit 6 = lcd_d6 = GPIO pin 23 
    LCD pin 14 = Data bit 7 = lcd_d7 = GPIO pin 18 

Planned future experimentation with the Pi: I really would like to try running 
Forth on it... 
