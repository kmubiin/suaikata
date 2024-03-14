{{ '---' }}

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
