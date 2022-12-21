---
published: true
title: Kandungan
---

### Kandungan

#### Senarai daftar

Daftar berikut disediakan mengikut rancangan.

<ol>{% for sa in site.data.daftar %}{% if sa.rasmi %}
<li>"{{ sa.alt }}"
oleh {{ sa.oleh.ahli | join: ", " }}</li>
{% endif %}{% endfor %}</ol>

Daftar kata boleh didapati di laman sumber dan tidak dipapar
terus di laman ini. Sebaliknya, laman ini hanya menyediakan
[salinan terhad daftar](contoh.md).

#### Senarai ura

Laman berikut disediakan untuk bacaan umum.

> senarai rencana di sini

#### Senarai bab

Laman berikut disediakan untuk panduan projek.

> senarai laman dari rak panduan

Semua laman dalam senarai bab di atas disediakan mengikut
[dasar ini](dasar.md).

Terdapat istilah-istilah yang tidak lazim atau keliru, dan
perlu diterjemah sendiri semasa mengusahakan projek ini.
Lihat [senarai istilah](glosari.md).

laman kembali: [utama][0]

  [0]: ../index.md
