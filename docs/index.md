---
layout: default
---

Projek suaikata ialah projek perkamusan sumber terbuka yang
dimulakan oleh dua orang penutur bahasa Melayu pada 2018.
Satu tahun kemudian, daftar kata pertama menjadi lengkap.

&#8889; **Daftar kata** &#8889;  
Bukan kamus harian. Projek ini mengusahakan daftar kata dan
membawakan takrif terpilih atau sekadar memadai.

&#9740; **CC-BY-4.0** &#9740;  
Syarat "sebut nama". Daftar kata itu boleh digunakan secara
bebas dengan syarat menyatakan perakuan hak cipta asal.

Termuat pada masa ini:

> Bahagian ini akan memuat senarai pautan ke kandungan
> terpilih atau terkini, sama ada dengan bantuan Jekyll atau
> secara manual--perlu selidik #beta

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

<ul>
  {% for post in site.categories.cuba %}
    <li>
      <a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

> Cuba papar objek Liquid di atas?

&nbsp;  
Maklumat lanjut:

&sect; **Hasil pena**
&ndash; Projek suaikata menyediakan terbitan tanpa rutin,
serta lema dan daftar dalam bahasa asal dan bahasa Melayu.
[Lihat bersuai](bersuai.md)

&sect; **Perkakasan**
&ndash; Projek suaikata dapat mengusahakan daftar kata
dengan adanya sumber dan perisian yang memainkan peranan.
[Lihat berbantu](berbantu.md)

&sect; **Cara kerja**
&ndash; Projek suaikata mempunyai pendekatan tersendiri bagi
mengusahakan daftar kata.
[Lihat panduan](panduan/index.md)

&nbsp;  
Untuk kemudahan lain, sila layari laman sumber di GitHub.
