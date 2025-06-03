---
layout: home
title: "Sintaxis de C++"
permalink: "/"
---

# **Página principal**
 
Haz clic en la unidad que te interese:

<ul>
{%- assign sorted_unidades = site.unidades | sort: 'order' -%}
{% for unidad in sorted_unidades %}
  <li>
    <a href="{{ unidad.url | relative_url }}">{{ unidad.title }}</a>
  </li>
{% endfor %}
</ul>

