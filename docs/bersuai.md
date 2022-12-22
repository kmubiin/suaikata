---
published: true
---

Berikut adalah senarai laman (bersuai) yang boleh dicapai:

{% assign pages = site.pages | sort: "path" %}
{% for p in pages %}
&nbsp;. {{ p.path }}{% if p.title %}
<a href="{{ p.url }}">{{ p.title }}</a>{% endif %}<br>{% endfor %}

{% comment %}
kod liquid diliputi oleh `if` supaya sebarang fail tanpa
bahagian awal dan tanpa tajuk boleh dikecualikan sekaligus;
pautan hanya dijana apabila bahagian awal `title:` hadir.
{% endcomment %}

laman kembali: [utama][0]

  [0]: index.md
