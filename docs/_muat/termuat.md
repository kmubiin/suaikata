{{ '---' }}
Laman termuat berada di {{ page.name }}

{% comment %}
laman termuat adalah laman khas untuk menyelidik kandungan
yang boleh dicapai dengan anu terbina bagi Jekyll
{% endcomment %}

site.repository
: {{ site.repository }}

site.url
: {{ site.url }}

site.time
: {{ site.time }}

site.timezone
: {{ site.timezone }}

site.data ({{ site.data.size }})
: kandungan data seperti berikut

{% comment %}
site.data adalah JSON dan Liquid tiada cara `Object.keys()`
sepertimana JavaScript; gunakan gelung `for d in site.data`
{% endcomment %}

{% if site.data.size > 0 %}
{% for d in site.data %}
{% if d[1].size > 2 %}
site.data.{{ d[0] }} ({{ d[1].size }})
: terakhir {{ d[1].last }}
{% else %}
site.data.{{ d[0] }}
: terhad {{ d[1] | default: '(tiada data)' }}
{% endif %}
{% endfor %}
{% endif %}

{% assign o = site.pages %}{% if o.size > 0 %}
site.pages ({{ o.size }}) {% for f in o %}
: {{ f.layout }}&emsp;{{ f.url }}{% endfor %}
{% endif %}

{% comment %}
site.static_files adalah longgokan data terbina Jekyll;
gunakan gelung `for f in site.static_files`
{% endcomment %}

{% assign o = site.static_files %}{% if o.size > 0 %}
site.static&#95;files ({{ o.size }}) {% for f in o %}
: {{ f.extname }}&emsp;{{ f.path }}{% endfor %}
{% endif %}

{% assign o = site.posts %}{% if o.size > 0 %}
site.posts ({{ o.size }}) {% for f in o %}
: {{ f.layout }}&emsp;{{ f.url }}{% endfor %}
{% endif %}

{% comment %}
site.collections.size ialah `1` meskipun array kosong `[]`;
senarai fail tanpa bahagian awal di `f.files` dan sebaliknya
di `f.docs`, kecuali `published: false` tidak tersenarai
{% endcomment %}

{% if site.documents.size > 0 %}
{% assign o = site.collections %}
site.collections ({{ o.size }}) {% for f in o %}
: {{ f.label }} {{ f.docs.size }} {{ f.files.size }}{% endfor %}

{% assign o = site.documents %}
site.documents ({{ o.size }}) {% for f in o %}
: {{ f.collection }}&emsp;{{ f.url | default: false }}{% endfor %}
{% endif %}
