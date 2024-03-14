{{ '---' }}

{% comment %}
ruang ini akan memapar senarai data daftar dan laman secara
terhad atau memilih; buat masa ini, senarai data dipapar
secara menyeluruh apabila laman dijana di localhost sahaja

kod liquid dari `baca/index.md` untuk memapar senarai daftar
akan dipindah salin ke sini (cadangan sementara)
{% endcomment %}

{% assign u = site.url | truncate: 16, "" %}
{% if u == 'http://localhost' %}
{% include termuat.md %}
{% else %}
Laman dalam talian bertarikh {{ site.time }}
{% endif %}
