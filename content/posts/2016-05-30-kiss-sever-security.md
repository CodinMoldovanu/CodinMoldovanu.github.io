---
title: KISS – Sever Security
author: Moldovanu Codin
type: post
date: 2016-05-30T20:28:25+00:00
url: /kiss-sever-security/
dsq_thread_id:
  - "5632959769"
categories:
  - Linux
  - Not-Daily
  - Tech
tags:
  - infosec
  - linux
  - ossec
  - security
  - server
  - snort

---
KISS, as in Keep It Short, Simple is an acronym that I learned a few years ago yet it&#8217;s one of the best way to describe how almost anything should work. I&#8217;ll talk a bit about how to have a secure server (or VPS, if you&#8217;re into that kind of thing) and avoid any nasty chinese h4x0rs trying to login using _root_ as a username.

I&#8217;ll go about it in layers, from passive to active and from integrated to dedicated. I use Webmin/Virtualmin and Debian Jessie on my server, so some parts won&#8217;t apply to you if your configuration is different, but others will.

<!--more-->

## First Layer &#8211; Common Sense in Webmin (or any other cPanel)

Disable root login for the SSH server. _**sudo nano /etc/ssh/sshd_config**_ and then scroll down to &#8220;#PermitRootLogin without-pass&#8221; and change that line to &#8220;PermitRootLogin no&#8221;. You can also do this by editing the SSH config inside Webmin.

Another safety measure you should take is using the Two-Factor Authentication feature present in Webmin that works with the Google Authenticator, this is basically the same Two-Factor login that&#8217;s present in Gmail, Facebook et.al.

## Second Layer &#8211; Webmin Tools

Enable/Install the Fail2Ban package and activate jails according to your needs. This tool will ban people when they match certain actions. You&#8217;ll get an email regarding any actions that it takes. It&#8217;s a pretty nice tool that could basically keep you as safe as it gets without getting down and dirty. The default jails are more than enough if you don&#8217;t plan on using weird servers (e.g. Teamspeak)

## Third Layer &#8211; Paranoid Android

This is the nicest layer, as it comes down to you being as paranoid and careful as you could get regarding the safety and security of your data.

IPS/IDS stands for Intrusion Prevention System or Intrusion Detection System and it will be one of your best friends to keep russian sk&#8217;s at bay.

IDS&#8217;s will let you know when stuff is going on, but won&#8217;t do much of else. Even the installation of a package will trigger a warning (if you set it to do so) that will let you know about it via an email. One of the best host based IDSs is [OSSEC ][1] which is free and open source. Again, the default rules are pretty ok for starters, but if you dig into the Documentation you&#8217;ll become a master in no time.

IPS&#8217;s will be the Cerberus for your sever and will prevent anything you don&#8217;t want happening, from SSH login attempts to root logins from shady IP classes (looking at you China). One of the best IPS&#8217;s is [Snort][2] which again is a free and open source tool. You&#8217;ll have to Sign Up or Subscribe to them to get access to a &#8220;Community Rule Package&#8221; in order to set everything up nicely with some default rules, but they have a pretty nice documentation in place that will help you customize everything pretty quickly.

As a final word, there&#8217;s no such thing as &#8220;too much infosec&#8221; as long as your systems don&#8217;t clash with each other and are set up to _be redundant not just layered._

&nbsp;

&nbsp;

 [1]: http://ossec.github.io/
 [2]: https://www.snort.org/