---
layout: page
title: Portfolio
permalink: /portfolio/
---

{% for project in site.portfolio %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" style="width: 100%; height: 100%; position: static; object-fit: cover;"  src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ project.url }}">
        {% if project.img %}
        <img class="thumbnail" style="width:100%; height: 100%; position: static; object-fit: cover;" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}

<hr/>
<br/>
<span class="contacticon center">
	<a href="mailto:wone.choi.0401@google.com"><i class="fa fa-envelope-square"></i></a>
	<a href="https://github.com/wonechoi" target="_blank"><i class="fa fa-github-square"></i></a>
	<a href="https://www.linkedin.com/in/hyewon-choi-519bb8177/" target="_blank"><i class="fa fa-linkedin-square"></i></a>
</span>

<div class="col three caption">
	&copy; HYEWON CHOI
</div>