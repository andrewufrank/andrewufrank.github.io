---
id: 127
title: Debian with XFCE4 on Lenovo Thinkpad Yoga14
date: 2016-04-03T06:30:00+00:00
author: Andrew Frank
layout: post
permalink: /debian-with-xfce4-on-lenovo-thinkpad-yoga14/
blogger_blog:
  - andrewufrank.blogspot.com
blogger_author:
  - andrew
blogger_permalink:
  - /2016/04/debian-with-xfce4-on-lenovo-thinkpad.html
blogger_internal:
  - /feeds/3533242289707427914/posts/default/7044045373275563724
categories:
  - Uncategorized
---
I bought a Lenovo Thinkpad Yoga14 because I wanted a new device with handwriting input for writing and drawing; i know that it would work with Ubuntu and assumed that it would also work with a regular Debian installation (I dislike Canonical's approach to force users to their views).<br /><br />Installation of Debian was somewhat more difficult; here the short description what worked for me in the end.<br /><br />1. I observed that my working installation of Ubuntu used libwacom-bin, which is only in Debian stretch; thus I decided to install stretch (aka testing). Installations of jessie were not supporting the pointer.<br /><br />2. To install Debian stretch (alpha 5 release) requires the non-free firmware and additionally the driver for the Intel Wireless 7265 rev 61 (aka 7265D), which is iwlwifi--7260-17.ucode (download from a git...), which i put on a second usb stick (on the first i had the inofficial stretch release including the firmware).<br /><br />3. Install regularly and add the USB stick with the firmware when requested.<br /><br />&nbsp;4. Restart and produce <span style="font-family: &quot;Courier New&quot;,Courier,monospace;">/etc/apt/sources.list</span> (not automatic in alpha 5)<br /><br /><blockquote><span style="font-family: &quot;Courier New&quot;,Courier,monospace;">deb http://ftp.at.debian.org/debian/ stretch main contrib non-free&nbsp;</span><br /><span style="font-family: &quot;Courier New&quot;,Courier,monospace;">deb http://security.debian.org/debian stretch/updates main contrib non-free&nbsp;</span></blockquote><br />and <span style="font-family: &quot;Courier New&quot;,Courier,monospace;">/etc/network/interfaces</span><br /><br /><blockquote><span style="font-family: &quot;Courier New&quot;,Courier,monospace;">auto lo&nbsp;</span><br /><span style="font-family: &quot;Courier New&quot;,Courier,monospace;">iface lo inet loopback&nbsp;</span><br /><br /><span style="font-family: &quot;Courier New&quot;,Courier,monospace;">auto wlp2s0&nbsp;</span><br /><span style="font-family: &quot;Courier New&quot;,Courier,monospace;">iface wlp2s0 inet dhcp&nbsp;</span><br /><span style="font-family: &quot;Courier New&quot;,Courier,monospace;">&nbsp;&nbsp;&nbsp;&nbsp; wpa-ssid xxxx&nbsp;</span><br /><span style="font-family: &quot;Courier New&quot;,Courier,monospace;">&nbsp; &nbsp;&nbsp; wpa-psk "pppppp"</span></blockquote><br />&nbsp;5. restart and login as root; check that network is ok.<br /><br />Then apt-get update, apt-get upgrade (some problem with iwlwifi?? - it needed a apt-get upgrade -f).  install xfce4, xfce4-goodies, xournal (for drawing)  startx to test  install lightdm<br /><br />it works, when you restart, the regular xfce login greeter is there!