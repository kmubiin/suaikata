---
---

### Format asal dan mudah alih

Helai daftar disimpan sebagai fail dalam bentuk tertentu
supaya boleh dibaca semula kemudian. Fail tersebut boleh
disimpan dalam dua bentuk:

1. Format asal
2. Format mudah alih

Apabila menyimpan fail baharu, perisian komputer akan
menyarankan format asal seperti XLS dan ODS. Perisian
komputer seperti Microsoft Office menggunakan format asal
XLS, atau XLSX sejak 2007, manakala LibreOffice menggunakan
format asal ODS.

Jika fail perlu dibaca semula menggunakan perisian lain,
maka fail tersebut hendaklah disimpan dalam format mudah
alih seperti CSV. Perisian web seperti Google Sheets dan
GitHub turut menyokong format mudah alih CSV.

Perbezaan dua format ini adalah **kelengkapan maklumat**.
Format asal mengandungi maklumat lengkap seperti rumus,
warna dan lebar sel untuk memapar seluruh kandungan pada
keadaan asal. Sebaliknya, format mudah alih mengandungi
teks biasa bersama pemisah teks sahaja.

Misalnya, pemapar fail di GitHub akan memaparkan CSV
sebagai jadual ala helaian rebak. Nombor baris mungkin
ditunjukkan di ruang paling kiri, bergantung pada ciri
pemapar fail yang disediakan.

|     |            |                 |
|:---:| ---------- | --------------- |
| `1` | inggeris   | melayu          |
| `2` | vocabulary | kosa kata       |
| `3` |            | cuba, satu, dua |

Dalam misal lain, penyunting teks biasa di GitHub atau
penyunting teks biasa di komputer akan memaparkan CSV baris
demi baris yang mengandungi sebarang teks biasa dan
pemisah teks. Tanda koma `,` biasanya digunakan sebagai
pemisah teks.

    inggeris,melayu
    vocabulary,kosa kata
    ,"cuba, satu, dua"

Jika tanda koma turut digunakan dalam mana-mana sel, maka
perisian akan menambah tanda petik dua `" "` meliputi
seluruh kandungan sel itu. Tanda petik ini tersembunyi
apabila dibaca oleh perisian helaian rebak dan terdedah
apabila dibaca oleh penyunting teks biasa.

CSV (Comma-separated values) boleh menjadi rumit apabila
melibatkan teks yang mengandungi tanda koma atau tanda petik
tambahan. Tanda-tanda itu harus dielakkan dalam CSV, dan
sekiranya masih rumit, gunakan TSV (Tab-separated values).

    inggeris<TAB>melayu
    vocabulary<TAB>kosa kata
    <TAB>cuba, satu, dua

Apabila menggunakan TSV, aksara kekunci `<TAB>` akan
menggantikan tanda koma `,` dan tanda koma tambahan dalam
sel tidak perlukan tanda petik dua. Dalam paparan sebenar,
aksara `<TAB>` hanyalah ruang lebar kosong antara teks dan
mana-mana sel yang dibiar kosong boleh kelihatan janggal dan
tidak tersusun seperti paparan helaian rebak.

Secara umum, format mudah alih hanya mengingati
**isi kandungan** dan **rupa ringkas kandungan**. Ciri ini
menjadikan CSV dan TSV lebih mudah dibaca semula dan
disunting menggunakan perisian yang berbeza.

laman kembali: [panduan][0]

  [0]: ../index.md
