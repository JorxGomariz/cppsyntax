---
layout: home
title: "**Sintaxis de C++**"
permalink: "/"
---

# ïndice
 
Haz clic en la unidad que te interese:

<ul>
{% for unidad in site.unidades %}
  <li>
    <!-- "{{ unidad.url }}" ya incluye baseurl (gracias a baseurl: "/cppsyntax") -->
    <a href="{{ unidad.url | relative_url }}">{{ unidad.title }}</a>
  </li>
{% endfor %}
</ul>

