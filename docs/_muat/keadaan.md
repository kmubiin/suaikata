{{ '---' }}
Keadaan projek pada masa ini:

{% assign d = site.data.daftar %}
{% assign t = site.data.terbit %}

- Bilangan daftar: {{ d | size }}
- Tarikh terakhir daftar: (nyahaktif sementara)
- Tarikh terakhir terbit: (nyahaktif sementara)

{% if site.url == 'https://kmubiin.github.io/suaikata' %}
Laman dalam talian bertarikh {{ site.time }}
{% else %}
Laman luar talian atau alamat telah berubah
{% endif %}
