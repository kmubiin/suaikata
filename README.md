# suaikata
Koleksi ringkas kosa kata

Bermula Jun 2024, laman dalam talian dinyahaktif dengan
sengaja dan secara lalai. Cara menerbit laman menggunakan
Pages kini menggunakan Actions, yang lebih rumit. Tumpuan
diberi bagi menjana laman di luar talian sahaja.

## Pemerian sumber

[daftar](daftar) -- sumber daftar kata  
[docs](docs) -- sumber laman dan kandungan  
&emsp;../_baca -- yang berasas  
&emsp;[../../kandungan.md](docs/baca/kandungan.md) --
yang tersedia  
&emsp;../_data -- yang berurus  
&emsp;../_muat -- yang muat bila perlu  
&emsp;../_usul -- yang bersejarah  
&emsp;../bersuai.md -- yang disedia guna templat  
&emsp;../_config.yml -- tetapan laman  
&emsp;[../index.md](docs/index.md) -- laman utama  
`index.md` -- fail rujukan di luar talian  
`LICENSE` -- fail salinan lesen projek ini  
`README.md` -- fail asal (laman ini)  

## Pemerian teks dan aturan

Kebanyakan kandungan dalam projek ini disedia dan disimpan
sebagai teks biasa. Bagaimanapun, teks biasa boleh memiliki
ciri yang berlainan berdasarkan mana-mana aturan berikut:

- Markdown--bahasa penanda bagi menyedia kandungan dan juga
  format fail bagi semua laman pra-HTML
- Liquid--bahasa templat bagi memapar data sendiri dan
  memuat kandungan secara memilih
- YAML--format fail bagi tetapan laman, bahagian awal laman
  dan tambahan data sendiri
- CSV--format fail bagi daftar ada makna
- TSV--format fail bagi daftar tanpa makna

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
