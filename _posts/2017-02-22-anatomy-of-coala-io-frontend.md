---
layout: post
title: "Anatomy Of The coala.io Frontend"
description: "How we created exciting elements for various usecases"
categories: ["stories", "coala"]
---

You must have read Kaisar's post ([Here's the link](https://yukiisbored.github.io/blog/2017/02/17/backend-voodoo-magic.html)) about the creating a stable and powerful Backend. It's an account of how the backend server was made stable, and reached a super amazing uptime, Hats Off to @yukiisbored, our DevOps star. Thanks for always being there!

This project is now finally in a stable state, Props to our community team leader [@sims1253](http://github.com/sims1253), Thanks you so much for trusting me with this responsiblity and for helping out to solve edge cases with UI. 


The new coala.io aims to fulfill the purpose of **ease in getting started with coala** and **to provide a bear search mechanism**. Thanks a ton [@sils](http://github.com/sils) for giving me an opportunity to work on coala.io frontend, This gave me a tremendous opportunity to learn from you and together we were able to create some fantastic components. 


Its under Lasse's and Maximilian's awesome supervision that this project finished, and more cool projects are going on. Stay tuned to community team's blog updates.


While creating the frontend, we had several interesting use cases to ponder upon. More often then not, they required minor or major restructure of default components provided by Materialize, the great library it is. We created several components based on Materialize and Angular.


<br>
<hr>


#### Dropdown + Caret

In the getting involved section, we required a dropdown for user to select languages and then they will shown corresponding example of coala usage. The default Materialize 'Dropdown' doesn't come with a caret. There is another similiar component 'Select' in Materialize that comes with a caret but this way there's no background color. 


![](/images/2.png) 
![](/images/3.png)


As soon as we added background color property to 'Select', color is added but that doesn't fit well without appropriate padding and margin, so this is what we did, To the ```<input>``` element, we added
```
background-color: color;
```

And to caret ```<span>```
```
padding-left: 10px;
```

**Result**

![](/images/1.png)

<hr>

#### Chip Links

Beneath the coala heading in the main page, there are 3 chips with icons linked to docs, source and chat. 

After adding fontawesome icons inside the chip, there is an alignment issue.

![](/images/5.png) 

After a 2:3 ratio of ```margin-right``` and ```margin-left```, and 1:1 ratio of ```padding-bottom``` and ```padding-top```, 

![](/images/4.png)

Darken ```background``` on hover and its all set!

<hr>

#### Contributor Card-View

In the Get Involved section there are cards in which data for each Developer is displayed. Our aim was to incooperate Reviews, Issues Opened, Commits, Bio, Display Picture, Full Name and User name. So we created a two cards, one to be left empty but having a height, and one for contents, and added the display picture exactly in the middle of these two cards. Interestingly, display pictures having transparent background look even more awesome with this effect. Props to [@fneu](http://github.com/fneu) for structuring the Data section in a single row giving equal widths to all 3 data subsections making it super awesome, displaying the count of Commits, Reviews and Issues of Developers.

![](/images/7.png) ![](/images/6.png) 

That's all folks!
There are a lot more components which I'll make sure to share in upcoming posts :) 

Easter Egg:- There's also another frontend work going on presently at the community team, we are Materializing coala Docs. Yeah! Sneak Peek coming real soon! 

G'Bye!
