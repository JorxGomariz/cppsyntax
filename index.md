---
layout: home
permalink: "/"
---

# Página principal
 
Haz clic en la unidad que te interese:

<ul>
{% for unidad in site.unidades %}
  <li>
    <!-- "{{ unidad.url }}" ya incluye baseurl (gracias a baseurl: "/cppsyntax") -->
    <a href="{{ unidad.url | relative_url }}">{{ unidad.title }}</a>
  </li>
{% endfor %}
</ul>

