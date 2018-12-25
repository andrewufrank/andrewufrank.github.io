---
id: 130
title: Optimisms in Software Development
date: 2011-01-30T11:38:00+00:00
author: Andrew Frank
layout: post
permalink: /optimisms-in-software-development/
blogger_blog:
  - andrewufrank.blogspot.com
blogger_author:
  - andrew
blogger_permalink:
  - /2011/01/optimisms-in-software-development.html
blogger_internal:
  - /feeds/3533242289707427914/posts/default/5981492359894478155
image: /wp-content/uploads/2011/01/P1020606.jpg
categories:
  - Uncategorized
---
<a href="https://test.gerastree.at/wp-content/uploads/2011/01/P1020606.jpg"><img style="float:left; margin:0 10px 10px 0;cursor:pointer; cursor:hand;width: 240px; height: 320px;" src="https://test.gerastree.at/wp-content/uploads/2011/01/P1020606-225x300.jpg" border="0" alt=""id="BLOGGER_PHOTO_ID_5567945270952982162" /></a>Software development is notoriously behind schedule and above budget. Why are we so unable to estimate the time it takes to produce an application?  <br /><br />Development of hardware is always underestimated and the development of software overestimated; reality is different. For example compare the current multi-core CPU in your laptop with the CPUs built from discrete components 40 years ago and then contrast this stunning advancement with the similarity of FORTRAN and ALGOL used on these CPU's and Java used today!<br /><br />“It is only a small matter of programming” was originally a 'game people play' (see the book by Eric Berne) and is now the title of a book by Nardi – the game is played as IT projects in most organization in the western world and we all suffer from late, inadequate and error-producing software we are forced to use in our work environment. <br /><br />I had recently a student proposing to write software to allow end-users to create and adapt graphical user interfaces. He started with a good idea, observing the connection between database schema and GUI, and had quickly wiped together rudimentary graphical editors for GUI and database schema. This must have been emotionally rewarding, i.e. fun, and it seemed a minor step to complete the rest. <br /><br />Having often started simple looking projects myself, to observe later the hidden complexity that made it hard to produce at the end, something coping with the complexity of a real world application, I start identifying some common sources for the optimism. We do not address the hard questions first and start to program early. The hard questions can be found by:<br />- Identify a compact but not trivial use case and describe it from the user's perspective in detail.<br />- Select a formal (or pseudo-formal) language to describe the representation for the information used in the program.<br />- Describe the functions (transformations) used to achieve the goal in a (pseudo-)formal language. <br /><br />In my effort to exploit the data structure information to produce a GUI I failed eventually when I started considering exceptions: special situations in the underlying application operations and problems with user input has to be dealt with in parallel with the ordinary application logic. I found the current exception handling violating the principle of locality in my code and confuse me to the point I gave up; I will return to the question when I have a good idea what I could do differently.<br /><br />Some advice at the end:<br />Use existing tools and do not duplicate them unless you have a compelling reason; try first to patch together a prototype using existing tools.