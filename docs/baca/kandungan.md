{% comment %}
Laman ini tidak ditambah bahagian awal dengan sengaja.
Kandungan laman ini boleh dimuat secara tidak langsung di
laman bersuai menggunakan kod Liquid `include_relative`.
{% endcomment %}

{% comment %}
Perihal laman ini:
. kod pautan yang akan dijana adalah sah apabila dimuat di
  suatu laman yang sama aras dengan index
. kod pautan relatif adalah sah dan sedia dicapai apabila
  dipapar oleh penyunting teks Markdown
. semua kod pautan relatif disertakan sebagai komen dan
  tidak akan muncul apabila laman dijana.
{% endcomment %}

Daftar kata boleh didapati di laman sumber dan tidak dipapar
terus di laman ini. Sebaliknya, laman ini menyediakan
bahan bacaan dan rujukan projek.

Laman berikut disediakan untuk bacaan umum.

- [{{ "Hasil kajian Mac 2018" }}](.{% link baca/ura/1803.md %}){% comment %}
&brvbar; [ura/1803.md](ura/1803.md){% endcomment %}
- [{{ "Hasil kajian April 2020" }}](.{% link baca/ura/2004.md %}){% comment %}
&brvbar; [ura/2004.md](ura/2004.md){% endcomment %}

Laman berikut disediakan untuk panduan projek.

{% comment %}
**Bab 1: Satu permulaan** menerangkan asal usul projek
suaikata dan pengetahuan umum yang berkaitan. Bab ini juga
menyusun semula hasil perbincangan bagi menyedia takrif
semasa menyiapkan daftar pertama.
{% endcomment %}

#### Bab 1: Satu permulaan

11. [{{ "Mengenal projek suaikata" }}](.{% link baca/bab/kenal.md %}){% comment %}
&brvbar; [bab/kenal.md](bab/kenal.md){% endcomment %}
12. [{{ "Sumber kata masukan" }}](.{% link baca/bab/sumber.md %}){% comment %} &brvbar; [bab/sumber.md](bab/sumber.md){% endcomment %}
13. [{{ "Hak cipta tidak terpelihara" }}](.{% link baca/bab/hak-cipta.md %}){% comment %} &brvbar; [bab/hak-cipta.md](bab/hak-cipta.md){% endcomment %}
14. [{{ "Lesen sumber terbuka" }}](.{% link baca/bab/lesen.md %}){% comment %} &brvbar; [bab/lesen.md](bab/lesen.md){% endcomment %}
15. [{{ "Asas penyediaan takrif" }}](.{% link baca/bab/asas.md %}){% comment %} &brvbar; [bab/asas.md](bab/asas.md){% endcomment %}
16. [{{ "Takrif asal dan terjemah" }}](.{% link baca/bab/takrif.md %}){% comment %} &brvbar; [bab/takrif.md](bab/takrif.md){% endcomment %}

{% comment %}
**Bab 2: Perihal daftar** menerangkan ciri daftar dan helai
daftar. Bab ini juga menerangkan cara simpan helai yang
sesuai supaya dapat dibaca semula kemudian.
{% endcomment %}

#### Bab 2: Perihal daftar

21. [{{ "Bentuk lazim daftar" }}](.{% link baca/bab/lazim.md %}){% comment %} &brvbar; [bab/lazim.md](bab/lazim.md){% endcomment %}
22. [{{ "Kelainan ciri daftar" }}](.{% link baca/bab/lain.md %}){% comment %} &brvbar; [bab/lain.md](bab/lain.md){% endcomment %}
23. [{{ "Mencipta helai daftar" }}](.{% link baca/bab/helai.md %}){% comment %} &brvbar; [bab/helai.md](bab/helai.md){% endcomment %}
24. [{{ "Dua atau lebih lajur" }}](.{% link baca/bab/lajur.md %}){% comment %} &brvbar; [bab/lajur.md](bab/lajur.md){% endcomment %}
25. [{{ "Penamat baris" }}](.{% link baca/bab/baris.md %}){% comment %} &brvbar; [bab/baris.md](bab/baris.md){% endcomment %}
26. [{{ "Menyimpan helai dengan nama" }}](.{% link baca/bab/nama.md %}){% comment %} &brvbar; [bab/nama.md](bab/nama.md){% endcomment %}

{% comment %}
**Bab 3: Aturan kerja** menerangkan semula cara menyedia dan
memuat daftar ke laman sumber dan usaha lain yang boleh
dilakukan selepas itu.
{% endcomment %}

#### Bab 3: Aturan kerja

31. [{{ "Menyedia daftar sendiri" }}](.{% link baca/bab/sedia.md %}){% comment %} &brvbar; [bab/sedia.md](bab/sedia.md){% endcomment %}
32. [{{ "Memuat daftar" }}](.{% link baca/bab/muat.md %}){% comment %} &brvbar; [bab/muat.md](bab/muat.md){% endcomment %}
33. [{{ "Menyelenggara daftar" }}](.{% link baca/bab/selenggara.md %}){% comment %} &brvbar; [bab/selenggara.md](bab/selenggara.md){% endcomment %}
34. [{{ "Soal terjemah" }}](.{% link baca/bab/terjemah.md %}){% comment %} &brvbar; [bab/terjemah.md](bab/terjemah.md){% endcomment %}
35. Tajuk ini akan diperbaharu (bab 3, jilid 3.5)
36. [{{ "Soal format helai" }}](.{% link baca/bab/format.md %}){% comment %} &brvbar; [bab/format.md](bab/format.md){% endcomment %}

[{{ "Dasar panduan" }}](.{% link baca/dasar.md %}){% comment %} &brvbar; [dasar.md](dasar.md){% endcomment %}
ada senarai rujukan untuk semua
bab di atas, tetapi telah dipindah salin ke setiap bab.
Oleh itu, laman dasar akan dimansuh kelak.

[{{ "Laman salinan" }}](.{% link baca/salinan.md %}){% comment %} &brvbar; [salinan.md](salinan.md){% endcomment %}
ada senarai salinan terhad
daftar, tetapi bakal dipindah salin ke data daftar dengan
reka bentuk baharu.
Oleh itu, laman salinan akan dimansuh kelak.

{% comment %}
Apabila salinan terhad daftar dipindah salin ke data daftar,
salinan itu dapat dijana di mana-mana laman menggunakan kod
Liquid. Kebaikan cara ini adalah salinan terhad daftar
dapat diurus tanpa perlu menyunting laman satu demi satu.
Keburukan cara ini adalah salinan terhad daftar tidak dapat
dipapar terus seperti kod Markdown, dan bergantung pada
penjana laman untuk melihat salinan data itu.
{% endcomment %}

Terdapat istilah-istilah yang tidak lazim atau keliru, dan
perlu diterjemah sendiri semasa mengusahakan projek ini.
Lihat [{{ "senarai istilah" }}](.{% link baca/glosari.md %}){% comment %} &brvbar; [glosari.md](glosari.md){% endcomment %}.

{% comment %} kembali ke laman utama
&brvbar; [../index.md](../index.md)  
atau kembali ke laman dimuat (bersuai)
&brvbar; [../bersuai.md](../bersuai.md){% endcomment %}
