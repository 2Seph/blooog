---
title: back end
date: 2025-01-10T19:00:00.000Z
tags:
  - study
---
upon trying to bring my 'giforecast' idea to life, i rant into a lot of trouble and confusion, youtube videos were not a lot of help. so now, thanks to a 'how to get started with backend' post on reddit, i'm gonna try and learn from the ground up with fullstackopen.com/en. comments also mentioned that taking up computer science will put you on the right track to learning design architecture and network stuff anyway. but, i'm impatient, and i have the **audacity** to dive into this magical backend stuff. i'll be using this post for my notes. fuck python, fuck everyone. let's fucking go (pt.2)

<img src="https://i.pinimg.com/736x/ef/b5/11/efb5119dc51f634bbca577bae2e03a4e.jpg" style="display:block; margin-left:auto; margin-right:auto; width:300px;">

<br>

<h2>0.0 fundamentals of web apps</h2>

when making web apps it's essential to have developer console open, (fn+f12 on chrome and shift+alt+i on firefox). the guide commands i disable cache coz thats good (found on network tab) & enable preserve log if i wanna save past logs.

the guide points me to the network tab to understand how the browser & server communicates with HTTP protocol. Where if i refresh the page, some activities on the left side shows up, and from my understanding these activities are the browsers' HTTP requests, or what the browser wants from the server. If I click on the activity, there are several headers I can look into that give me more info about what happened, for example: the request url, request method, status code, content type & date.

<img src="https://note.nekoweb.org/network.png" 
style="width:400px; display:block; margin-left:auto; margin-right:auto;">

<br>

the chain of events caused by opening this page: 
* browser sends -> HTTP GET html code of page -> server -> gives html document
* broswer sends -> HTTP GET img -> server -> gives img

the guide also tells me that a **callback function** is simply a function that is passed as an argument to another function and executed later, often in response to an event. 

and that the browser is the frontend, the JavaScript that runs on the browser is the frontend code. The server on the other hand is the backend.

<h4>assignments for 0 - chain of events</h4>

<a href="https://fullstackopen.com/en/part0/fundamentals_of_web_apps#forms-and-http-post">this might help</a> 
1. depict situation when user creates a new note (by writing smth on text field and clicking save button) on ./exampleapp/notes 
2. depict situation when user goes to the ./exampleapp/spa version of notes app
3. depict situation when user creates a new note in ./exampleapp/spa

(remember 0.1 will be abt react which chantal & most developers know, dont get left behind by getting scared of fake assignments)
