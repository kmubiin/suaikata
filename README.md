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

## Pemerian teks dan aturan

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

Semua laman sedia dipapar menggunakan penyunting teks, atau
pelayar web bersama add-ons, yang ada sokongan Markdown.
Elemen asas seperti perenggan, senarai berturutan, dan
pautan boleh dipapar seperti sepatutnya.

Beberapa elemen tambahan seperti nota kaki dan senarai
definisi bergantung pada pemproses kramdown. Bagaimanapun,
kedua-duanya digunakan secara terhad dan masih dapat dipapar
tanpa kramdown, sebagai pautan dan perenggan biasa.

Penjana laman Jekyll menggunakan pemproses kramdown yang
menyokong elemen asas dan elemen tambahan. Jika Jekyll
digunakan untuk menjana laman, maka semua laman dapat
dipapar pada pelayar web secara lalai.
