---
layout: page
title: current
permalink: /current/
---
<ul class="post-list">
	{% for post in site.posts %}
	  {% if post.tags contains 'current' %}
	  <li style="border-top:1px solid grey; padding-top: 20px">
            {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
            <img src="{{post.img}}" style="float:right;max-height:80px" />
            <span class="post-meta">{{ post.date | date: date_format }}</span>
            <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
        </li>
	  {% endif %}
	{% endfor %}
</ul>
