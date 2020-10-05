---
title: What a time to be alive
author: Moldovanu Codin
type: post
date: 2015-08-24T21:23:50+00:00
url: /what-a-time-to-be-alive/
dsq_thread_id:
  - "6019705036"
categories:
  - Arduino
  - Linux
  - Tech
tags:
  - "360"
  - arduino
  - board
  - controller
  - dongle
  - free60
  - linux
  - linux on xbox
  - pc
  - rf
  - rf board
  - technology
  - to
  - ubuntu
  - wireless
  - xbox
  - xbox360

---
What a time to be alive, indeed. Technology has evolved so much, you can now do basically anything with just a few parts, regardless of the complexity of the project. From the mere and common resistor to the ESP8266 module, things have changed pretty fucking fast. IoT, Cloud, FW, whatever &#8211; we&#8217;re now used to seeing these abbreviations everywhere, although if you&#8217;d have told me 5 years ago that I&#8217;ll do 70% of my business in front of a PC, I would not have believed that.

<!--more-->

A long time ago I bought an Xbox360, sold it and later on bought a RGH&#8217;d Xbox360 (basically an Xbox that has its CPU jacked in a cycle and allows you to run unsigned code). I played for a while on it and recently I built a PC gaming rig, therefore the Xbox started gathering dust on a table. I wanted to game on the PC using the xbox controllers, and did not want to actually shell out 20$ for the wireless dongle, so I did what anyone with a internet connection would&#8217;ve done&#8230;I hacked myself together a wireless dongle for the PC.

&nbsp;

I ordered a 30RON (circa 7$) &#8220;borked&#8221; RRoD Xbox360, and took the RF board off of that, created two PCBs to stick in the original connector, soldered some wires, flashed some firmware to an Arduino and connected the RF board to the COM port on my motherboard, so everything would be stealthy. Ta-da ! It works.

[<img loading="lazy" class="alignnone size-large wp-image-89" src="http://codin-moldovanu.com/wp-content/uploads/2015/08/DSC_8572-1024x681.jpg" alt="DSC_8572" width="1024" height="681" srcset="https://codin.ro/wp-content/uploads/2015/08/DSC_8572-1024x681.jpg 1024w, https://codin.ro/wp-content/uploads/2015/08/DSC_8572-300x199.jpg 300w, https://codin.ro/wp-content/uploads/2015/08/DSC_8572-752x500.jpg 752w" sizes="(max-width: 1024px) 100vw, 1024px" />][1] [<img loading="lazy" class="alignnone size-large wp-image-90" src="http://codin-moldovanu.com/wp-content/uploads/2015/08/DSC_8573-1024x681.jpg" alt="DSC_8573" width="1024" height="681" srcset="https://codin.ro/wp-content/uploads/2015/08/DSC_8573-1024x681.jpg 1024w, https://codin.ro/wp-content/uploads/2015/08/DSC_8573-300x199.jpg 300w, https://codin.ro/wp-content/uploads/2015/08/DSC_8573-752x500.jpg 752w" sizes="(max-width: 1024px) 100vw, 1024px" />][2]

Now, I was left with a full RGH&#8217;d Xbox, and another one that&#8217;s not working and lacking the RF board. I solved the &#8220;not working&#8221; part by figuring out that someone tried to x-clamp it, and in the process attached some washers that were short-circuiting the board, removed &#8217;em and now it works, but it doesn&#8217;t have an RF board.

I took out the RF board from the RGH&#8217;d one, and installed it on the &#8220;former-not-working&#8221; Xbox&#8230;

&nbsp;

This put me in quite a pickle&#8230;what should I do with the RGH&#8217;d Xbox360 without an RF board ?

PUT LINUX ON IT. Fuck. Yeah.

So I did that.

Basically I now have a fully working Xbox360, a Wireless dongle for my PC and a Linux server running a Ubuntu PPC port. (That 7$ Xbox was a steal. The lesson here is &#8211; buy shit that people describe as being &#8220;broken&#8221;, if you&#8217;re tech savvy you&#8217;ll probably fix whatever the problem is, and you can flip that for some more cash for a bigger problem and so on.)

<div id='gallery-1' class='gallery galleryid-88 gallery-columns-3 gallery-size-thumbnail'>
  <dl class='gallery-item'>
    <dt class='gallery-icon landscape'>
      <a href='http://codin.ro/what-a-time-to-be-alive/dsc_8574-2/#main'><img width="150" height="150" src="https://codin.ro/wp-content/uploads/2015/08/DSC_85741-150x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" aria-describedby="gallery-1-100" /></a>
    </dt>
    
    <dd class='wp-caption-text gallery-caption' id='gallery-1-100'>
      RGH&#8217;d 360
    </dd>
  </dl>
  
  <dl class='gallery-item'>
    <dt class='gallery-icon landscape'>
      <a href='http://codin.ro/what-a-time-to-be-alive/dsc_8576/#main'><img width="150" height="150" src="https://codin.ro/wp-content/uploads/2015/08/DSC_8576-150x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" aria-describedby="gallery-1-99" /></a>
    </dt>
    
    <dd class='wp-caption-text gallery-caption' id='gallery-1-99'>
      RGH&#8217;d 360
    </dd>
  </dl>
  
  <dl class='gallery-item'>
    <dt class='gallery-icon landscape'>
      <a href='http://codin.ro/what-a-time-to-be-alive/dsc_8581/#main'><img width="150" height="150" src="https://codin.ro/wp-content/uploads/2015/08/DSC_8581-150x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" aria-describedby="gallery-1-92" /></a>
    </dt>
    
    <dd class='wp-caption-text gallery-caption' id='gallery-1-92'>
      RGH&#8217;d 360, booting via USB, HDMI out and inet in
    </dd>
  </dl>
  
  <br style="clear: both" />
  
  <dl class='gallery-item'>
    <dt class='gallery-icon landscape'>
      <a href='http://codin.ro/what-a-time-to-be-alive/dsc_8577-2/#main'><img width="150" height="150" src="https://codin.ro/wp-content/uploads/2015/08/DSC_85771-150x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" aria-describedby="gallery-1-98" /></a>
    </dt>
    
    <dd class='wp-caption-text gallery-caption' id='gallery-1-98'>
      RGH&#8217;d 360 installing Linux to its HDD
    </dd>
  </dl>
  
  <dl class='gallery-item'>
    <dt class='gallery-icon landscape'>
      <a href='http://codin.ro/what-a-time-to-be-alive/dsc_8580/#main'><img width="150" height="150" src="https://codin.ro/wp-content/uploads/2015/08/DSC_8580-150x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" aria-describedby="gallery-1-93" /></a>
    </dt>
    
    <dd class='wp-caption-text gallery-caption' id='gallery-1-93'>
      7$ Xbox 360, shitty cooler.
    </dd>
  </dl>
  
  <dl class='gallery-item'>
    <dt class='gallery-icon landscape'>
      <a href='http://codin.ro/what-a-time-to-be-alive/dsc_8579/#main'><img width="150" height="150" src="https://codin.ro/wp-content/uploads/2015/08/DSC_8579-150x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" aria-describedby="gallery-1-94" /></a>
    </dt>
    
    <dd class='wp-caption-text gallery-caption' id='gallery-1-94'>
      RGH RF Board on cheap Xbox
    </dd>
  </dl>
  
  <br style="clear: both" />
  
  <dl class='gallery-item'>
    <dt class='gallery-icon landscape'>
      <a href='http://codin.ro/what-a-time-to-be-alive/dsc_8572/#main'><img width="150" height="150" src="https://codin.ro/wp-content/uploads/2015/08/DSC_8572-150x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" aria-describedby="gallery-1-89" /></a>
    </dt>
    
    <dd class='wp-caption-text gallery-caption' id='gallery-1-89'>
      RF Board in the PC front mask
    </dd>
  </dl>
  
  <dl class='gallery-item'>
    <dt class='gallery-icon landscape'>
      <a href='http://codin.ro/what-a-time-to-be-alive/dsc_8573/#main'><img width="150" height="150" src="https://codin.ro/wp-content/uploads/2015/08/DSC_8573-150x150.jpg" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" aria-describedby="gallery-1-90" /></a>
    </dt>
    
    <dd class='wp-caption-text gallery-caption' id='gallery-1-90'>
      RF Board in the PC front mask.
    </dd>
  </dl>
  
  <br style='clear: both' />
</div>

[If anyone needs the sketch for the Arduino regarding the MS Wireless Xbox Dongle, or schematics, just let me know and I&#8217;ll post them.]

[See future post regarding the installation of Linux on the 360, I&#8217;ll host the files as well because the Free60 forum seems to be slowly dying.]

&nbsp;

 [1]: http://codin-moldovanu.com/wp-content/uploads/2015/08/DSC_8572.jpg
 [2]: http://codin-moldovanu.com/wp-content/uploads/2015/08/DSC_8573.jpg