---
title: home
layout: "home.njk"
---


<div class="index-text">

<img src="https://i.pinimg.com/736x/40/1c/54/401c541931fe54d99cdba80594123852.jpg"
style="max-width:70%;">


welcome!!


<br>

<div class="index-a">
    <b>recent study notes:</b>
        {% assign recent_study_posts = collections.study | sort: 'date' | reverse %}
        {% for study in recent_study_posts limit:2 %}
            <li><a href="{{ study.url }}">{{ study.data.title }}</a></li>
        {% endfor %}
    </div>

<br>
    
    <div class="index-a">
    <b>recent journal entries:</b>
        {% assign recent_journal_posts = collections.journal | sort: 'date' | reverse %}
        {% for journal in recent_journal_posts limit:2 %}
            <li><a href="{{ journal.url }}">{{ journal.data.title }}</a></li>
        {% endfor %}
    </div>




<!-- TO DO:

- styling
- deploy to github
- setup with netlify
- setup with cms


-->


<!-- IDEAS:

- archive by month

-->



</div>