Senarai daftar kata yang rasmi:

{% comment %}
kod berikut sengaja ditulis rapat sedemikian supaya hasil
tukaran ke kod HTML lebih kemas, mungkin ralat pada Liquid
{% endcomment %}

{% assign d = site.data.daftar %}

<ul>{% for sa in d %}{% if sa.ciri.rasmi %}
<li>"{{ sa.nama.c }}"{% capture n %}{% increment i %}{% endcapture %}
oleh {{ sa.para.pengusaha | join: ", " }}</li>
{% endif %}{% endfor %}</ul>

Bilangan daftar rasmi/semua:
{{ n | plus: 1 }}/{{ d | size }}
