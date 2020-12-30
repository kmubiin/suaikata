{% assign m = site.time %}
{% assign d = site.data.daftar %}
{% assign t = site.data.terbit %}

Keadaan projek pada masa ini:

- Bilangan daftar: `{{ d | size }}`
- Tarikh terakhir daftar: `{{ d.last.tarikh.c }}`
- Tarikh terakhir terbit: `{{ t.last.lagi.last.o }}`
- Tarikh laman: `{{ m }}`
