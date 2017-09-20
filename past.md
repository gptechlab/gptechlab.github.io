---
layout: page
title: past
permalink: /past/
---
<ul class="post-list">
    {% for post in site.categories.project %}
    {% if post.tags contains 'past' %}
      <li style="height:80px; border-top: 1px solid rgba(0,0,0,0.2);">
            {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
            <img src="{{post.img}}" style="max-height:80px" />
            <span class="post-meta">{{ post.date | date: date_format }}</span>
            <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
        </li>
      {% endif %}
    {% endfor %}
  </ul>
