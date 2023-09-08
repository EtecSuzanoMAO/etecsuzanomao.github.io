---
layout: page
title: Arquivos
---

Pesquise todos os artigos por mês e ano

{% assign postsByYearMonth = site.posts | group_by_exp: "post", "post.date | date: '%m/%Y'" %}
{% for yearMonth in postsByYearMonth %}
  <h2>{{ yearMonth.name }}</h2>
  <ul>
    {% for post in yearMonth.items %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
