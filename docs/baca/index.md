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
[salinan terhad daftar](salinan.md).

#### Senarai ura

Laman berikut disediakan untuk bacaan umum.

- [Hasil kajian Mac 2018](ura/1803.md)
- [Hasil kajian April 2020](ura/2004.md)

#### Senarai bab

Laman berikut disediakan untuk panduan projek.

##### Bab 1: Satu permulaan

11. [Mengenal projek suaikata](bab/kenal.md)
12. [Sumber kata masukan](bab/sumber.md)
13. [Hak cipta tidak terpelihara](bab/hak-cipta.md)
14. [Lesen sumber terbuka](bab/lesen.md)
15. [Asas penyediaan takrif](bab/asas.md)
16. [Takrif asal dan terjemah](bab/takrif.md)

##### Bab 2: Perihal daftar

21. [Bentuk lazim daftar](bab/lazim.md)
22. [Kelainan ciri daftar](bab/lain.md)
23. [Mencipta helai daftar](bab/helai.md)
24. [Dua atau lebih lajur](bab/lajur.md)
25. [Penamat baris](bab/baris.md)
26. [Menyimpan helai dengan nama](bab/nama.md)
27. [Format helai daftar](bab/format.md)

##### Bab 3: Aturan kerja

31. [Menyedia daftar sendiri](bab/sedia.md)
32. [Memuat daftar](bab/muat.md)
33. [Mengulang kaji](bab/ulang-kaji.md)
34. [Soal terjemah](bab/terjemah.md)
35. [Soal piawai](bab/piawai.md)

Semua laman dalam senarai bab di atas disediakan mengikut
[dasar ini](dasar.md).

Terdapat istilah-istilah yang tidak lazim atau keliru, dan
perlu diterjemah sendiri semasa mengusahakan projek ini.
Lihat [senarai istilah](glosari.md).

laman kembali: [utama][0]

  [0]: ../index.md
