---
layout: page
title: team
permalink: /team/
---
<style type="text/css">
table {
  border-collapse: collapse;
  width: 100%;
}

th, td {
  padding: 8px;
  text-align: left;
  border-bottom: 1px solid #ddd;
}

tr:hover{
  background-color:#f5f5f5
}
.projectlink {
  background : rgba(0, 132, 0, 0.3);
  padding:2px;
}
</style>
name | proficiencies | projects | location
--- | --- | --- | ---
king.ho@greenpeace.org | html, css, js, php, node, c, c++, c# | {% for post in site.categories.project %}{% if post.tags contains 'kiho' %}<a class='projectlink' href='{{ post.url | relative_url }}'>{{ post.title | escape }}</a>{% endif %}{% endfor %} | Amsterdam, Netherlands

<div>
  <ul class="post-list">
    <table>
      <thead>
        <th>name</th>
        <th>proficiencies</th>
        <th>projects</th>
        <th>location</th>
      </thead>
      <tr>
        <td>king.ho@greenpeace.org</td>
        <td>html, css, js, php, node, c, c++, c#</td>
        <td>
          {% for post in site.categories.project %}
          {% if post.tags contains 'kiho' %}
            <a class='projectlink' href='{{ post.url | relative_url }}'>{{ post.title | escape }}</a>
          {% endif %}
          {% endfor %}
        <td>Amsterdam, Netherlands</td>
      </tr>
      <tr>
        <td>torbjorn.zetterlund@greenpeace.org</td>
        <td>html, css, js, php, node</td>
        <td>
          {% for post in site.categories.project %}
          {% if post.tags contains 'tzetterl' %}
            <a class='projectlink' href='{{ post.url | relative_url }}'>{{ post.title | escape }}</a>
          {% endif %}
          {% endfor %}
        </td>
        <td>Amsterdam, Netherlands</td>
      </tr>
      <tr>
        <td>stefan.behnke@greenpeace.org</td>
        <td>php, RFID tech</td>
        <td>
          {% for post in site.categories.project %}
          {% if post.tags contains 'sbehnke' %}
            <a class='projectlink' href='{{ post.url | relative_url }}'>{{ post.title | escape }}</a>
          {% endif %}
          {% endfor %}
        </td>
        <td>Hamburg, Germany</td>
      </tr>
    </table>    
  </ul>
</div>

