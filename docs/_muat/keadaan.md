{{ '---' }}
Keadaan projek pada masa ini:

{% assign d = site.data.daftar %}
{% assign dt = d.last.bila %}
{% assign t = site.data.terbit %}

- Bilangan daftar: {{ d | size }}
- Tarikh terakhir daftar: {{ dt.last.c }}
- Tarikh terakhir terbit: {{ t.last.bila }}

{% assign u = site.url | truncate: 16, "" %}
{% if u == 'http://localhost' %}
{% include termuat.md %}
{% else %}
Laman dalam talian bertarikh {{ site.time }}
{% endif %}
