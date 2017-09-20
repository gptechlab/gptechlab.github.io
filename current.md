---
layout: page
title: current
permalink: /current/
---
<ul class="post-list">
	{% for post in site.posts %}
	  {% if post.tags contains 'current' %}
	  <li style="height:80px; border-top: 1px solid rgba(0,0,0,0.2);">
            {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
            <a href="{{ post.url | relative_url }}"><img src="{{post.img}}" style="max-height:80px" /></a>
            <span class="post-meta">{{ post.date | date: date_format }}</span>
            <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
        </li>
	  {% endif %}
	{% endfor %}
</ul>
