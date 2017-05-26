---
layout: post
title: "coala-ifying landing-frontend, webServices and projects"
description: "GSoC Bonding Period Week 3"
categories: ["stories", "coala"]
bg: images/8.png
header_color: crimson
---

This week I worked on making code in landing-frontend, webServices and projects coala compliant. The aim was to add more critical sections in coafiles, then run coala and do fixing. I added the SpaceConsistencyBear in all three of them. There is a reason why I love this bear more and it is because this is one of the bears which can detect and then FIX stuff as well! Isn't that totally superawesome. You don't have to worry about going navigating through the files to fix the error, instead it fixes the stuff itself, and as a 'user' I am really more than happy to integrate such linters in CI for my all projects. Okay let me tell you one more, it actually fixes the spacing/tab issues for you, without you having to do a thing.

So let me share how we can setup SpaceConsistencyBear for coding projects.


First thing, create a .coafile in the root of repo
.coafile
```
#Empty huh, lets fill it.
```

Add a section, all
```
[all]
```

Add bear,
```
[all]
bears = SpaceConsistencyBear
```

Tell them thethe bears what files it should do the fix
```
[all]
bears = SpaceConsistencyBear
files = **.(html|md|css|js|py)
```

Then tell them what to ignore
```
[all]
bears = SpaceConsistencyBear
files = **.(html|md|css|js|py)
ignore = vendors/**
```

And then finally, choose what you want to use throughout your project,
Spaces or Tabs
```
[all]
bears = SpaceConsistencyBear
files = **.(html|md|css|js|py)
ignore = vendors/**
use_spaces = yeah
```

If you want to use tabs, do ```use_spaces = no``` ok.

Then run coala on your project, preferably with
```
coala --apply-patches
```
And then see the action !

Thank You
