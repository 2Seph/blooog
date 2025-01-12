---
title: back end
date: 2025-01-10T19:00:00.000Z
tags:
  - study
---
upon trying to bring my 'giforecast' idea to life, i rant into a lot of trouble and confusion, youtube videos were not a lot of help. so now, thanks to a 'how to get started with backend' post on reddit, i'm gonna try and learn from the ground up with fullstackopen.com/en. comments also mentioned that taking up computer science will put you on the right track to learning design architecture and network stuff anyway. but, i'm impatient, and i have the **audacity** to dive into this magical backend stuff. i'll be using this post for my notes. fuck python, fuck everyone. let's fucking go (pt.2)

<img src="https://i.pinimg.com/736x/ef/b5/11/efb5119dc51f634bbca577bae2e03a4e.jpg" style="display:block; margin-left:auto; margin-right:auto; max-width:300px;">

<br>

<h2>0.0 fundamentals of web apps</h2>

when making web apps it's essential to have developer console open, (fn+f12 on chrome and shift+alt+i on firefox). the guide commands i disable cache coz thats good (found on network tab) & enable preserve log if i wanna save past logs.

the guide points me to the network tab to understand how the browser & server communicates with HTTP protocol. Where if i refresh the page, some activities on the left side shows up, and from my understanding these activities are the browsers' HTTP requests, or what the browser wants from the server. If I click on the activity, there are several headers I can look into that give me more info about what happened, for example: the request url, request method, status code, content type & date.

<img src="https://note.nekoweb.org/network.png" 
style="max-width:300px; display:block; margin-left:auto; margin-right:auto;">

<br>

the chain of events caused by opening this page: 

* browser sends HTTP GET request of html code of page -> server gives html document
* broswer sends HTTP GET request of img -> server gives img

the old ways of handling form submissions included sending form data to server then reloading the page & fetching back all the files html,css,js,json. form also had action (a url where data will be sent), and a method (post). the spa way of doing it on the other hand is; no action & method in the form (but just an id), and no page reload when there's a new form submission. my assignment answer for this can be found [here](https://docs.google.com/document/d/1Y8clXXFTHbqERVwwLrkHW3hzn9CIFJlZQNccNOgspBs/edit?usp=sharing)

the guide also tells me that a **callback function** is simply a function that is passed as an argument to another function and executed later, not when the page loads, but in response to a specific event.

and that the browser is the frontend, the JavaScript that runs on the browser is also the frontend code. The server on the other hand is the backend.

<h2>1.0 intro to react</h2>

the guide shows me how to start a react app with vite, which will be called 'introdemo.' first i had to install libraries:

```
npm create vite@latest introdemo -- --template react
cd introdemo
npm install
npm run dev  <<- how to run it
```

and i only had to copy paste some code in some files

main.jsx was simplified to:

```
import ReactDOM from 'react-dom/client'

import App from './App'

ReactDOM.createRoot(document.getElementById('root')).render(<App />)
```

and app.jsx was simplified to:

```
const App = () => {
  return (
    <div>
      <p>Hello world</p>
    </div>
  )
}

export default App
```
