---
layout: post
title: "Iteration Game"
description: "GSoC Coding Period Phase II"
categories: ["stories", "coala"]
bg: images/8.png
header_color: pink
---

Here we go! the coafile bot is merged into GitMate-2. Its been a journey of full of celery beat with python bot which uses polling every 10 seconds. Expanding on the restrictions of a cron, celery allows us to keep schedule in seconds for a repetitive task. So if you are planning to have a repetitive task in a Django website, or a python project in general, go with celery.

I'm gathering all the use cases where I found celery can do wonders,

#### Repetitive interactions with REST APIs
- Suppose you have a Django project, you want to have a task/mechanism/code to fetch data from another API by making http calls to that API, and using django models it should save that fetched data into DB, and this is a repetitive task which you want to keep doing every other hour for example. Celery Beat is the answer. :)

#### Making polling bots
- For polling bots, Celerey can do the job of running a function after every set amount of seconds, so there you go, your bots driver function can run every 5 seconds, no time.sleep() (not that there's any bad with time.sleep(), its just that celery has workers and it plays well with scaling)

#### Mammoth tasks whilst scaling better
- Suppose I have a form in my webapp, someone fill and submits that form, I get the form data in backend, do some processing, okay, heavy processing, like I spawn a docker container, and return the results obtained from that docker container back to backend, and backend responds back to frontend. Now celery's the friend, it can balance the load and/or make it synchronous/async. 

I'd share some more insights once I get some time after the phase if officially ends, and I will sit and collect and some more info to share. 

Right now I'm working on adding tests for project.coala.io, its html-proofer, the amazing utility that checks the html file for any kinds of errors and plays beautifully with jekyll and travis.

