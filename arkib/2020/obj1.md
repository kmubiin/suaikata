---
date: 2020-08-08
title: Objek gunaan pertama di laman Jekyll
---

### Objek gunaan pertama di laman Jekyll

Di sini, objek gunaan merangkumi dua jenis objek:

1. Objek YAML di bahagian awal laman Jekyll, dan;
2. Objek Liquid di bahagian badan laman Jekyll.

Maklumat berkaitan laman seperti tajuk (title) dan kategori
(category) dapat disimpan menggunakan objek YAML dan dapat
dipapar semula menggunakan objek Liquid.

Bagi objek gunaan pertama, suatu laman yang ditanda dengan
kategori "cuba" hendak dipapar di laman lain. Ada beberapa
prasyarat yang dikenal pasti seperti berikut.

- Pastikan tetapan Jekyll ada alamat laman yang sah;

  ```
    # tetapan Jekyll di _config.yml
    url: https://kmubiin.github.io/suaikata
    permalink: /:title:output_ext
  ```

- Satu objek YAML `category:` mesti ada di bahagian awal
suatu laman;

  ```
    ---
    category: cuba
    ---
  ```

  Jika suatu laman itu tidak diberi tajuk atau mahu diberi
  tajuk lain, tambah satu lagi objek YAML `title:` juga.

  ```
    ---
    title: satu
    category: cuba
    ---
  ```

- Satu objek Liquid mesti ada di bahagian badan laman lain
bersama kod Markdown atau HTML bagi senarai pautan;

  Markdown list:

  ```
    {% for post in site.categories.cuba %}
    - [{{ post.title }}]({{ site.url }}{{ post.url }})
    {% endfor %}
  ```

  HTML list:

  ```
    <ul>
    {% for post in site.categories.cuba %}
    <li>
    <a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
    </ul>
  ```

- Sebarang laman yang ditanda di bahagian awal laman mesti
disimpan dengan nama `YYYY-MM-DD-tajuk.md` dalam folder
`_posts` supaya dapat dikenal pasti oleh Jekyll.

  ```
    _posts/2020-08-08-dua.md
    _posts/2020-08-08-satu.md
  ```

Dengan memenuhi kesemua prasyarat di atas, objek Liquid
bersama kod Markdown tadi akan bertukar menjadi kod HTML
dengan pautan yang betul seperti berikut.

```
  <ul>
    <li>
      <p><a href="https://kmubiin.github.io/suaikata/satu.html">satu</a></p>
    </li>
    <li>
      <p><a href="https://kmubiin.github.io/suaikata/dua.html">dua</a></p>
    </li>
  </ul>
```

Apabila menggunakan objek Liquid bersama kod Markdown,
pasangan tag pautan `<a>...</a>` akan diliputi oleh tag
perenggan `<p>...</p>`. Tag perenggan ini tidak ditambah
apabila menggunakan objek Liquid bersama kod HTML.

- [satu](https://kmubiin.github.io/suaikata/satu.html)
- [dua](https://kmubiin.github.io/suaikata/dua.html)

Hasil paparan adalah senarai pautan ke laman yang ditanda
dengan kategori "cuba". Senarai pautan adalah sah pada masa
cubaan dan hanya sekadar contoh pada masa lain. Selain jarak
antara dua baris, hasil paparan adalah sama.

Objek gunaan boleh digunakan untuk memapar senarai laman
yang ditanda dengan suatu kategori. Namun, hanya laman
bertarikh (post) yang berada dalam `_posts` akan dipapar
dan laman umum (page) yang berada di luar diabai.

&nbsp;  
laman kembali: [arkib][0]

  [0]: ../index.md
