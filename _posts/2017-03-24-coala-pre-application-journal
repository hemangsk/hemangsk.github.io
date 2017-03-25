---
layout: post
title: "The Pre Application Period Journal"
description: "Ideas and proofs of concept for the future coala.io"
categories: ["stories", "coala"]
bg: images/8.png
header_color: crimson
---

##### Ideas and proofs of concept for the future coala.io

The Google Summer of Code 2017 have opened their student application window. I'm really excited and I'm going to applying under [coala](http://coala.io) :) for the project _Improve coala Website and Supporting Tools_.

There are a lot of, a lot of proposals expected and only few make it through the multiple levels of evaluation. If I can make it through, that'll add a bucket of summer of code awesomeness to my already awesome journey with coala and contributing to Open Source so far. I have lot of plans and lots of conceptualization on which I am working, refining them and adding them to my application if they fit just right.

I'm planning to cover the following objectives, 
- Creating a powerful backend to run coala online by developing the ```coala Online Module```.
- Making the coala ```Projects``` web application completely configurable, modular and extensible.
- Creating a centralized CSS and HTML components source for all coala web Projects.
- Enhancement of ```coala-html```

The first objective, ```coala Online module```.

Why ? The aim is to provide users an interface to do in-browser linting. I am planning on achieving this by providing two running modes in ```coala-quickstart```, ```which-bears``` and ```get-settings-from-json```. The main features of these settings will be that there will be no need for user to enter input midway through the process. 
This will really help because when ```coala-quickstart``` will be running inside the webservices on some code entered by user, it will 
```
read_all_settings_from_a_json 
-> run 
-> output json
``` 
and so on. 
There will be no need of 
```
run 
-> coala-quickstart says: "I want an Input from user!!, Go back to frontend and ask for user input" and shell is paused until then 
-> Come back with user input and feed it to shell 
-> Continue with execution 
-> output_json
```
As there is a disadvantage related to asking user input for shell that I read about during research, that giving shell input right to user is not a good idea. Sounds right, because someone might enter malicious code in the shell.

How ? Django has performed really awesome till now, therefore it will be just perfect to implement the module in Django, inside ```coala``` 's Docker base image. The main tasks here will be to refine on the proposed changes in coala-quickstart, apart from that, creating the engaging web UI where user will be entering settings for bears will be exciting and challenging. This module will go in the Try coala section on coala.io, which we can then rename to coala Online.

For the second objective, Using a ```YAML``` parsing module for Angular, to basically minimize use of ```JSON``` while creating projects in ```Projects webapp```. 

Why ? JSON has great compatibility with Angular, but as a project creator point of view, there are several rules to follow while creating projects metadata and that makes the process cumbersome. 

How ? So a project can be created by a single file,
```
field1: 
field2: 
field3:
```
And thus leaving no room for conflicts while multiple projects being added at the same time. Then there are some important features which the ```Projects webapp``` needs, One is the timeline for tracking progress. The projects can be In Progress, Completed and To be Started. The appraoch I am thinking of doing this is a custom version of [Angular Timeline Component](http://rp.js.org/angular-timeline/example/index.html). This will make tracking progress and adding new status updates related to project. really straightforward.

The [YAML parser](https://nodeca.github.io/js-yaml/) 's another usage is in making the webapp configurable. 
The need for this is directly focussed on increasing the webapps usability  for the community. So it will provide the user the option to create a configuration file, from where the settings will be fetched and final webpage is generated. As a thought, ```YAML``` wins here, as Jekyll, Travis and others have been using it to get user's configuration and its proven itself pretty convenient. 
So A config.yml will be present, in which we can take input for various parameters, 
```
your_organisation_name : <>
your_organisation_logo_link: <>
your_organisation_license : <>
color_scheme : <>
```
And other organisation will be able to get up and running with their own version Projects webapp in no time!

Coming to the third objective, the main aim will be to, decouple, refactor and document the CSS and HTML components that we are using across web projects.

Why ? So that it is easier to solve bugs in them and manage them. Then we can provide link to the CSS, and that link can be used everywhere with 
```
<link href="http:// <cdn-url> .coala.css"></link>
```
How ? Two good services that I have shortlisted and tried out are jsDelivr https://www.jsdelivr.com/ and rawgit https://rawgit.com/, while in rawgit there is no traffic limits or throttling and it is powered by StackPath's super fast global CDN. So essentially, we'll have fast webpages, easy to manage CSS framework, and well documented components which can be used in any web project. Removing the redundant CSS, making Better Media Queries, using SASS or LESS for precompose tasks. Then separating HTML markup structure of UI elements, and documenting them. 

#### coala-html, Awesomeness!
coala-html is an interactive tool, which gives users the option to view the analysis results in browser, with some beautiful CSS and powerful AngularJS. coala-html started taking shape last summer, and it’s ready for some more power packed features. That will be the most important objectives of this project.

Ideas,
The most well defined of all the ideas I’ve been planning in coala-html is the much required Result Search Mechanism.
Grouping of Results, Addition of filters based on Severity, Bears, Files.
The other useful feature for users would be to show Interactive Graphs and Statistics of Analysis Performed, powered by D3.js.
	This will be a representation of the Results using visualizations.

I feel displaying pictorial graphs of severity of issues with the code, can really help the development team to get a view of how much code they have fixed and how much code is still in bad condition and needs to be refactored.

The major aim is to provide meaningful and useful  “Analysis of Analysis” in coala-html. Apart from it, coala-html can use some more of the Material Design. The Card Views for Results, and better colors in syntax highlighting.

 That’s all folks!
