---
layout: page
title: Categorias
---

<div class="categorias">
  {% for category in site.categories %}
    <article class="tutorial">
      <h2><a href="{{ site.baseurl }}{{ category.url }}">{{ category.title }}</a></h2>
    </article>
  {% endfor %}
</div>
