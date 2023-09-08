---
layout: page
title: Creditos
---

{% for membro in site.data.credits %}

## {{ membro.name }}

Do Grupo: {{ membro.group }}

{% endfor %}

<br/>
### Esse site não seria possivel sem essas ferramentas

{% for ferramenta in site.data.foss %}

## {{ ferramenta.name }}

{{ ferramenta.url }}

{% endfor %}