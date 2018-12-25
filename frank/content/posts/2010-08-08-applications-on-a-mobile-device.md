---
id: 137
title: Applications on a mobile device
date: 2010-08-08T08:56:00+00:00
author: Andrew Frank
layout: post
permalink: /applications-on-a-mobile-device/
blogger_blog:
  - andrewufrank.blogspot.com
blogger_author:
  - andrew
blogger_permalink:
  - /2010/08/applications-on-mobile-device.html
blogger_internal:
  - /feeds/3533242289707427914/posts/default/6749164374869238340
image: /wp-content/uploads/2010/08/P1010205.jpg
categories:
  - Uncategorized
---
<a href="https://test.gerastree.at/wp-content/uploads/2010/08/P1010205.jpg"><img style="float:left; margin:0 10px 10px 0;cursor:pointer; cursor:hand;width: 320px; height: 240px;" src="https://test.gerastree.at/wp-content/uploads/2010/08/P1010205-300x225.jpg" border="0" alt=""id="BLOGGER_PHOTO_ID_5502968298421256834" /></a><br />In my effort to study the ontology of space, time and persons in my life and how to organize it in a better Personal Information Manager, I want to build a system I can use to test the ontology to gradually improve it. I believe that only ontologies which are actually used can teach us anything about ontology design.<br /><br />Therefore, I need a method to build applications on the mobile design in a high level language such that I can derive the code from a formally described ontology, preferably Haskell, which reveals structure of the program and does not force programming in particular ways. Simply: I need a Haskell compiler producing code executable on the mobile, because only if it is executing on the mobile and the data are synced, the application is available even if not connected to the Internet. <br /><br />There are project to compile Haskell to JavaScript, which can be executed in most browsers on the mobile and small server programs running in a mobile exists. Unfortunately, neither of the JavaScript project is currently usable. They are often based on the York Haskell Compiler (yhc), which seems abandoned. Other projects are 'proof of concept' and to make them usable is beyond what I am prepared to do. It will take some time, before I can compile Haskell and run it on the mobile.<br /><br />Second best:<br /><br />Use another language, e.g. JavaScript, lua or python which execute on an Android mobile. I fear this will detract from identify the ontology, ontological issues obfuscated by the particulars of the language. I briefly looked at OCaml, a functional language close to Haskell, but the code read as text was quite misleading ("ignore" all over the place - my brain follows the advice and ignores the rest of the line...). <br /><br />Restrict the application development to make it usable only when connected to the Internet; then I can write in Haskell and hopefully drive the code from the ontology - as much as possible from a formal description of the ontology deriving the code automatically. Later, the code can be hand-translated to a language executable on the mobile (today, I would probably use Lua) and run there.