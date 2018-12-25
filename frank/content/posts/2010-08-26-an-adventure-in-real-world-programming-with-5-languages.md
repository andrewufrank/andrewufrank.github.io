---
id: 135
title: An adventure in real world programming with 5 languages
date: 2010-08-26T07:32:00+00:00
author: Andrew Frank
layout: post
permalink: /an-adventure-in-real-world-programming-with-5-languages/
blogger_blog:
  - andrewufrank.blogspot.com
blogger_author:
  - andrew
blogger_permalink:
  - /2010/08/adventure-in-real-world-programming.html
blogger_internal:
  - /feeds/3533242289707427914/posts/default/7887926968108316370
image: /wp-content/uploads/2010/08/P1010631-cows-in-fog-.jpg
categories:
  - Uncategorized
---
<a href="https://test.gerastree.at/wp-content/uploads/2010/08/P1010631-cows-in-fog-.jpg"><img style="float:left; margin:0 10px 10px 0;cursor:pointer; cursor:hand;width: 320px; height: 170px;" src="https://test.gerastree.at/wp-content/uploads/2010/08/P1010631-cows-in-fog--300x160.jpg" border="0" alt=""id="BLOGGER_PHOTO_ID_5509628665105019186" /></a><br />I wanted to build a tool which I can use on my mobile (Android, HTC Desire); not finding a path to compile Haskell to anything executable on the mobile, I decided to follow advice from <a href="http://building-iphone-apps.labs.oreilly.com/"> Building iPhone Apps with HTML, CSS, and JavaScript  </a> to build a web application using Haskell to construct the web server with <a href="http://docs.yesodweb.com/#"> Yesod </a>.<br /><br />What I did not expect was the number of un-coordinated and slightly different languages I had to learn. The project included a total of 5 different computer languages:<br />- Haskell, for programming the application,<br />- CouchDB (fortunately accessible from Haskell), <br />- javascript, to code the building of the index in couchDB,<br />- HTML, to describe the structure of the output,<br />- CSS, to describe the appearance of the web page.<br />Modern computer languages are quite similar, but differ in small ways: how do they deal with white space and what is white space? how to insert a comment? how to 'escape' a character, which has a particular meaning? <br /><br />In the process I was reading documentation, and could not, for example, find an advanced, well structured description how to use HTML and CSS; the specification is readable, but does not indicate how the various features, which seemingly are producing the same effects, are best used, to avoid their quirks. Not only had I to learn the languages, but also to find specialized editors and tools for debugging (e.g. a Firefox extension to see what HTML and CSS arrived at the browser) - each tool with its own set of 'small differences'.<br /><br />I succeeded, but two questions remain, one existential, one social:<br />- is it possible, to build a web application in a single language (specifically: in Haskell)?<br />- why do the 'real programmers' accept this sorry state of the world?<br /><br />The first question leads to a testable hypothesis, which I hope to report about soon; the second reminds me of an observation of a social science researcher (I do not remember who it was), who pointed out that social institutions oscillate to a middle ground of complexity. If they are so simple that everybody can understand them, ingenuous people make them more complex; if they are so complex that nobody can use them any more, efforts to simplify are made. I guess, social systems need complexity to differentiate between amateurs and experts; complexity assures income to experts. This seems not only to apply to the legal system, with layers and tax advisers, but also to programmers?