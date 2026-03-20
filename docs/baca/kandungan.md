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

- [Hasil kajian Mac 2018][1803] {% comment %}
&brvbar; [ura/1803.md](ura/1803.md){% endcomment %}
- [Hasil kajian April 2020][2004] {% comment %}
&brvbar; [ura/2004.md](ura/2004.md){% endcomment %}

[1803]: .{% link baca/ura/1803.md %}  
[2004]: .{% link baca/ura/2004.md %}  

Laman berikut disediakan untuk panduan projek.

{% comment %}
**Bab 1: Satu permulaan** menerangkan asal usul projek
suaikata dan pengetahuan umum yang berkaitan. Bab ini juga
menyusun semula hasil perbincangan bagi menyedia takrif
semasa menyiapkan daftar pertama.
{% endcomment %}

#### Bab 1: Satu permulaan

1. [Mengenal projek suaikata][11] {% comment %}
&brvbar; [bab/kenal.md](bab/kenal.md){% endcomment %}
2. [Sumber kata masukan][12] {% comment %}
&brvbar; [bab/sumber.md](bab/sumber.md){% endcomment %}
3. [Hak cipta tidak terpelihara][13] {% comment %}
&brvbar; [bab/hak-cipta.md](bab/hak-cipta.md){% endcomment %}
4. [Lesen sumber terbuka][14] {% comment %}
&brvbar; [bab/lesen.md](bab/lesen.md){% endcomment %}
5. [Asas penyediaan takrif][15] {% comment %}
&brvbar; [bab/asas.md](bab/asas.md){% endcomment %}
6. [Takrif asal dan terjemah][16] {% comment %}
&brvbar; [bab/takrif.md](bab/takrif.md){% endcomment %}

[11]: .{% link baca/bab/kenal.md %}  
[12]: .{% link baca/bab/sumber.md %}  
[13]: .{% link baca/bab/hak-cipta.md %}  
[14]: .{% link baca/bab/lesen.md %}  
[15]: .{% link baca/bab/asas.md %}  
[16]: .{% link baca/bab/takrif.md %}  

{% comment %}
**Bab 2: Perihal daftar** menerangkan ciri daftar dan helai
daftar. Bab ini juga menerangkan cara simpan helai yang
sesuai supaya dapat dibaca semula kemudian.
{% endcomment %}

#### Bab 2: Perihal daftar

1. [Bentuk lazim daftar][21] {% comment %}
&brvbar; [bab/lazim.md](bab/lazim.md){% endcomment %}
2. [Kelainan ciri daftar][22] {% comment %}
&brvbar; [bab/lain.md](bab/lain.md){% endcomment %}
3. [Mencipta helai daftar][23] {% comment %}
&brvbar; [bab/helai.md](bab/helai.md){% endcomment %}
4. [Dua atau lebih lajur][24] {% comment %}
&brvbar; [bab/lajur.md](bab/lajur.md){% endcomment %}
5. [Penamat baris][25] {% comment %}
&brvbar; [bab/baris.md](bab/baris.md){% endcomment %}
6. [Menyimpan helai dengan nama][26] {% comment %}
&brvbar; [bab/nama.md](bab/nama.md){% endcomment %}

[21]: .{% link baca/bab/lazim.md %}  
[22]: .{% link baca/bab/lain.md %}  
[23]: .{% link baca/bab/helai.md %}  
[24]: .{% link baca/bab/lajur.md %}  
[25]: .{% link baca/bab/baris.md %}  
[26]: .{% link baca/bab/nama.md %}  

{% comment %}
**Bab 3: Aturan kerja** menerangkan semula cara menyedia dan
memuat daftar ke laman sumber dan usaha lain yang boleh
dilakukan selepas itu.
{% endcomment %}

#### Bab 3: Aturan kerja

1. [Menyedia daftar sendiri][31] {% comment %}
&brvbar; [bab/sedia.md](bab/sedia.md){% endcomment %}
2. [Memuat daftar][32] {% comment %}
&brvbar; [bab/muat.md](bab/muat.md){% endcomment %}
3. [Menyelenggara daftar][33] {% comment %}
&brvbar; [bab/selenggara.md](bab/selenggara.md){% endcomment %}
4. [Soal terjemah][34] {% comment %}
&brvbar; [bab/terjemah.md](bab/terjemah.md){% endcomment %}
5. Tajuk ini akan diperbaharu (bab 3, jilid 3.5)
6. [Soal format helai][36] {% comment %}
&brvbar; [bab/format.md](bab/format.md){% endcomment %}

[31]: .{% link baca/bab/sedia.md %}  
[32]: .{% link baca/bab/muat.md %}  
[33]: .{% link baca/bab/selenggara.md %}  
[34]: .{% link baca/bab/terjemah.md %}  
[35]: #  
[36]: .{% link baca/bab/format.md %}  

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
