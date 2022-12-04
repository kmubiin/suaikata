{{ '---' }}
Keadaan projek pada masa ini:

{% assign d = site.data.daftar %}
{% assign t = site.data.terbit %}

- Bilangan daftar: {{ d | size }}
- Tarikh terakhir daftar: {{ d.last.bila }}
- Tarikh terakhir terbit: {{ t.last.bila }}

{% assign u = site.url | truncate: 16, "" %}
{% if u == 'http://localhost' %}
{% include termuat.md %}
{% else %}
Laman dalam talian bertarikh {{ site.time }}
{% endif %}
