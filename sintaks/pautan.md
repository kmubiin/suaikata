Uji pautan untuk GitHub pages
=============================

Diberi laman utama: `tree/gh-pages/tinjau/index.md`

GitHub Pages memaparkan laman ini di alamat yang diluluskan
(tertera sebagai OK) oleh Jekyll seperti berikut:

* `{url}/tinjau/` - OK (ada tanda `/` di hujung)
* `{url}/tinjau` - ERROR
* `{url}/tinjau/index` - OK
* `{url}/tinjau/index.html` - OK
* `{url}/tinjau/index.md` - ERROR

Diberi laman sampingan: `tree/gh-pages/tinjau/lagi.md`

GitHub Pages memaparkan laman ini di alamat yang diluluskan
(tertera sebagai OK) oleh Jekyll seperti berikut:

* `{url}/tinjau/lagi` - OK
* `{url}/tinjau/lagi/` - ERROR
* `{url}/tinjau/lagi.html` - OK
* `{url}/tinjau/lagi.md` - ERROR

Perbandingan sumber dan alamat untuk melayari laman utama
dan laman sampingan direktori:

| laman utama               | laman sampingan           |
| ------------------------- | ------------------------- |
| `{src}/tinjau/index.md`   | `{src}/tinjau/lagi.md`    |
| `{url}/tinjau/`           | tiada                     |
| `{url}/tinjau/index`      | `{url}/tinjau/lagi`       |
| `{url}/tinjau/index.html` | `{url}/tinjau/lagi.html`  |

Petunjuk:

* `{url}` merujuk pada alamat yang diberikan oleh GitHub
melalui tetapan laman projek, yakni:
`http://kmubiin.github.io/suaikata`
* 'ERROR' menandakan alamat yang tidak sah.
* `{src}` merujuk pada alamat fail sumber di GitHub
* `{url}` merujuk pada alamat fail hasil di GitHub Pages

Nota penggunaan:

* Laman utama harus dinamakan `index.md`
* Laman utama ada tanda `/` di hujung alamat bersih, yakni
alamat tanpa nama penuh fail, untuk mewakili folder
* Laman sampingan tidak berakhir dengan tanda tersebut
* Kedua-dua laman utama dan laman sampingan boleh dilayari
di alamat penuh, yakni alamat yang berakhir dengan `.html`

---

Salinan terpilih daripada dahan `gh-pages` untuk percubaan (kini dipadam)
