---
layout: post
title: Fighting with FTP
date: '2009-04-08T15:18:00.000-07:00'
author: BikeBoy
tags:
- technology
- rant
- chad
modified_time: '2009-04-08T15:56:15.865-07:00'
blogger_id: tag:blogger.com,1999:blog-5444398.post-5084490665484518703
blogger_orig_url: http://blog.chadfrost.com/2009/04/fighting-with-ftp.html
---

Some things should just be easier than they are... 

Anna has a bunch of GigaPan images she created, and wants to get them to the 
museum to be printed out giganto-size for the upcoming open house. Well, 
GigaPans are aptly named -- each one is 2-3GB in size! Putting 'em on a flash 
drive just isn't practical; only a couple will fit on a DVD; and I didn't have 
an extra USB hard drive ready to go. 

No problem, I thought -- my nifty new network attached storage (NAS) has a FTP 
server built in to it! I can just fire that up, and we'll be off to the races. 
Yeah, right. 
<!--more-->

Step 1: turn on FTP server. This part *was* easy! 

Step 2: check that it works. OK, slightly more complicated: the NAS sits on my 
local network, so the router has to be configured to direct incoming FTP 
requests to the NAS. Testing that it works means connecting to a remote 
server, then trying to connect back from there. No big deal, except it doesn't 
work -- until, after 30 min, it does. Grrr. 

Step 3: put the gigapan files on the server. The files are on Anna's work 
laptop, which has wireless access -- yeah, it will take all night to transfer 
the files because I still only have 802.11b, but there's time. Oops, forgot 
we're dealing with a *windows* laptop here... it drops the connection after 
the 4th file. Doh! Yes, I should have plugged it in to the network, but all 
the ports on my switch are being used and this just seemed... easier. 

Step 3a: find a HD to get the files off the laptop: Three of three that I have 
at home are formatted for Mac... only the third one has contents disposable 
enough to warrant re-formatting. But at least with the files copied off onto 
the HD, if this little FTP experiment fails utterly, there's a reasonable Plan 
B. 

Step 3b: copy files from HD onto NAS: should be straightforward, but while 
doing this I notice that web browsers are having a hard time connecting to the 
FTP server. Much pondering and testing ensues... Using a browser (Firefox, 
Safari, Explorer) works fine on the internal network, but hangs ungracefully 
if the connection is from the outside. Regular 'ol FTP clients work fine, 
regardless. A clue is that Lynx (a text-only browser) works where the others 
fail. 

Step 4: What is wrong with the browsers?!?! A digression, but it was a real 
stumper. Turns out all the failing browsers prefer "passive" FTP, which 
appears to be problematic in my particular configuration of routers and 
devices and FTP server. Explorer can be made to default to "active" FTP 
connections, but Firefox is just stuck unless a plug-in is installed. At least 
the problem is known/understood (if not readily fixable) so off to the next 
step... 

Step 5: Write & test foolproof instructions for Windows command-line ftp. 
Annoying, but this just reinforces the superiority of the command line, as far 
as I'm concerned. I hope the folks on the other end are successful in 
retrieving the files! 

This whole thing really should have taken 30min, tops... instead, I bet it 
took 6 hours -- 4 last night, and a couple more this morning -- before it was 
all done. 
