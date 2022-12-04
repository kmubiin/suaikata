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
: kandungan data seperti berikut<br><br>

{% comment %}
site.data mengandungi objek JSON;
JavaScript ada `Object.keys()` untuk memapar JSON, tetapi
Liquid tiada cara itu; gunakan gelung `for d in site.data`
{% endcomment %}

{% assign o = site.data | sort %}
{% if o.size > 0 %}{% for d in o %}
site.data.{{ d[0] }} ({{ d[1].size | default: 0 }})
: {% if d[1].last.id %}{% for sa in d[1] %}{{ sa.id }}, {% endfor %}
{% else %}objek tiada 'id'{% endif %}

{% if d[1].last %}terakhir {{ d[1].last | default: 'tiada' }}
{% else %}pangkal {{ d[1] | default: 'tiada' }}{% endif %}
{% endfor %}{% endif %}

{% assign o = site.static_files %}
<br>{% if o.size > 0 %}
site.static&#95;files ({{ o.size }}) {% for f in o %}
: {{ f.extname }}&emsp;{{ f.path }}{% endfor %}
{% endif %}

{% assign o = site.pages %}
<br>{% if o.size > 0 %}
site.pages ({{ o.size }}) {% for f in o %}
: {{ f.layout }}&emsp;{{ f.url }}{% endfor %}
{% endif %}

{% comment %}
site.pages mengandungi sebarang fail yang ada bahagian awal,
tetapi tersimpan di luar folder "posts" dan "collections"
{% endcomment %}

{% assign o = site.posts %}
<br>site.posts ({{ o.size }}) {% if o.size > 0 %}{% for f in o %}
: {{ f.layout }}&emsp;{{ f.url }}{% endfor %}{% else %}
: tiada{% endif %}

{% assign o = site.collections %}
<br>site.collections ({{ o.size }}) {% for f in o %}
: {{ f.label }} {{ f.files.size }} terbit: {{ f.docs.size }}{% endfor %}

{% assign o = site.documents %}
<br>{% if o.size > 0 %}
site.documents ({{ o.size }}) {% for f in o %}{% if f.url %}
: {{ f.collection }}&emsp;{{ f.url }}{% endif %}{% endfor %}{% endif %}

{% comment %}
site.documents mengandungi semua fail yang disimpan dalam
folder "posts" dan "collections";
`f.files` adalah senarai fail tanpa bahagian awal;
`f.docs` adalah senarai fail ada bahagian awal, kecuali
fail tidak tersenarai dengan `published: false`;
{% endcomment %}

Termuat tamat.
