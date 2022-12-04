Senarai daftar kata yang rasmi:

{% comment %}
kod berikut sengaja ditulis rapat sedemikian supaya hasil
tukaran ke kod HTML lebih kemas, mungkin ralat pada Liquid
{% endcomment %}

{% assign d = site.data.daftar %}

<ul>{% for sa in d %}{% if sa.rasmi %}
<li>"{{ sa.alt }}"{% capture n %}{% increment i %}{% endcapture %}
oleh {{ sa.oleh.ahli | join: ", " }}</li>
{% endif %}{% endfor %}</ul>

Bilangan daftar rasmi/semua:
{{ n | plus: 1 }}/{{ d | size }}
