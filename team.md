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
king.ho@greenpeace.org | html, css, js, php, node, firebase, c, c++, c# | {% for post in site.categories.project %}{% if post.tags contains 'kiho' %}<a class='projectlink' href='{{ post.url | relative_url }}'>{{ post.title | escape }}</a>&nbsp;{% endif %}{% endfor %} | Amsterdam, Netherlands
torbjorn.zetterlund@greenpeace.org | html, css, js, php, node, firebase | {% for post in site.categories.project %}{% if post.tags contains 'tzetterl' %}<a class='projectlink' href='{{ post.url | relative_url }}'>{{ post.title | escape }}</a>&nbsp;{% endif %}{% endfor %} | Amsterdam, Netherlands
cliodhna.kirk@greenpeace.org | html, css, js | {% for post in site.categories.project %}{% if post.tags contains 'ckirk' %}<a class='projectlink' href='{{ post.url | relative_url }}'>{{ post.title | escape }}</a>&nbsp;{% endif %}{% endfor %} | Amsterdam, Netherlands
jack.blackwell@greenpeace.org | html, css, js, node, firebase | {% for post in site.categories.project %}{% if post.tags contains 'jblackwe' %}<a class='projectlink' href='{{ post.url | relative_url }}'>{{ post.title | escape }}</a>&nbsp;{% endif %}{% endfor %} | Amsterdam, Netherlands
gabriel.harte@greenpeace.org | python, js | {% for post in site.categories.project %}{% if post.tags contains 'gharte' %}<a class='projectlink' href='{{ post.url | relative_url }}'>{{ post.title | escape }}</a>&nbsp;{% endif %}{% endfor %} | Amsterdam, Netherlands
fabian.krautgasser@greenpeace.org | python, C | {% for post in site.categories.project %}{% if post.tags contains 'fkrautga' %}<a class='projectlink' href='{{ post.url | relative_url }}'>{{ post.title | escape }}</a>&nbsp;{% endif %}{% endfor %} | Amsterdam, Netherlands
