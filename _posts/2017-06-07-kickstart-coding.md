---
layout: post
title: "The Silence of the CI"
description: "GSoC Coding Period Week 1"
categories: ["stories", "coala"]
bg: images/8.png
header_color: cadetblue
---

Coding Period has begun and first week comes to an end. This week I worked on adding a new option in ```coala-quickstart``` which is a utility that creates coafiles for you blazing fast. coafile is the config file which lets you configure and customize coala linting on your code. 

This new option is called, ```--allow-incomplete-sections```. 

Continous Integration or CI as we also call it, is a development practice that requires developers to integrate code into a shared repository several times a day. Each code commit or pull request is then verified by an automated build, allowing teams to detect problems early. Developers make CI softwares, the one which provide automated builds and automated linting on every PR's push made. 

If you want to have such a mechanism, that you want to run a software on your code everytime a commit is pushed, you add a feature in your code which allows it to run silently (without asking user input, the input is your code which you pushed). 

In script programs, one way to do this is adding a ```--ci``` like argument and informing everywhere in your code that, "Hey CI mode is on, don't ask for any input!". 

coala-quickstart has a CI mode already and it skipped all the input questions except one, Here is the [commit](https://github.com/coala/coala-quickstart/commit/f459086447bacdfe8dc2af55e02cfe71c3940203) in which we fixed it. 

Then I added the new option, the new option basically allows the users to get unusable
bears (bears which have non optional settings) as well in generated coafile. 

During the review process, I learnt about various testing tools and code coverage tools like codecov, dived a level deeper into pytest, learnt about mock module in python. Every PR at coala is a learning experience because we students get so much to learn in a single PR. 
My mentors Lasse and Fabian have planned a systematic way of working, meeting and progress reporting for us. 

The coming week is going to be 'ultra' great. 
Hope we can get coala Online on coala.io is gonna run non optional bears soon!

Have a great day!
