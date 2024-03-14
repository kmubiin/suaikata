{{ '---' }}

{% comment %}
ruang ini akan memapar senarai data daftar dan laman secara
terhad atau memilih; buat masa ini, senarai data dipapar
secara menyeluruh apabila laman dijana di localhost sahaja

kod liquid dari `baca/index.md` untuk memapar senarai daftar
akan dipindah salin ke sini (cadangan sementara)

{% raw %}
<ol>{% for sa in site.data.daftar %}{% if sa.rasmi %}
<li>"{{ sa.alt }}"
oleh {{ sa.oleh.ahli | join: ", " }}</li>
{% endif %}{% endfor %}</ol>
{% endraw %}

Hasil paparan bagi kod di atas (setakat 15 Dis 2022):

1. "kata kerap PSAT" oleh kmubiin, raafsmakmal
2. "kata dua-huruf Melayu" oleh kmubiin
3. "kata dua-huruf Inggeris" oleh kmubiin
{% endcomment %}

{% assign u = site.url | truncate: 16, "" %}
{% if u == 'http://localhost' %}
{% include termuat.md %}
{% else %}
Laman dalam talian bertarikh {{ site.time }}
{% endif %}
