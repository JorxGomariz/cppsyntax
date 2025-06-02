---
layout: default
title: "Sintaxis de C++"
permalink: "/"
---

# Bienvenido a Sintaxis de C++

En este sitio encontrarás diferentes unidades (temas) sobre sintaxis de C++.  
Haz clic en la unidad que te interese:

<ul>
{% for unidad in site.unidades %}
  <li>
    <!-- "{{ unidad.url }}" ya incluye baseurl (gracias a baseurl: "/cppsyntax") -->
    <a href="{{ unidad.url | relative_url }}">{{ unidad.title }}</a>
  </li>
{% endfor %}
</ul>

