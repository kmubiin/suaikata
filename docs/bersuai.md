---
published: true
---

### Kandungan (bersuai)

Kemas kini setakat [{{ site.time }}](termuat.md)

Projek suaikata mempunyai pendekatan tersendiri bagi
mengusahakan daftar kata. Suatu daftar kata harus bermula
dengan senarai tanpa makna.

&emsp;[Lihat panduan](panduan/index.md)

Hakikatnya, bukan semua perkataan dalam bahasa asal dapat
diterjemah begitu sahaja. Di luar daftar kata, projek
suaikata ada senarai istilah yang terhad.

&emsp;[Lihat glosari](glosari.md)

Sebelum daftar pertama diusahakan, projek suaikata telah
membuat kajian rinci. Hasil kajian terawal ialah Mac 2018.

&emsp;[Mac 2018](ura/1803.md)
&emsp;[April 2020](ura/2004.md)

Berikut adalah senarai daftar kata yang diusahakan secara
rasmi oleh projek suaikata.

{% assign d = site.data.daftar %}
<ul>{% for sa in d %}{% if sa.ciri.rasmi %}
<li>"{{ sa.nama.c }}"
oleh {{ sa.para.pengusaha | join: ", " }}</li>
{% endif %}{% endfor %}</ul>

{% comment %}
Kod Liquid di atas sengaja ditulis rapat sedemikian supaya
hasil tukaran ke kod HTML adalah lebih baik. Sama ada
kebolehan terhad atau keadaan ralat pada Liquid.
{% endcomment %}

> Kajian daftar telah disalin semula sebagai data dan boleh
> dipapar melalui `site.data.daftar`, kecuali paparan sedang
> diuji pada masa ini

laman kembali: [utama][0]

  [0]: index.md

