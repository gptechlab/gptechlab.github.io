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
</style>
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
          <a href='{{ post.url | relative_url }}'>{{ post.title | escape }}</a><br>
        {% endif %}
        {% endfor %}
      <td>Amsterdam, Netherlands</td>
    </tr>
    <tr>
      <td>torbjorn.zetterlund@greenpeace.org</td>
      <td>html, css, js, php, node</td>
      <td><a href='https://gptechlab.github.io/project/2017/09/18/plastic-tracking-app.html'>plastics tracking</a></td>
      <td>Amsterdam, Netherlands</td>
    </tr>
    <tr>
      <td>stefan.behnke@greenpeace.org</td>
      <td>php, RFID tech</td>
      <td></td>
      <td>Hamburg, Germany</td>
    </tr>
  </table>    
</ul>
