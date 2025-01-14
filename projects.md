---
layout: page
title: Projects
permalink: /projects/
---

## Introduction
The intention of this post is to:
* Provide a place for me to point to when applying for work/job to show proof of my skills and showcase projects I have done or been a part of.
* Provide a quick reference for myself to keep track of what I have done previously to make decisions of future projects to not duplicate things I have done already.

<!-- On my way to completing my Master's degree in CS, I wish to start applying the awesome things I have been learning and also try to get opportunities to use the things I learned to contribute in helping build a product or service by getting a job. -->

<!-- Looking online, I see people have impressive portfolio's to show their skills and the cool projects they have been a part of. I want to do that too. For me, a precursor for that is what I have done already. -->

## Project List (Count: {{site.data.projects | size}})
> Note: Click on a project to read more about it.

<!-- Filter by tags: -->
<!-- Add buttons to use here -->


{% for project in site.data.projects %}
<details>
    <summary>
        {{project.name}} 
        <!-- <div style="display:flex; float:right">
            {% for category in project.categories %}
            <span style="margin-right:10px;border:solid red;border-radius:10%;">
                {{category}}
            </span>
            {% endfor %}
        </div> -->
    </summary>
    <strong>Description:</strong>
    {% if project.description %}
    {{project.description}}
    {% else %}
    <em>(Project Description will be added soon)</em>
    {% endif %}
</details>
---
{% endfor %}


<!-- {% for project in site.data.projects %}
{% if project.categories contains "python" %}
* {{project.name}}
{% endif %}
{% endfor %} -->

<!-- ---

{% assign categories = "" | split: ',' %}
{% for project in site.data.projects %}
    {% for category in project.categories %}
        {% unless categories contains category %}
            {% assign categories = categories | push: category %}
        {% endunless %}
    {% endfor %}
{% endfor %}

<!-- <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous"> 

{% for category in categories %}<span class="btn btn-sm btn-outline-dark" style="margin-right:10px">{{category}}</span>{% endfor %} -->