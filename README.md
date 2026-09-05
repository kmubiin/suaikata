# suaikata
Koleksi ringkas kosa kata

Bermula Jun 2024, laman dalam talian dinyahaktif dengan
sengaja dan secara lalai. Cara menerbit laman menggunakan
Pages kini menggunakan Actions, yang lebih rumit. Tumpuan
diberi bagi menjana laman di luar talian sahaja.

## Pemerian sumber

[daftar](daftar) -- sumber daftar kata  
[docs](docs) -- sumber laman dan kandungan  
&emsp;../baca -- yang berasas  
&emsp;[../baca/kandungan.md](docs/baca/kandungan.md) --
yang tersedia \#  
&emsp;../_data -- yang berurus  
&emsp;../_muat -- yang muat bila perlu \#  
&emsp;../_usul -- yang bersejarah  
&emsp;../bersuai.md -- yang disedia guna templat \#  
&emsp;../_config.yml -- tetapan laman  
&emsp;[../index.md](docs/index.md) -- laman utama  
`index.md` -- fail rujukan di luar talian  
`LICENSE` -- fail salinan lesen projek ini  
`README.md` -- fail asal (laman ini)  

\# akan disemak semula dan pasti dipermudah

## Pemerian format

Kebanyakan kandungan dalam projek ini disedia dan disimpan
sebagai teks biasa, dengan mana-mana format berikut.

1. Markdown atau `.md`--format bagi semua kandungan yang
   sedia dibaca dan boleh dijana semula menjadi laman HTML.

2. YAML atau `.yml`--format bagi tetapan laman, bahagian
   awal laman dan data sendiri, yang guna pasangan teks
   seperti `anu: nilai`.

3. CSV atau `.csv`--format bagi daftar ada makna, yang guna
   aksara tanda koma sebagai pemisah teks.

4. TSV atau `.tsv`--format bagi daftar tanpa makna, yang
   guna aksara jarak lebar atau kekunci `<TAB>` bagi
   menggantikan aksara koma sebagai pemisah teks.

Penyunting teks boleh membaca semua kandungan teks tanpa
membezakan mana-mana format. Bagaimanapun, perisian yang
lebih khusus harus digunakan untuk memapar secara betul.

## Kelainan bahasa dan aturan

Markdown yang terpakai bagi sumber ini adalah yang diperluas
dan khusus untuk penjana laman Jekyll. Markdown ini
merangkumi ciri-ciri yang lazim berserta yang diperluas
dengan ciri tambahan seperti jadual dan nota kaki.

Penjana laman Jekyll adalah perisian banyak-dalam-satu yang
digunakan untuk membangunkan sumber ini. Jekyll terdiri
daripada bahagian seperti:

- pemproses penanda kramdown untuk menjana semula kandungan
  teks dalam fail Markdown menjadi laman HTML;

- bahasa templat Liquid untuk menyokong kod sampingan dalam
  fail Markdown untuk memuat data melalui YAML dan memuat
  kandungan secara memilih;

- sebilangan besar perisian kecil berasaskan Ruby untuk
  mengenal pasti bahagian awal laman, dan menggabungkan
  kandungan dan gaya laman.

Sekalipun tidak menggunakan Jekyll, ciri tambahan seperti
senarai definisi dan nota kaki masih dapat dipapar secara
lalai sebagai perenggan dan pautan biasa.

Penjana laman adalah cara lazim untuk menukarkan Markdown
menjadi HTML untuk menyedia laman web. Bagi pengguna umum,
pelayar web bersama add-ons adalah cara yang lebih ringkas
untuk memapar Markdown secara langsung.
