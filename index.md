---
layout: home
title: "Sintaxis de C++"
permalink: "/"    # garantiza que la Home sea la raíz
---

# Bienvenido a la Sintaxis de C++

Aquí encontrarás los distintos temas organizados por unidades. Haz clic en el que necesites:

<ul>
{% for unidad in site.unidades %}
  <li>
    <a href="{{ unidad.url }}">{{ unidad.title }}</a>
  </li>
{% endfor %}
</ul>

