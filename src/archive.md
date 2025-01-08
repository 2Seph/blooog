---
title: archive
layout: "home.njk"
---

<div class="archive-text">
    <details>
        <summary>study notes</summary>
        <ul>
            {% assign studyCollection = collections.study | sort: "date" | reverse %}

            {% for study in studyCollection %}
                <li> <a href="{{study.url}}">{{study.data.title}} ({{study.data.date | postDate }}) </a> </li>
            {% endfor %}
        </ul>
    </details>

    <details>
        <summary>journal entries</summary>
        <ul>
            {% assign journalCollection = collections.journal | sort: "date" | reverse %}

            {% for journal in journalCollection %}
                <li><a href="{{journal.url}}">{{journal.data.title}} ({{journal.data.date | postDate }})</li>
            {% endfor %}
        </ul>
    </details>
    
</div>
