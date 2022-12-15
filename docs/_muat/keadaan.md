{{ '---' }}
Keadaan projek pada masa ini:

> Kandungan laman sedang disemak semula pada masa ini.
> Kecuali laman utama, kebanyakan kandungan laman akan
> disalin dan disusun semula dalam masa terdekat.
> -- Nota bertarikh 15 Dis 2022 (Khamis)

{% comment %}
ruang ini akan memapar senarai tarikh terakhir yang lebih
menyeluruh--senarai baru akan dijana berdasarkan fail-fail
data yang dicipta semula baru-baru ini
{% endcomment %}

{% assign u = site.url | truncate: 16, "" %}
{% if u == 'http://localhost' %}
{% include termuat.md %}
{% else %}
Laman dalam talian bertarikh {{ site.time }}
{% endif %}
