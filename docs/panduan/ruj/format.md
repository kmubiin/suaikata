---
published: true
---

### Format helai daftar

&nbsp;  
Helai daftar disimpan sebagai fail pada komputer supaya
boleh dibaca semula kemudian. Fail tersebut boleh disimpan
dalam dua bentuk:

1. Format asal
2. Format mudah alih

Perbezaan dua format tersebut adalah **lebih maklumat**.
Format asal mengandungi maklumat lengkap seperti rumus,
warna dan lebar sel untuk memapar seluruh kandungan pada
keadaan asal. Sebaliknya, format mudah alih mengandungi
teks biasa dan pemisah teks sahaja.

&nbsp;  
**Format asal**: Apabila menyimpan fail baharu, perisian
komputer akan menyarankan format asal seperti XLS dan ODS.
Microsoft Office menggunakan XLS, atau XLSX sejak 2007,
manakala LibreOffice menggunakan ODS.

Kandungan format asal yang dibaca oleh perisian komputer
biasanya dipapar dalam helaian rebak yang terdiri daripada
lajur berabjad dan baris bernombor.

|     |`A`         | `B`             |
|:---:| ---------- | --------------- |
| `1` | inggeris   | melayu          |
| `2` | vocabulary | kosa kata       |
| `3` |            | cuba, satu, dua |

&nbsp;  
**Format mudah alih**: Apabila menggunakan beberapa perisian
yang berbeza, fail tersebut sewajarnya disimpan dalam format
mudah alih seperti CSV dan TSV. Perisian web seperti Google
Sheets dan GitHub turut menyokong format mudah alih.

Kandungan format mudah alih adalah lebih ringkas berbanding
format asal, dan dipapar mengikut pilihan pengguna bagi
perisian web atau perisian komputer yang digunakan.

Misalnya, pemapar fail di GitHub akan memaparkan CSV
sebagai jadual ala helaian rebak. Nombor baris mungkin
ditunjukkan di ruang paling kiri, bergantung pada ciri
pemapar fail yang disediakan.

|     |            |                 |
|:---:| ---------- | --------------- |
| `1` | inggeris   | melayu          |
| `2` | vocabulary | kosa kata       |
| `3` |            | cuba, satu, dua |

Dalam misal lain, penyunting teks biasa dan garis perintah
akan memaparkan CSV baris demi baris yang mengandungi
sebarang teks biasa dan pemisah teks.

Pilihan format mudah alih antara CSV dan TSV adalah mengikut
kehendak pengguna. CSV mungkin lebih biasa dipilih.
Bagaimanapun, TSV kelihatan lebih baik kerana ruang lebar
kosong antara teks yang mudah dibaca oleh pengguna dan masih 
mudah dipapar seperti CSV menggunakan perisian yang berbeza.

&nbsp;  
**CSV (Comma-separated values)** biasanya menggunakan aksara
tanda koma `,` sebagai pemisah teks. Bergantung pada bahasa
pengguna yang ditetapkan pada komputer, aksara lain mungkin
juga digunakan sebagai pemisah teks.

    inggeris,melayu
    vocabulary,kosa kata
    ,"cuba, satu, dua"

Jika tanda koma turut digunakan dalam mana-mana sel, maka
perisian akan menambah tanda petik dua `" "` meliputi
seluruh kandungan sel itu. Tanda petik ini tersembunyi
apabila dipapar dalam helaian rebak dan sebaliknya terdedah
apabila dipapar dalam penyunting teks biasa.

Kandungan fail CSV boleh menjadi rumit apabila melibatkan
teks yang mengandungi tanda koma atau tanda petik tambahan.
Tanda-tanda itu harus dielakkan bagi CSV, dan sekiranya
masih rumit, gunakan TSV.

&nbsp;  
**TSV (Tab-separated values)** menggunakan aksara kekunci
`<TAB>` bagi menggantikan aksara tanda koma `,` sebagai
pemisah teks. Berbeza dengan CSV, tanda koma tambahan dalam
sel tidak perlukan tanda petik dua lagi.

    inggeris<TAB>melayu
    vocabulary<TAB>kosa kata
    <TAB>cuba, satu, dua

Dalam paparan sebenar, aksara `<TAB>` hanyalah ruang lebar
kosong antara teks dan mana-mana sel yang dibiar kosong
boleh kelihatan janggal dan tidak tersusun. Oleh itu, TSV
sewajarnya digunakan untuk menyimpan teks yang sama panjang
bagi satu-satu lajur.

Format mudah alih hanya mengingati isi dan rupa ringkas
kandungan. Ciri ini menjadikan CSV dan TSV lebih mudah
dibaca dan disunting menggunakan perisian yang berbeza.

&nbsp;  
laman lompat kembali: [nama][1]

laman kembali: [panduan][0]

  [0]: ../index.md
  [1]: ../bab/nama.md
