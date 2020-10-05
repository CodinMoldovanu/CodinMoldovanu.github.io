---
title: Installing Linux to the HDD of an Xbox360
author: Moldovanu Codin
type: post
date: 2015-08-29T22:29:38+00:00
url: /installing-linux-to-the-hdd-of-an-xbox360/
dsq_thread_id:
  - "5886094466"
categories:
  - Linux
  - Tech
tags:
  - "360"
  - beta
  - beta2
  - bootloader
  - cd
  - console
  - debian
  - debootstrap
  - etch
  - gentoo
  - hard drive
  - hdd
  - install
  - installing
  - jtag
  - linux
  - live
  - livecd
  - rgh
  - run
  - running
  - script
  - server
  - sh
  - to
  - xbox
  - xbox360
  - xell
  - xenon
  - your

---
This is a follow-up on the post regarding installing Debian on the Xbox360.

Most of the resources from the Free60 Project (which is now kinda dead) are either outdated or no longer available. Comcast user &#8220;ssmurf&#8221; did a good job hosting most of the files needed for the whole process , but I don&#8217;t know how longer he&#8217;ll host them, so I decided to mirror most of the files myself, including the debootstrap. Usually Linux archives have the tendency to become bloated and ridiculously hard to access.

<!--more-->

You&#8217;ll need

  * 2 CDs  (DVDs work as well)
  * USB keyboard /& mouse
  * JTAG/RGH Xbox360
  * Patience

Resources addresses

  * Gentoo Live CD Xenon Beta 2 (<a href="http://downloads.sourceforge.net/free60/gentoo-livecd-xenon-beta-v2.iso" target="_blank" rel="noopener">http://downloads.sourceforge.net/free60/gentoo-livecd-xenon-beta-v2.iso</a>)
  * Xell Bootloader                                      (<a href="http://codin.ro/lynxbox/XeLL-Bootloader-sda2-v2.6.24.3.tar.gz" target="_blank" rel="noopener">http://codin.ro/lynxbox/XeLL-Bootloader-sda2-v2.6.24.3.tar.gz</a>)
  * Install Script                                           (<a href="http://codin.ro/lynxbox/install.sh" target="_blank" rel="noopener">http://codin.ro/lynxbox/install.sh</a>)

Installation

  1. Create a CD with the Gentoo LiveCD image and boot it up. Just wait and you&#8217;ll be entered into the default user.
  2. Open a terminal window and write the following commands : &#8220;sudo su&#8221;,&#8221;wget http://codin.ro/lynxbox/install.sh&#8221;,&#8221;sh ./install.sh&#8221; &#8211; This will enter you into superuser mode, then will fetch the script and afterwards will start executing the script. After the script finishes you&#8217;ll be told to boot the Xell Bootloader (the one which you should&#8217;ve burned to a CD by now)
  3. Reboot and be sure to have the Bootloader disc in the Xbox, everything should go without a hitch. A few prompts will appear, just hit Enter for the Bluescreen regarding resolutions and &#8220;Yes&#8221; for the warning regarding the pleothora of packages that will be installed.
  4. Ta-Da !

&nbsp;

After I manage to make everything smooth, I&#8217;ll follow up regarding setting up a LAMP+FTP stack on the machine, and performance graphs.

**Update 1 &#8211; Managed to install the LAMP stack, everythink works properly so far. Virtualmin won&#8217;t work because of the PPC arch. Besides that, I managed to update to Debian Lenny (5.0), without too many issues. The goal is, I think, updating all the way up to Jessie (8.0) from Etch (4.0) although stuff may become borked along the path. I&#8217;ll keep updating this post, and probably will make another post tonight regarding the LAMP stack. **

_**Links are updated as of 30 December 2017. **_

[<img loading="lazy" class="alignnone size-full wp-image-106" src="http://codin-moldovanu.com/wp-content/uploads/2015/08/debiansrv.png" alt="debiansrv" width="687" height="1015" srcset="https://codin.ro/wp-content/uploads/2015/08/debiansrv.png 687w, https://codin.ro/wp-content/uploads/2015/08/debiansrv-203x300.png 203w, https://codin.ro/wp-content/uploads/2015/08/debiansrv-338x500.png 338w" sizes="(max-width: 687px) 100vw, 687px" />][1]

 [1]: http://codin-moldovanu.com/wp-content/uploads/2015/08/debiansrv.png