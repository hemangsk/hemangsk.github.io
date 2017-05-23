---
layout: post
title: "The Making of coalaCSS"
description: "GSoC Bonding Period Week 2"
categories: ["stories", "coala"]
bg: images/8.png
header_color: darkblue
---

The Making of coalaCSS

So for the first two weeks I worked on coalaCSS library. The main motivation was to help us unify all the scattered CSS, and bring consistency across projects. So, initially I made a list of all the custom components used in landing-frontend, and then created parent classes for these components. Next thing was to generalize the classes and use pre made classes wherever possible, which Lasse helped me understand that this is the whole point of making a CSS class. 


Then I proceeded to completely eliminate bootstrap and use MaterializeCSS for columns. At first it went quite ok, but then when I tested the output on mobile device, It was way different than the expected. The solution was to use the col s1, col s2 and such classes made for small screens, available in MaterializeCSS.


The next thing was to iterate the same process over projects.coala.io, and create parent classes for custom components exclusive to this web project. 

You can see the sparkles for coala Web projects right here on : 
https://github.com/coala/coalaCSS


That's all folks!

Thank You
