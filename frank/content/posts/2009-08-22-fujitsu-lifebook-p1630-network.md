---
id: 143
title: Fujitsu Lifebook P1630 Network
date: 2009-08-22T06:49:00+00:00
author: Andrew Frank
layout: post
guid: https://test.gerastree.at/2009/08/22/fujitsu-lifebook-p1630-network/
permalink: /fujitsu-lifebook-p1630-network/
blogger_blog:
  - andrewufrank.blogspot.com
blogger_author:
  - andrew
blogger_permalink:
  - /2009/08/fujitsu-lifebook-p1630-network.html
blogger_internal:
  - /feeds/3533242289707427914/posts/default/2348785016924853417
categories:
  - Uncategorized
---
I will collect on this blog page hints for others with a P1630:<br /><br />The network connection on the P1630 was sort of flaky. It improved after installing linux-backports-modules-jaunty.<br /><br />sudo apt-get install linux-backports-modules-jaunty<br />restart!<br /><br />Now I have a decent signal level and it connects quickly.