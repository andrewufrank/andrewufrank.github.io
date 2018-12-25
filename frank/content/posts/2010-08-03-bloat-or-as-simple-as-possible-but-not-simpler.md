---
id: 139
title: 'Bloat or &#8220;as simple as possible, but not simpler&#8221;'
date: 2010-08-03T07:07:00+00:00
author: Andrew Frank
layout: post
permalink: /bloat-or-as-simple-as-possible-but-not-simpler/
blogger_blog:
  - andrewufrank.blogspot.com
blogger_author:
  - andrew
blogger_permalink:
  - /2010/08/bloat-or-as-simple-as-possible-but-not.html
blogger_internal:
  - /feeds/3533242289707427914/posts/default/6137593956726673857
image: /wp-content/uploads/2010/08/IMAG0017.jpg
categories:
  - Uncategorized
---
<a href="https://test.gerastree.at/wp-content/uploads/2010/08/IMAG0017.jpg"><img style="float:left; margin:0 10px 10px 0;cursor:pointer; cursor:hand;width: 192px; height: 320px;" src="https://test.gerastree.at/wp-content/uploads/2010/08/IMAG0017-180x300.jpg" border="0" alt=""id="BLOGGER_PHOTO_ID_5501079344618117474" /></a><br />Most software tools grow over time, only a small number stays the same. These are not increase in functionality, because they have already all what is needed; they are perfect. What is the receipt to achieve that?<br /><br />In my own work I see the following pattern which leads to bloat: underestimating complexity and building something too simple. The pattern, once recognized, may lead to improved designs, such that software bloat can be avoided. Here two examples:<br /><br />I tried to build a tool to automate the construction of graphical user interfaces from ontology and I included facilities for conversion between the screen representation and the representation in the application program. Different applications had different requirements for this conversion and the functionality grew ...<br />What was wrong? the complexity of the conversion requires a full programming language and I was, step by step and functionality by functionality inventing my own. Bad move!<br />What can be done? have the part which converts between GUI and application written in an ordinary programming language (in my case, Haskell) and remove all functionality which can be provided in the conversion functions written in the general programming language. - Progress: the tool becomes smaller and simpler!<br /><br />I found the same approach in couchDB: parts, where complexity of the application comes in, are programmed in a programming language (e.g. views - compare with the complexity of special languages for report generation of old). CouchDB just manages the code (in javascript - a nice functional programming language!). <br /><br />Bloat occurs slowly if we try to build something that is too simple, and then  realize that a bit of functionality here and a bit of functionality there must be added and before we see it, we have BLOAT. It is a sign of not factoring out complexity in parts where it can be handled with the ordinary programming language and can be avoided in many cases.