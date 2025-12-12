---
published: true
title:  # ruang tajuk sengaja tidak diisi
---

Berikut adalah kandungan (bersuai) yang boleh dicapai:

{% include_relative baca/kandungan.md %}{% comment %}
&brvbar; [baca/kandungan.md](baca/kandungan.md)
{% endcomment %}

----

Senarai laman tanpa susunan bab:

{% assign pages = site.pages | sort: "path" %}
{% for p in pages %}
&nbsp;{{ p.path }} {% if p.title %}..
[{{ p.title }}](.{{ p.url }})
{% endif %}{% comment %}sini ada baris baru{% endcomment %}
{% endfor %}

{% comment %}
kod liquid diliputi oleh `if` supaya sebarang fail tanpa
bahagian awal dan tanpa tajuk boleh dikecualikan sekaligus;
pautan hanya dijana apabila bahagian awal `title:` hadir.

objek `{{ site.url }}` dan `{{ site.baseurl }}` kelihatan
sama tetapi tidak serupa;
`{{ site.url }}` boleh mewakili alamat laman mutlak, tetapi
sah untuk index sahaja, dan bukan untuk laman selain itu.

objek `{{ site.baseurl }}{{ p.url }}` mewakili alamat mutlak
dan `{{ p.url }}` mewakili alamat relatif laman;
tiada beza bagi localhost, tetapi perlu guna alamat mutlak
apabila menjana pautan di luar index

objek `.{{ p.url }}` juga mewakili alamat mutlak, kerana
imbuhan aksara titik `.` di hadapan alamat laman adalah
setara dengan `{{ site.baseurl }}` apabila dijana.
{% endcomment %}

{% assign tajuk = "kembali ke laman utama" %}
[{{ tajuk }}](.{% link index.md %}){% comment %}
&brvbar; [index.md](index.md){% endcomment %}
