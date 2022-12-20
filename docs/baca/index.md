---
published: true
title: Kandungan
---

### Kandungan

#### Senarai daftar

Daftar kata boleh didapati di laman sumber dan tidak dipapar
di laman ini. Sebaliknya, laman ini hanya menyediakan
[salinan terhad daftar](contoh.md).

Senarai daftar kata yang rasmi:

{% assign d = site.data.daftar %}
<ul>{% for sa in d %}{% if sa.rasmi %}
<li>"{{ sa.alt }}"{% capture n %}{% increment i %}{% endcapture %}
oleh {{ sa.oleh.ahli | join: ", " }}</li>
{% endif %}{% endfor %}</ul>

Bilangan daftar rasmi/semua:
{{ n | plus: 1 }}/{{ d | size }}

#### Senarai ura

Laman berikut disediakan untuk bacaan umum.

> senarai rencana di sini

#### Senarai bab

Laman berikut disediakan mengikut [dasar ini](dasar.md).

> senarai laman dari rak panduan

Terdapat istilah-istilah yang muncul semasa menyediakan
kandungan laman dalam senarai di atas. Senarai istilah itu
dikumpul dan dipapar terus dalam [glosari](glosari.md).

laman kembali: [utama][0]

  [0]: ../index.md
