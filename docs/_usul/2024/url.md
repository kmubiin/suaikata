---
published: false
date: 2024-03-22
title: Kod pautan sah URL
---

### Kod pautan sah URL

Usul ini adalah berdasarkan isu tercipta yang ditanda
label "pepijat" dan yang bertajuk "Pengaruh kod untuk
menjana pautan yang sah" (22 Mac 2024)[^1]. Isu ini telah
diselesai pada 14 Disember 2025.

Di sini, "pautan yang sah" adalah sama ada pautan mutlak
atau pautan relatif yang boleh menghubungkan suatu laman
dengan laman yang lain. Pautan yang sah harus tidak
memapar 404 (page not found) atau ralat seumpamanya.

{% comment %}
Usul ini belum selesai ditulis #todo
{% endcomment %}

[^1]: https://github.com/kmubiin/suaikata/issues/48

----

Tampal dan salin daripada isu yang dipetik:

Isu ini dicipta untuk melaporkan kelainan pautan yang dijana menggunakan kod Liquid. Ada dua cara yang dikenal pasti untuk menjana pautan, iaitu:

[1] menjana pautan dengan kod Liquid (rujuk [Variables](https://jekyllrb.com/docs/variables/)) dan HTML:

    <a href="{{ site.url }}{{ page.url }}">tajuk</a>

[2] menjana pautan dengan kod Liquid [a] (rujuk [Linking to pages](https://jekyllrb.com/docs/liquid/tags/#link)) dan Markdown:

    [tajuk]({% link alamat/asal/fail.md %})

Kedua-dua cara tersebut boleh menjana pautan di laman yang dijana, kecuali salah satu cara tersebut mungkin memapar pautan yang tidak laku di localhost. Perbezaan ini tidak dapat dikenal pasti apabila menggunakan pelayar web "fungsi penuh" seperti Firefox dan Chrome.

- Mengikut cara [1], kod Liquid `{{ site.url }}` akan memapar alamat samaran `http://localhost:4000`. Alamat ini tidak semestinya disokong oleh pelayar web dan mungkin juga tidak dibenar melayari alamat sedemikian mengikut tetapan pelayar web atau sistem operasi.

- Mengikut cara [2], kod Liquid `{% link ... %}` akan memapar alamat IP `http://127.0.0.1:4000` bagi localhost. Alamat IP seharusnya disokong oleh semua pelayar web dan dapat dilayari secara langsung.
 
- Berbeza dengan cara [1], tag link bagi cara [2] perlu dinyatakan alamat asal ke fail Markdown (.md) supaya boleh ditukarkan ke alamat kekal laman (.html) apabila laman dibina.

Bagaimanapun, berdasarkan laman rujukan yang kedua ([Linking to pages](https://jekyllrb.com/docs/liquid/tags/#link)), terdapat nota di bawah tajuk bahagian laman:

> Since Jekyll `4.0` , you don’t need to prepend `link` and `post_url` tags with `site.baseurl`.

Umm, maksudnya... kod Liquid `{{ site.url }}` adalah tidak tepat dan sebaliknya `{{ site.baseurl }}` harus digunakan untuk menjana pautan yang setara dengan `{% link ... %}`--dan ya, ini telah diuji serta-merta di localhost dan disahkan benar!

~Kesimpulannya, laman bersuai (`docs/bersuai.md`) sewajarnya menggunakan cara [2] untuk menjana pautan bagi senarai laman.~ Kod Liquid adalah lebih ringkas dan mudah, dan juga tidak perlu bercampur aduk dengan kod HTML.

Aduhai, sekarang baru ingat balik kenapa tak guna kod Liquid sejak mula dulu... sebab GitHub Pages masih guna Jekyll 3.X [b], jadi kod Liquid tidak menjana pautan yang sah (`link` tag masih perlukan `site.baseurl` di hadapan alamat fail laman).

~Mungkin~ Ternyata boleh guna cara lain seperti ini [3] (telah diuji):

    [tajuk]({{ site.baseurl }}{{ page.url }})
    [tajuk](.{{ page.url }})

Kedua-dua kod di atas adalah setara, apabila diuji di localhost dan di GitHub Pages.

Perlu diingatkan bahawa kod Liquid juga bergantung pada tetapan laman `_config.yml`, dan nilai yang diisi pada `site.url` dan `site.baseurl` [c]. Tetapi jika alamat penuh laman terus diganti pada `site.url`, maka `site.baseurl` tidak diperlukan? Mungkin lebih baik diasingkan supaya ada pilihan untuk menjana alamat relatif berdasarkan `site.baseurl` sahaja.

Terbitan yang terjejas: semasa (semua terbitan sejak 0d38487 dan `2.22.1222`)

---

[a] Barangkali kod Liquid `{% ... %}` dan `{{ ... }}` tidak boleh bersarang (nested) dalam mana-mana satu dengan yang lain; selepas diuji semula dengan teliti, laman gagal dibina di localhost juga--mungkin ujian sebelum ini buat sambil
 lewa, jadi terlepas pandang.

[b] Rujuk ~[laman versi ini](https://pages.github.com/versions/)~ laman hilang--yang tersenarai adalah `Jekyll 3.9.5` setakat `2024-04-06 12pm +0000` (dinyatakan di hujung laman). [Laman versi ringkas JSON](https://pages.github.com/versions.json) ada menyenarai jekyll versi "3.10.0" setakat 2025-09-23 hari ini.

[c] Kedua-dua `url` dan `baseurl` dinyatakan secara lalai apabila laman dibina di GitHub Pages, sekalipun tidak diaktifkan di `_config.yml`. Jadi, tetapan bagi projek suaikata harus dinyahaktif dengan tanda pagar `#` sebagai komen yang boleh dirujuk semula.

---

Lagi pengesahan:

- "pautan" dalam isu ini boleh merujuk pada pautan mutlak atau pautan relatif
- "pautan yang sah" adalah sama ada pautan mutlak atau pautan relatif yang boleh menghubungkan suatu laman dengan laman yang lain seperti sepatutnya; tidak memapar 404 (page not found) atau ralat seumpamanya
- pautan mutlak ialah pautan lengkap dan kekal, yang mana pautan itu memapar pautan yang sama dan serupa apabila laman diterbit;
- pautan mutlak juga dikenal dengan istilah teknologi maklumat "permalink"
- pautan relatif ialah pautan separa lengkap, yang mana pautan itu memapar pautan yang sama tetapi boleh berbeza mengikut alamat asal laman yang diterbit
- kedua-dua pautan mutlak dan pautan relatif boleh memapar pautan yang setara, dengan cara masing-masing
- cara [3] yang dikemukakan di atas adalah kegunaan laman bersuai, untuk menjana senarai laman bersama pautan yang sah secara auto

Lagi rancangan (selain laman bersuai):

- kebanyakan laman di `baca/*` menyediakan "laman kembali" ke kandungan menggunakan Markdown;
- menjana pautan dengan Markdown adalah hampir sama dengan cara [3], kecuali tajuk dan alamat laman yang dituju dinyatakan secara langsung (tanpa kod Liquid)
- walau bagaimanapun, menjana pautan dengan Markdown bergantung pada Jekyll dan Jekyll Relative Link plugin untuk memapar pautan yang sah, pada masa nyata (tidak kekal)
- sepatutnya pautan relatif yang sah harus dipapar di pelayar web, menggunakan kod Liquid dan Markdown (hampir sama dengan cara [3]), apabila laman dijana dan diterbit;
- manakala pautan relatif yang asal harus dipapar dengan penyunting teks atau pemapar Markdown sahaja;
- jadi, pindah salin yang asal (.md) sebagai komen kod Liquid dan sediakan pautan yang sah (.html) menggunakan kod markdown mengikut cara [3] seperti ini:

      {% comment %}
      [tajuk](alamat/relatif/asal.md)
      {% endcomment %}
      [tajuk](./alamat/relatif/sah.html)

- atau, komen kod Liquid yang sama tetapi pautan yang sah (.html) mengikut cara [2] seperti ini:

      {% comment %}
      [tajuk](alamat/relatif/asal.md)
      {% endcomment %}
      [tajuk](.{% link alamat/relatif/asal.md %})

- aksara titik satu `.` adalah setara dengan `{{ site.baseurl }}` apabila laman dijana dalam talian; bagaimanapun, `baseurl` tidak memberi sebarang nilai apabila laman dijana di localhost dan boleh menjadi punca pautan tidak sah.
 
---

Tugasan dalam isu ini:

- [x] gantikan baris `url: ...` dengan `#url: ...` dan `#baseurl: ...` di `_config.yml`
- [x] gantikan kod Liquid dan HTML (seperti cara [1]) dengan kod Liquid dan Markdown (salah satu daripada cara lain [3] dan *bukan* cara [2]) di `bersuai.md`
- [x] bina dan uji laman `bersuai.md` di localhost dan di GitHub Pages (8bda83a)
- [x] perbaik "laman kembali" di semua laman `baca/*` menggunakan kod Liquid dan Markdown untuk dua keadaan sekaligus (lihat "lagi rancangan" di atas)
- [x] bina dan uji laman-laman lain yang berkenaan di localhost ~dan di GitHub Pages~
- [ ] simpan semula isu ini sebagai dokumen usul di `_usul/2024/url.md` untuk rujukan
