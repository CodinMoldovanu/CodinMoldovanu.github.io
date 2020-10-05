---
title: Stop building stuff on sand – the Internet, Linux
author: Moldovanu Codin
type: post
date: 2016-10-21T23:25:56+00:00
url: /stop-building-stuff-on-sand-the-internet-linux/
dsq_thread_id:
  - "5900681434"
categories:
  - Linux
  - Not-Daily
  - Tech
  - Uncategorized
tags:
  - attack
  - ddos
  - debian
  - distro
  - dns
  - dyn
  - dyndns
  - hacking
  - internet
  - kernel
  - linux
  - securitate
  - server

---
You&#8217;ve probably heard about the big DNS attack on Dyn&#8217;s servers today, and you probably know that it was the main cause of &#8220;half the internet&#8221; not working properly today.

The attack targeted Dyn&#8217;s DNS servers and took _down a shitload of websites (_well, not really took down, but I&#8217;ll explain further along_)_, including Netflix, WSJ, Imgur, Reddit, Spotify, etc. According to CNBC citing Dyn &#8220;tens of millions of IP addresses&#8221; were sending packets and causing mayhem for the U.S. based company.<!--more-->

In simple terms, DNS is basically speed-dial for websites. You don&#8217;t memorize 62.231.78.23, you memorize &#8220;google.com&#8221;. Well, think of the IP as being the phone number, the domain name as the speed-dial button. If the speed dial doesn&#8217;t work, you gotta use the full phone number &#8211; so you could go to Google.com by typing in 62.231.78.23 if &#8220;Google.com&#8221; isn&#8217;t working, but you probably don&#8217;t have a post-it stuck to your PC saying &#8220;In case of emergency, dial 62.231.78.23 for Google&#8221;.

DNS is old, clunky, and messy. After having set up an old school physical server with everything a server should have, from a DNS server down to installing OSSEC to receive live alerts regarding the security of it, I can honestly say that DNS is horrible. There are about 40 RFC&#8217;s (standards, good practices, etc.) that you should read to properly set up DNS for a server, and all that on a website that looks like something Stallman would see on his PC while browsing any website back in the 90&#8217;s. Oh look, here you can see an RFC from August 1990 and one from December 2015. In the same format, albeit a different colour scheme.

<p class="jetpack-slideshow-noscript robots-nocontent">
  This slideshow requires JavaScript.
</p>

<div id="gallery-369-1-slideshow" class="slideshow-window jetpack-slideshow slideshow-black" data-trans="fade" data-autostart="1" data-gallery="[{&quot;src&quot;:&quot;https:\/\/codin.ro\/wp-content\/uploads\/2016\/10\/another.png&quot;,&quot;id&quot;:&quot;395&quot;,&quot;title&quot;:&quot;another&quot;,&quot;alt&quot;:&quot;&quot;,&quot;caption&quot;:&quot;1990&quot;,&quot;itemprop&quot;:&quot;image&quot;},{&quot;src&quot;:&quot;https:\/\/codin.ro\/wp-content\/uploads\/2016\/10\/ietf2015.png&quot;,&quot;id&quot;:&quot;396&quot;,&quot;title&quot;:&quot;ietf2015&quot;,&quot;alt&quot;:&quot;&quot;,&quot;caption&quot;:&quot;2015&quot;,&quot;itemprop&quot;:&quot;image&quot;}]" itemscope itemtype="https://schema.org/ImageGallery">
</div>

I am being a bit pedantic, I admit, but you&#8217;d expect 26 years to be enough for a widely used technology to properly evolve further than adding IPv6 and DNSSEC. Open a Private Window, query Google for &#8220;dns&#8221; &#8211; I challenge you to find a link to anything official on the first page. You won&#8217;t, nor would anyone who just got a job as a SysAdmin at DynDNS &#8211; despite the fact that he should be properly trained, stuff like this still happens, just like some doctors screw up operations.

How about stopping for a bit and challenging the IESG (Internet Engineering Steering Group) and IETF(Internet Engineering Task Force) to actually assess the situation at hand, and decide upon actual improvements, creating proper documentation and generally creating a proper professional environment regarding the technology so that you don&#8217;t have to open 40 tabs and read documentation that you may or may not need. Making the information more easily accessible and readable means more people will actually go through it and that means more security.

There have generally been two trends in the internet world &#8211; centralization and decentralization. The latter being prefered by security enthusiasts, the first being prefered by snooping eyes and big companies, not necessarily in that order. It&#8217;s amazing really that DNS is still a centralized service which makes it vulnerable to such attacks &#8211; despite the standards requiring you to have at least 2 DNS servers in different IP classes, &#8220;preferably in different buildings, with different ISPs&#8221;, they&#8217;re still vulnerable. A decentralized system (look at the blockchain for example) is virtually unhackable, you just have your IP &#8211; domain list in your PC and nothing can happen to it, albeit there is a sizeable size issue with the number of domains registered having skyrocketed lately. (This is a gross oversimplification, but the idea is the same.)

Regarding the attack &#8211; people will rush to say Russia, because _some countries_ just love cold wars and trips to space &#8211; but in reality we just don&#8217;t know who did it. A few weeks ago the first IoT DDoS attack took place in which some 50,000 IP Cams attacked Brian Krebs&#8217; website and took it down. The cams were infected with Mirai, a _(now)_ open source botnet that managed to make its way around the globe.

<div id="attachment_419" style="width: 810px" class="wp-caption alignnone">
  <a href="https://www.incapsula.com/blog/malware-analysis-mirai-ddos-botnet.html" target="_blank"><img aria-describedby="caption-attachment-419" loading="lazy" class="alignnone size-full wp-image-419" src="http://codin.ro/wp-content/uploads/2016/10/mirai-botnet-map.png" alt="mirai-botnet-map" width="800" height="458" srcset="https://codin.ro/wp-content/uploads/2016/10/mirai-botnet-map.png 800w, https://codin.ro/wp-content/uploads/2016/10/mirai-botnet-map-300x172.png 300w, https://codin.ro/wp-content/uploads/2016/10/mirai-botnet-map-768x440.png 768w" sizes="(max-width: 800px) 100vw, 800px" /></a>
  
  <p id="caption-attachment-419" class="wp-caption-text">
    Incapsula.com
  </p>
</div>

The people at Incapsula poked around in the source code and found something pretty silly, whoever created Mirai hardcoded a list of IPs that ought not to be disturbed (IPs found on a wiki page) that belonged to the US DoD, General Electric, HP, IANA and the US Postal Service. This smells like something a skiddie would do, and probably is.

So, seeing how tools like Mirai are easily available on GitHub and other channels, why is anyone rushing to blame Russia and not some bored kid somewhere in Argentina? I mean, Russia could&#8217;ve done it, but don&#8217;t say it without having some actual proof.

## Dirty Cow

That&#8217;s the nickname given to <span class="st">CVE-<wbr />2016-5195 which is a privilege escalation kernel vulnerability &#8211; basically giving non-privileged users root access. Vulnerabilities are common and they get patched pretty fast, except that Dirty Cow <strong><em>has been there for 9 years and we&#8217;ve just discovered it now</em></strong><strong>. </strong>Funnily enough Kees Cook who works at Google recently published <a href="https://outflux.net/blog/archives/2016/10/18/security-bug-lifetime/">a paper that puts the average lifetime of a linux bug at 5 years</a>. </span>

Linux, is found on 65% of the top one million web servers in the world right now, so that&#8217;s about 650,000 web servers that are vulnerable to this bug. If half of those are VPSs with 5 users/server we come up with 325,000*5 = 1,625,000 possible privilege escalation opportunities. The problem is that despite the fact that Linux is said to be the most secure OS, and Open Source at the same time, bugs like these exist and we won&#8217;t know until they&#8217;re being used to exploit our &#8220;good guy&#8221; servers. If a kernel vulnerability that allows root access hasn&#8217;t surfaced despite living for 9 good years, what other &#8220;smaller&#8221; vulnerabilities do exist in the kernel?

I mean, Linux is free and anyone can contribute but there are companies like RedHat that are using the Linux Kernel and creating software that requires expensive (I think) licenses, so you do expect a lot of security when _actually paying _for what&#8217;s basically a free product that already has a good record of security with the added license and goodies that RedHat bundles in with its OS.

We should keep in mind that Linux development is way different than that of say Windows or Apple&#8217;s OS X (_or whatever they call it now)_. Linux is basically just a kernel, so developers work on tiny bugs (or big ones) and small optimizations, new hardware compat and generally stuff that you don&#8217;t really see on your screen. Either way, you &#8211; the end user &#8211; don&#8217;t just install the Linux kernel, you get a distro like Fedora, Debian, Ubuntu or Arch if you&#8217;re into BDSM and those things. There are a lot of distros, and I mean [A LOT of distros][1] (but personally, Debian is king, Elementary OS is nice). A distro has a Linux kernel and a GUI, among other things.

So, with another gross simplification we have:

  * A dev team working on the Linux Kernel
  * Another dev team working on the general distro (e.g. Debian)
  * Yet another dev team working on the GUI (e.g. KDE)

Keep in mind that these are all different projects, with little or no connection between them whatsoever. Also keep in mind that there are 20+ actually used Linux distros, and 5+ actually used GUIs. We run into the same problem as the Android OS &#8211; _fragmentation_.

There is such a huge amount of work simply wasted on reinventing the wheel over and over again, dev teams creating the same menu bars again and again to create &#8220;a new GUI&#8221; or to improve said GUI, hundreds of people creating new &#8220;distros&#8221; by just repackaging something already existing but using a different GUI and so on.

As a conclusion, after steering off topic a bit, can we stop just building cities on thin ice and actually improve the said thin ice? Let&#8217;s rehaul DNS, or rethink it, or stop using it altogether. How about this &#8211; any company that&#8217;s maintaining a distro should have (ehm, as a good practice or something that will make them seem better in the eyes of the consumer) at least 5 researchers (should be called a LINUX KERNEL TASK FORCE) dedicated to Linux kernel development &#8211; slightly communistic, but they should be paid for this work so that solves the communistical problem.

&nbsp;

**Regarding the vulnerability &#8211; **You&#8217;ll be delighted to hear that it has been patched and a messenger pigeon will make its way downstream to your local linux distro maintainer to further fly even lower to your server with the patched kernel update, so please expect him with some water and a _apt-get update && apt-get upgrade _prepared.

##

 [1]: https://upload.wikimedia.org/wikipedia/commons/1/1b/Linux_Distribution_Timeline.svg