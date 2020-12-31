### Kod cubaan memapar data terubah

Di sini, kod cubaan merujuk pada objek dan kenyataan Liquid
yang membawa nilai yang tidak tetap semasa membaca data.
Catatan ini telah dibuat apabila selesai menguji paparan
senarai daftar kata di laman bersuai.

Mengikut cara lazim, anu pertama `a` diberi nilai `0`
terlebih dahulu dan diikuti gelung `for` yang ada anu kedua
`b`. Diberi suatu senarai mudah, ahlinya disalin satu per
satu ke `b` manakala bilangan ahli dikira dalam gelung dan
disalin ke `a`.

Berikut adalah perbandingan kod JavaScript, Python, dan
Liquid untuk memapar nilai yang dikira dalam gelung `for`.

#### Kod JavaScript

Mengikut cara JavaScript, gelung `for...of` mempunyai kod
yang paling ringkas untuk memapar senarai mudah. Dua bentuk
lain ialah `for` dan `for...in` yang perlu ada anu tambahan
seperti `i` dan dipapar melalui indeks seperti `b[i]`.

Input dalam fail HTML:

    <script>
    var a=0;
    for (let b of ["satu","dua","tiga"]) {
      console.log(b);
      document.write("b ialah " + b + "<br>");
      a=a+1;
    }
    console.log(a);
    document.write("a ialah " + a + "<br>");
    </script>

Output di konsol pelayar web:

    satu
    dua
    tiga
    3

Output di badan pelayar web:

    b ialah satu
    b ialah dua
    b ialah tiga
    a ialah 3

Hasilnya, `console.log` memapar kedua-dua nilai anu di
konsol pelayar web manakala `document.write` pula memapar
teks bersama nilai tersebut di badan pelayar web.

#### Kod Python

Mengikut cara Python, aturan untuk memapar nilai `b` dan `a`
adalah hampir sama dengan cara JavaScript. Bezanya, kod
Python adalah lebih ringkas.

Input dan output di konsol Python:

    >>> a=0
    >>> for b in ["satu","dua","tiga"]:
    ...   print("b ialah " + b)
    ...   a=a+1
    ... 
    b ialah satu
    b ialah dua
    b ialah tiga
    >>> print("a ialah {}".format(a))
    a ialah 3

Binaan gelung adalah `for...in` mirip JavaScript tetapi
paparan menggunakan cara `for...of` yang tidak memerlukan
anu tambahan. Ternyata kod Python adalah lebih mudah.

Hasilnya adalah sama seperti hasil kod JavaScript.

#### Kod Liquid

Mengikut cara Liquid, aturan untuk memapar nilai `b` dan `a`
adalah sedikit lain berbanding JavaScript dan Python.

Input dalam fail Markdown/HTML:

    {% assign senarai = "satu,dua,tiga" | split: "," %}

    {% for b in senarai %}
    b ialah {{ b }} (x {% increment x %})
    <br>{% endfor %}
    x ialah {{ x }}<br>

    {% for b in senarai %}
    b ialah {{ b }} {% capture a %}{% increment n %}{% endcapture %}
    <br>{% endfor %}
    a ialah {{ a | plus: 1 }}<br>

Senarai mudah `["satu","dua","tiga"]` tidak boleh dicipta
terus oleh Liquid sepertimana JavaScript dan Python.
Sebaliknya, suatu rantaian kata akan disuap pada fungsi
`split` bagi Liquid dan disimpan dalam suatu anu.

Binaan dan paparan gelung adalah `for...in` mirip Python
kecuali ada iringan penamat `endfor` di akhir gelung. Satu
lagi perbezaan adalah anu pertama di baris permulaan tidak
diperlukan kerana ada fungsi terbina bagi Liquid.

Fungsi `increment` bagi Liquid digunakan untuk mengira dan
memapar terus bilangan ahli dalam senarai pada setiap
kitaran gelung. Fungsi ini mengandungi suatu anu yang
menyimpan nilai kiraan yang bermula dari `0` dan bertambah
satu kemudian (lihat `x` dalam gelung `for` pertama).

Output di muka pelayar web:

    b ialah satu (x 0)
    b ialah dua (x 1)
    b ialah tiga (x 2)
    x ialah 3

    b ialah satu
    b ialah dua
    b ialah tiga
    a ialah 3

Merujuk pada gelung `for` pertama dan output pada empat
baris awal: Kitaran pertama memapar nilai asal `0` dan
kitaran ketiga memapar nilai asal `2`. Di luar gelung, yang
dipapar adalah nilai akhir selepas tambah satu iaitu `3`.

Merujuk pada gelung `for` kedua dan output pada empat
baris akhir: Fungsi `capture` bagi Liquid dengan anu pilihan
`a` digunakan untuk menyimpan kiraan yang dibuat oleh fungsi
`increment`. Namun pada kitaran terakhir, `a` hanya ada
nilai asal `2` sebelum tambah satu. Fungsi `plus` bagi
Liquid menjadikan `a` bersamaan nilai asal tambah satu yang
menyamai nilai akhir yang dibawa oleh fungsi `increment`.

Hasilnya, output pada empat baris akhir, adalah sama seperti
hasil kod JavaScript dan juga Python.

&nbsp;  
laman kembali: [arkib][0]

  [0]: ../index.md
