---
---

### Penamat baris

Apabila menyunting fail di platform tertentu, teks biasa
mungkin menggunakan **penamat baris yang berbeza**. Senarai
platform umum dan penamat baris yang digunakan adalah
seperti berikut:

- Unix: LF (`\n`)
- Mac: CR (`\r`)
- DOS/Windows: CR LF (`\r \n`)

Teks biasa dengan mana-mana penamat baris boleh dibaca
seperti biasa menggunakan aplikasi lazim. Namun begitu,
aplikasi atau laman dalam talian adakalanya tidak menyokong
kesemua penamat baris. Misalnya di GitHub, jumlah sumbangan
yang terpapar di laman dipengaruhi oleh penamat baris.

Bandingkan sumbangan pertama (0bda916) dan kedua (5c4032d)
bagi fail katakerap.csv seperti berikut:

    $ git log --oneline | grep -A3 'Muatnaik'
    5c4032d Muatnaik 4000 perkataan Inggeris paling biasa
    747de60 Delete katakerap.csv
    0bda916 Add files via upload
    7447ef1 ...

    $ git diff --shortstat 7447ef1 0bda916
     1 file changed, 23020 insertions(+)

    $ git diff --shortstat 0bda916 5c4032d
     1 file changed, 1 insertion(+), 23020 deletions(-)

Bandingkan kiraan baris bagi fail contoh dan fail asal
daripada sumbangan berkenaan:

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

Teks biasa 'ASCII text' dianggap menggunakan penamat baris
LF walaupun tidak tercatat. Teks biasa bersama baris
penamat CR didapati menunjukkan bilangan baris yang salah
(0) berbanding penamat baris CRLF yang menunjukkan
bilangan baris yang betul (23020).

Sebaiknya gunakan penamat baris LF atau CR LF.

laman kembali: [panduan][0]

  [0]: ../index.md
