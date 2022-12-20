---
published: true
title: Senarai laman
---

### Senarai laman (bersuai)

{% assign pages = site.pages | sort: "path" %}
{% for p in pages %}
&nbsp;. {{ p.path }}
<a href="{{ p.url }}">{{ p.title | default: "..." }}</a><br>{% endfor %}

laman kembali: [utama][0]

  [0]: index.md
