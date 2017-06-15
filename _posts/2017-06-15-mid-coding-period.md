---
layout: post
title: "coala Online"
description: "GSoC Coding Period Week 2-3"
categories: ["stories", "coala"]
bg: https://user-images.githubusercontent.com/13018570/27181346-da91a618-51f4-11e7-9c6b-d5db3a5f408f.png
header_color: teal
---

coala Online is gradually reaching towards a stable state. 

With this [commit](https://gitlab.com/gitmate/open-source/gitmate-2/commit/d654330d3835d6de7a628f37222b136393eba1fc), we've finally on the way
to run bears with non optional settings on the web. The user flow is essentially the same as we discussed in https://hemangsk.github.io/stories/coala/2017/05/29/end-of-bonding-period.html.

#### The few things which we refined along the way. 

Optimizing the features to be added in coala-quickstart. 
  Earlier the plan was to add a dir and sections_only mode. Then @jayvdb and @sils helped me figure out a clean approach, that helped me to
  get a better perspective. The lesson I learnt is that, It is important to think hard enough if you want to add new features upstream for your project.
  Because if the things are not planned good, then what might happen if upstream features are added without proper planning is that after some time, you'll definitely realize that, "Oh! this isn't working
  according to my needs, lets add that feature too, then later, lets add this too and so on.".
  
GitMate turned out to be a better base for coala_online module, rather than webServices. As more than half of the stuff which we wanted to have in coala_online
was already there in GitMate, Lasse and Fabian suggested me that an endpoint in GitMate is better suit. Then I took inspiration from 
Naveen's work on coala-incremental-results docker image and gitmate_code_analysis. 
Special thanks to him who's always there (otherwise, quite busy with the new MacBook :P) to help me understand a lot stuff here & there.




Greetings!
