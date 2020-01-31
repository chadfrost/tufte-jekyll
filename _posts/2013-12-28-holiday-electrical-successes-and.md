---
layout: post
title: Holiday Electrical Successes and Failures
date: '2013-12-28T18:31:00.000-08:00'
author: BikeBoy
tags:
- electronics
- cooking
- repair
- projects
- sous vide
modified_time: '2013-12-28T18:32:58.598-08:00'
thumbnail: http://4.bp.blogspot.com/-lby-6POHLV4/Ur-G7PR76MI/AAAAAAAABuA/KYl26RZC4FU/s72-c/Chad+Frost%E2%80%99s+_IMG_2784.JPG
blogger_id: tag:blogger.com,1999:blog-5444398.post-6768081262598945659
blogger_orig_url: http://blog.chadfrost.com/2013/12/holiday-electrical-successes-and.html
---

As I'm rattling around the house the past few days recovering from a really 
poorly-timed evil cold/cough, not feeling well enough to actually go out and 
do anything but not so bad that I'm flat-out in bed, I figured I'd catch up on 
some projects. 

{% maincolumn 'assets/img/sous-vide-setup.jpg' 'My DIY sous-vide setup.' %}
<!--more-->

I got all the parts in before Christmas to do an add-on for Anna's sous vide 
cooker that I built a while back. Anna wanted the ability to do sous vide in a 
smaller container, so we ordered a cheap hotplate, an aquarium pump, an 
additional PT100 temperature sensor, and some spring clamps. In this add-on, 
my existing PID controller box would be used to run the hot plate; when I 
built the controller box, it was with the intent that it could be used to 
control other things, so it has a 1/4 phono jack as the temperature sensor 
input, and a couple of 120V wall outlets (one switched by the PID, the other 
always on). The aquarium air pump will be used to bubble air in the sous vide 
bath, to keep the heat even. 

I soldered up the PT100 to a 1/4" stereo phono plug I had from the previous 
sous vide, plugged everything in, and re-calibrated the PID to the new setup. 
Looks like it will work great! 

On to the next project. 

{% maincolumn 'assets/img/transformer.jpg' 'The guts of the old Ikea transformer.' %}

The Ikea halogen track lights in our office went out just before Christmas. I took 
the power supply apart, and it's just a rectifying transformer of the cheapest 
sort - should be very easy to replace. 

For curiosity's sake, I broke open the case of the transformer. From the 
photo, you can see that the circuit board is populated with through-hole 
components, like you'd typically see in a DIY kit or something cooked up in my 
garage -- not seen in consumer electronics much since the early 1980s. Why? 
Because building it this way depends on human labor, not machinery, and there 
are still places in the world where that's by far the cheapest way to do it. 

Exploitation of workers aside, this box does a pretty straightforward job, 
converting 120VAC into 12VDC, with some nice fringe benefits like turning on a 
bit gently so as to not shock the poor halogen bulbs, and perhaps a safety 
feature or two (like a tiny, non-replaceable fuse...) 

Finding a replacement online was easy. Finding one that looked like it would 
be a drop-in replacement, *and* had at least a few reviews that didn't read 
like "DOA", "worked for a week and then died", "stay AWAY from this!" and the 
like, proved harder. I settled on a power supply that seemed to have decent 
reviews, and wasn't the cheapest of the pile, and ordered away. (Power 
supplies like this seem to run from about $10, to $60... a replacement Ikea 
lamp is about $80. I opted for a ~$20 part.) 

The power supply arrived today, and I was eager to alleviate the darkness that 
has pervaded the office for a few weeks now. I wired it in to the lamp, and 
fired it up. 

Hm. Looks a bit... dim. Anna agrees. 

#@$%&amp;! 

I fire up the 'scope to see what the heck this thing's putting out... and holy 
moly, that's an ugly waveform! But, it's driving lamps, so it really shouldn't 
matter too much, as long as it's about the right shape. 

{% maincolumn 'assets/img/transformer-scope-1.jpg' 'Zoomed in... not very clean.' %}

{% maincolumn 'assets/img/transformer-scope-2.jpg' 'Zoomed out, it’s 
still pretty ugly. But, sine-like. With some filtering to take out the HF 
stuff...' %}

{% maincolumn 'assets/img/transformer-scope-3.jpg' 'It doesn’t look too 
bad. But check out the voltage -- this is why the lights were so dim!' %}

The new power supply is only supplying about 6V, peak-to-peak, running 5 x 20W 
bulbs. It's a 150W supply, so it should be OK with that load. I tried running 
1 x 10W bulb, and it really didn't care for that... not enough load I think. 
Next, I tried 3 x 20W -- and got pretty much the same as for 5 bulbs. Crumbs. 
I'll be sending it back, and now I have to find a different power supply and 
throw the dice again. 
