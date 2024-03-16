---
published: true
title:  # ruang tajuk sengaja tidak diisi
---

Berikut adalah senarai laman (bersuai) yang boleh dicapai:

{% assign pages = site.pages | sort: "path" %}
{% for p in pages %}
&nbsp;. {{ p.path }}{% if p.title %}
<a href="{{ site.url }}{{ p.url }}">{{ p.title }}</a>{% endif %}
<br>{% endfor %}

{% comment %}
kod liquid diliputi oleh `if` supaya sebarang fail tanpa
bahagian awal dan tanpa tajuk boleh dikecualikan sekaligus;
pautan hanya dijana apabila bahagian awal `title:` hadir.

objek `{{ site.url }}{{ p.url }}` mewakili alamat mutlak,
manakala `{{ p.url }}` mewakili alamat relatif laman;
tiada beza bagi localhost, tetapi perlu guna alamat mutlak
apabila menjana pautan di luar index
{% endcomment %}

laman kembali: [utama][0]

  [0]: index.md
