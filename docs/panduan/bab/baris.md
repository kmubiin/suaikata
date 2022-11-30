---
published: true
tajuk: Penamat baris
bahagian: bab
bab: 2
urutan: 5
---

### Penamat baris

Apabila menyunting fail di platform tertentu, teks biasa
mungkin menggunakan **penamat baris yang berbeza**. Senarai
platform umum dan penamat baris yang digunakan adalah
seperti berikut:

- Unix: `\n` (LF)
- Mac: `\r` (CR)
- DOS/Windows: `\r \n` (CR LF)

Teks biasa dengan mana-mana penamat baris boleh dibaca
seperti biasa menggunakan aplikasi lazim. Namun begitu,
aplikasi atau laman dalam talian adakalanya tidak menyokong
kesemua penamat baris.

Misalnya di GitHub, jumlah sumbangan yang terpapar di laman
dipengaruhi oleh penamat baris. Bandingkan dua sumbangan
berkaitan (0bda916, 5c4032d) dan kiraan baris fail CSV
berkenaan seperti berikut:

    $ git log --oneline | grep -A3 'Muatnaik'
    5c4032d Muatnaik 4000 perkataan Inggeris paling biasa
    747de60 Delete katakerap.csv
    0bda916 Add files via upload
    7447ef1 ...

    $ git diff --shortstat 7447ef1 0bda916
     1 file changed, 23020 insertions(+)

    $ git diff --shortstat 0bda916 5c4032d
     1 file changed, 1 insertion(+), 23020 deletions(-)

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

Fail contoh 'ASCII text' menggunakan penamat baris LF
walaupun tidak dipaparkan. Fail CSV dengan penamat baris
yang berbeza memulangkan kiraan baris seperti berikut:

- LF: 6 (benar)
- CR: 0 (tidak benar)
- CRLF: 23020 (benar)

GitHub dan perisian lain tidak boleh membuat kiraan baris
yang betul bagi fail yang menggunakan penamat baris CR. Oleh
sebab itu, lebih baik gunakan penamat baris LF atau CR LF.

&nbsp;  
laman kembali: [panduan][0]

  [0]: ../index.md
