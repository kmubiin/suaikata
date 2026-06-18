---
published: true
title: Soal format helai
rak: panduan
bab: 3
jilid: 3.6
---

### Soal format helai

Panduan ini adalah berdasarkan perubahan dari semasa ke
semasa dan berkaitan dengan isu tercipta yang bertajuk
"Pengendalian data" (13 Mac 2018)[^1] dan "Kemudahan
capaian data" (14 Mac 2018)[^2].

Helai daftar harus disimpan sebagai fail pada komputer
untuk salinan sendiri dan boleh dipapar semula secara bebas.
Secara umum, fail boleh disimpan dalam dua format:

1. Format asal
2. Format mudah alih

Format asal mengandungi teks biasa dan pelengkap teks
seperti warna teks, rumus pengiraan dan rujukan sel, panjang
dan lebar sel, dan lain-lain. Format mudah alih pula
mengandungi teks biasa dan pemisah teks sahaja.

Perbezaan dua format tersebut adalah lebih maklumat. Bagi
memapar semula helai daftar pada keadaan asal, pengguna
perlu menyimpan fail dalam format asal.

Apabila menyimpan fail baharu, perisian komputer akan
menyarankan format asal seperti XLS dan ODS. Secara lalai,
Microsoft Office menggunakan XLS, atau XLSX sejak 2007,
manakala LibreOffice menggunakan ODS.

Gambaran daftar pada perisian komputer:

    .------------.---.-----------------.
    |   |     A      |        B        :
    |---|------------|-----------------.
    | 1 | inggeris   | melayu          :
    |---|------------|-----------------.
    | 2 | vocabulary | kosa kata       :
    |---|------------|-----------------.
    | 3 |            | cuba, satu, dua :
    | . | . . . . . .| . . . . . . . . .

Fail dalam format asal biasanya dipapar pada helaian rebak
atau hamparan elektronik. Setiap muka pada helaian itu
terdiri daripada lajur berabjad dan baris bernombor. Ruang
di atas lajur berabjad menunjukkan koordinat dan kandungan
sel yang sedang dipilih.

Walaupun fail dalam format asal dapat menyimpan helai daftar
pada keadaan asal, namun fail itu tidak mesti dapat dipapar
menggunakan perisian yang berbeza. Fail itu mungkin perlu
dimuat dan disimpan semula dalam format mudah alih.

Gambaran daftar pada pemapar fail atau perisian lain:

    ....................................
    : 1 : inggeris   : melayu          :
    :   :............:.................:
    : 2 : vocabulary : kosa kata       :
    :   :............:.................:
    : 3 :            : cuba, satu, dua :
    :...:............:.................:

Fail dalam format mudah alih dapat dipapar terus pada
pemapar fail atau perisian yang berbeza. Misalnya, GitHub
ada kemudahan memapar data[^3] secara langsung bagi fail
yang dimuat dalam format mudah alih. Ruang di paling kiri
menunjukkan nombor baris, jika berkenaan.

Dalam misal lain, penyunting teks biasa atau garis perintah
akan memapar baris demi baris bagi fail yang sama. Setiap
baris itu mengandungi sebarang teks biasa dan pemisah teks
sahaja, yang mungkin dipapar secara berjarak.

Gambaran daftar yang dipapar dengan garis perintah:

    $ column -t -s ',' daftar.csv 
    inggeris    melayu            
    vocabulary  kosa kata         
                "cuba       satu   dua"

Helai daftar yang disimpan dengan format mudah alih hanya
mengingati isi dan rupa ringkas kandungan. Format mudah alih
ada dua pilihan lazim:

1. CSV (Comma-separated values)[^4]
2. TSV (Tab-separated values)[^5]

Kandungan fail CSV:

    inggeris,melayu
    vocabulary,kosa kata
    ,"cuba, satu, dua"

Fail CSV biasanya menggunakan aksara tanda koma `,` sebagai
pemisah teks. Bergantung pada bahasa pengguna yang
ditetapkan pada komputer, aksara selain tanda koma mungkin
digunakan sebagai pemisah teks.

Jika tanda koma turut digunakan dalam mana-mana sel, maka
perisian akan menambah tanda petik dua `" "` meliputi
seluruh kandungan sel itu. Tanda petik ini tersembunyi
apabila dipapar pada helaian rebak dan sebaliknya terdedah
apabila dipapar pada penyunting teks biasa.

CSV boleh menjadi rumit apabila melibatkan teks yang ada
tanda koma atau tanda petik tambahan. Tanda-tanda itu harus
dielakkan bagi CSV, dan sekiranya masih rumit, gunakan TSV.

Kandungan fail TSV:

    inggeris<TAB>melayu
    vocabulary<TAB>kosa kata
    <TAB>cuba, satu, dua

Fail TSV menggunakan aksara kekunci `<TAB>` bagi
menggantikan aksara tanda koma `,` sebagai pemisah teks.
Berbeza dengan CSV, tanda koma tambahan dalam sel tidak
perlukan tanda petik dua lagi.

Dalam paparan sebenar, aksara `<TAB>` hanyalah jarak lebar
antara teks dan mana-mana sel yang dibiar kosong boleh
kelihatan janggal dan tidak tersusun. Oleh itu, TSV
sewajarnya digunakan untuk menyimpan teks yang sama panjang
bagi satu-satu lajur.

Pilihan format mudah alih antara CSV dan TSV adalah mengikut
kehendak pengguna. CSV mungkin lebih biasa dipilih.
Bagaimanapun, TSV kelihatan lebih baik kerana ruang kosong
antara teks yang mudah dibaca oleh pengguna dan masih
mudah dipapar menggunakan perisian yang berbeza.

{% assign tajuk = "kembali ke kandungan (bersuai)" %}  
[{{ tajuk }}](../..{% link bersuai.md %}){% comment %}
&brvbar; [../kandungan.md](../kandungan.md){% endcomment %}

{% comment %}
Semua rujukan di bawah hanya mengandungi pautan ke sumber
asal menggunakan sintaksis nota kaki bagi Kramdown. Jika
nota kaki tidak muncul, maka pautan mutlak akan muncul
pada teks yang dirujuk dalam mana-mana perenggan di atas.
{% endcomment %}

[^1]: https://github.com/kmubiin/suaikata/issues/5
[^2]: https://github.com/kmubiin/suaikata/issues/6
[^3]: https://help.github.com/articles/rendering-csv-and-tsv-data/
[^4]: https://tools.ietf.org/html/rfc4180
[^5]: https://www.iana.org/assignments/media-types/text/tab-separated-values
