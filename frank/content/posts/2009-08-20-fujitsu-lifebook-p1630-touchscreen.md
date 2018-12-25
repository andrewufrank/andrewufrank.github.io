---
id: 144
title: Fujitsu Lifebook P1630 Touchscreen
date: 2009-08-20T07:53:00+00:00
author: Andrew Frank
layout: post
guid: https://test.gerastree.at/2009/08/20/fujitsu-lifebook-p1630-touchscreen/
permalink: /fujitsu-lifebook-p1630-touchscreen/
blogger_blog:
  - andrewufrank.blogspot.com
blogger_author:
  - andrew
blogger_permalink:
  - /2009/08/fujitsu-lifebook-p1630-touchscreen.html
blogger_internal:
  - /feeds/3533242289707427914/posts/default/2780017364760539037
categories:
  - P1630 Lifebook Fujitsu Ubuntu Tablet
---
<a href="http://2.bp.blogspot.com/_Z6mNar6sZs4/So0PDboxLhI/AAAAAAAAAB0/EA6A2HSt5Vg/s1600-h/CIMG0201.JPG"><img style="margin: 0pt 10px 10px 0pt; float: left; cursor: pointer; width: 320px; height: 240px;" src="http://2.bp.blogspot.com/_Z6mNar6sZs4/So0PDboxLhI/AAAAAAAAAB0/EA6A2HSt5Vg/s320/CIMG0201.JPG" alt="" id="BLOGGER_PHOTO_ID_5371966482155646482" border="0" /></a><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br />I have a new ultraportable (1 kg) Lifebook P1630 with a touchscreen. I hope to use it for presentations in the same manner I use currently the Fujitsu Stylistic 5010 tablet.<br />The P1630 comes with Vista installed - but this is unusable slow on a Core 2 Duo processor and I do not tolerate the waiting updates of MS software forces on me. I want to run Linux, meaning Ubuntu 9.04 Jaunty!<br />Installation was a breeze (much faster than just the update with MS) and everything worked out of the box, except for the touchscreen.<br /><br />With help from the web, I got it working. This is to report what I did, to help others with P1630 (and probably P1620). The P1630 (and 1620) connect the touchscreen via usb, not serial - thus the advice for P1510 etc. does not work (e.g. this <a href="http://ubuntuforums.org/showthread.php?t=811200&amp;page=4">script</a>). The method proposed by Sam Engstrom <a href="http://doitfast4u.blogspot.com/2008/07/howto-get-touchscreen-working-on.html">propagated here</a>  does also not work, because it connects the touchscreen using a setserial and /dev/ttyS0. It seems that this could be solved by connecting the touchscreen to an eventN (with a hal/policy?) and then use wacdump /dev/input/eventN (N a number 1..9). I did not explore this further.<br /><br />I got the touchscreen of the P1630 working with these <a href="http://spareinfo.blogspot.com/2009/05/linux-on-fujitsu-u810-p1620-touchscreen_19.html">tools</a>. This worked immediately, with the BIOS set to "tablet" (not "touch screen") except for some confusion with the calibration. The calibration routine acted strangely on my system: after calibration any touch on the screen would open the trash folder (anybody has an explanation? I had observed this before I installed any touchscreen software already). The calibration routine did leave the max_x and max_y values set to the initial -1 values. I fixed in the code by adding two additional tests to read:<br /><br />    <blockquote>  if (calibrate) {<br />             calib_minx = ..<br />             calib_miny = ..<br />             calib_maxx = (calib_maxx==-1)?x:((x>calib_maxx)?x:calib_maxx);<br />             calib_maxy = (calib_maxy==-1)?y:((y>calib_maxy)?y:calib_maxy);<br />     }</blockquote><br />make! sudo make install! and it works.<br /><br />The sampling of the stylus is unfortunately not very rapid and handwriting looks wiggly. Does anybody have a hint how this could be improved?<br /><br />Addition: I learned that there are new (corrected) versions <a href="http://sites.google.com/site/spareinfosite/Home/fujitsu-usb-touchscreen-0.3.5.tar.gz">available</a>, the change has the same effect, but I have not tried it yet.