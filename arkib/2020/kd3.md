---
date: 2020-04-08
title: Kajian daftar kata kerap unik
---

### Kajian daftar kata kerap unik (kd3)

&nbsp;  
Daftar kata kerap unik (kerapu) terbitan projek suaikata
ialah daftar dwibahasa Inggeris-Melayu berdasarkan daftar
kata kerap yang disalin semula dengan pembaikan terhad.

Daftar ini adalah sumbangan sukarela.

#### Tentang kata kerap unik

Senarai perkataan bahasa Inggeris paling biasa dan terhad
pada tiga aksara atau kurang berserta terjemahan dalam
bahasa Melayu. Susunan adalah setara dengan yang asal.

Pembaikan daftar kata kerap boleh didapati dari segi *rupa*
terjemahan seperti berikut.

- aksara `~` diganti dengan `-` kerana formula dalam helaian
rebak tidak dapat melakukan padanan yang betul

- aksara noktah `.` di hujung dan tengah baris dibuang

- aksara koma `,` diganti dengan `;` supaya setiap sel tidak
perlukan tanda petik kata&mdash;fail menjadi lebih kecil

- aksara angka berkurung yang tidak seragam diganti dengan
angka latin dan diiringi satu aksara penjarak

- aksara penjarak berlebihan sebelum aksara lain dibuang

- aksara penjarak berlebihan dan berturutan dibuang

Semua analisa awal dan perubahan di atas dilakukan dalam
helaian rebak dan menggunakan rumus sokongan terbina dalam
LibreOffice Calc. Rumus yang digunakan adalah termasuk:
`SUBSTITUTE`, `IF`, `RIGHT`, `CONCATENATE`, `MATCH`, `ROW`,
`TRIM`, `LEN`.

Maklumat lanjut tentang rumus dan hasil bagi daftar kerapu
telah disalin dan disimpan berasingan di arkib (2020-03-10).
Boleh juga dicapai dari sini:

- [Rumus gunaan daftar kerapu](rh3.md)

- [Daftar kerapu ada hasil #N/A](rh3na.md)

#### Tentang binaan daftar

Susunan lajur dan baris bagi daftar kata kerap unik:

| perkataan  | terjemahan | unik    | aksara    |
| ---------- | ---------- | ------- | --------- |
| (lema 1)   | (makna 1)  | (baris) | (panjang) |
| (lema 1)   | (makna 2)  | (baris) | (panjang) |
| (lema 2)   | (makna 1)  | ...     | ...       |

Ada empat lajur, iaitu "perkataan", "terjemahan", "unik",
dan "aksara". Setiap baris boleh memuatkan lema yang sama
berserta makna yang lain daripada baris sebelumnya.

- Lajur "perkataan" dan "terjemahan" adalah sama seperti
daftar asal, yakni daftar kata kerap

- Lajur "unik" menyimpan padanan kedudukan baris dalam
daftar asal bagi pasangan perkataan dan terjemahan yang
tidak berulang

- Lajur "aksara" menyimpan bilangan aksara bagi setiap
perkataan di baris masing-masing, terhad pada 3 aksara
atau kurang sahaja dalam daftar ini

Baris disusun mengikut kekerapan dan setara dengan susunan
yang asal. Bandingan kedudukan baris di lajur "unik" untuk
pengesahan.

#### Tentang hasil daftar

Maklumat kemas kini bagi daftar kata kerap unik:

- Bahasa pengantar: Inggeris-Melayu
- Kelas daftar: umum
- Pengusaha daftar: 1
- Tarikh mula: 2020-03-08
- Tarikh siap: 2020-04-08
- Tarikh lengkap: -

Maklumat perangkaan bagi daftar kata kerap unik:

| Bilangan     | Asal    | Semasa  |
| ------------ | -------:| -------:|
| kata masukan | 23019   | 1258    |
| satu aksara  | -       | 2       |
| dua aksara   | -       | 112     |
| tiga aksara  | -       | 1144    |

Jumlah kata masukan adalah sama dengan hasil tambah satu
aksara, dua aksara, dan tiga aksara di lajur semasa.

Bilangan asal dan semasa bagi daftar ini mengira semua
baris yang ada dalam fail, kecuali tajuk di baris pertama.
Bagaimanapun, bilangan semasa adalah termasuk perkataan
berulang yang mempunyai terjemahan yang berbeza.

&nbsp;  
laman kembali: [arkib][0]

  [0]: ../index.md
