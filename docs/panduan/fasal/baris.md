---
---

### Penggunaan baris

Apabila pengguna menyunting fail di platform yang berbeza,
teks biasa mungkin disimpan dengan baris penamat yang
berbeza.

> Dalam pengkomputan, teks biasa (Bahasa Inggeris: Plain
> text) ialah kandungan fail berjujukan biasa yang dapat
> dibaca sebagai bahan teks tanpa banyak pemprosesan,
> berbanding dengan teks berformat dan fail perduaan
>
> Sumber: [Teks biasa di Wikipedia Bahasa Melayu][a]

Baris penamat berserta penggunaan di platform umum adalah
seperti berikut:

| Baris penamat | Platform    |
| ------------- | ----------- |
| LF            | Unix        |
| CR            | Mac         |
| CRLF (EOL)    | DOS/Windows |

Kebanyakan pengguna akan mendapati teks biasa dengan
mana-mana baris penamat boleh dibaca seperti biasa
menggunakan aplikasi lazim. Namun begitu, aplikasi atau
laman dalam talian adakalanya tidak menyokong kesemua
baris penamat.

Misalnya di GitHub, para pengguna harus menyedari bahawa
pilihan baris penamat dalam teks biasa akan mempengaruhi
jumlah sumbangan (contributions) yang dipaparkan di laman,
yakni bilangan baris yang diubah dalam teks biasa.

Sumbangan pertama:

> Add files via upload
>
> 1 parent `7447ef1` commit
`0bda916e5f03ec82696939ed507483bb4ba85c4f`
>
> [...] Showing with 23,020 additions and 0 deletions.

Sumbangan kedua:

> Muatnaik 4000 perkataan Inggeris paling biasa
>
> 1 parent `747de60` commit
`5c4032de829ed5e2cde2214f59b0fea83345c326`
>
> [...] Showing with 1 addition and 0 deletions.
>
> 3 commits 23,021 ++ 23,020 --

Lihat perbezaan kiraan baris terhadap teks biasa bersama
baris penamat yang berbeza, yang dilakukan melalui garis
perintah `file` dan `wc` di GNU/Linux seperti berikut.

    $ file *.csv
    contoh.csv:                 ASCII text
    katakerap-baru-5c4032d.csv: ASCII text, with CR line
     terminators
    katakerap-lama-0bda916.csv: ASCII text, with CRLF line
     terminators

    $ wc *.csv
         6     10    143 contoh.csv
         0  40179 441155 katakerap-baru-5c4032d.csv
     23020  40179 553304 katakerap-lama-0bda916.csv
     23026  80368 994602 total

Teks biasa 'ASCII text' dianggap menggunakan baris penamat
LF walaupun tidak ditunjukkan. Teks biasa bersama baris
penamat CR didapati menunjukkan bilangan baris yang salah
(0) berbanding baris penamat CRLF yang menunjukkan
bilangan baris yang betul (23020).

Maka, baris penamat **LF** atau **CRLF** harus digunakan.

Laman ini adalah berdasarkan teks daripada komen dalam
[isu #17][b] di GitHub Issues, kecuali sebahagian teks telah
disemak dan ditulis semula untuk penjelasan.

  [a]: https://ms.wikipedia.org/wiki/Teks_biasa
  [b]: https://github.com/kmubiin/suaikata/issues/17
