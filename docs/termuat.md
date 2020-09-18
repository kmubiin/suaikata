---
layout: null
---

Laman ini adalah laman khas untuk menyelidik kandungan yang
boleh dicapai dengan anu terbina bagi Jekyll.

site.url
: {{ site.url }}
: bersumber pada [index.md](index.md)

site.time
: {{ site.time }}

site.timezone
: {{ site.timezone }}

site.data
: bilangan {{ site.data.size }}
: kandungan hadir sebagai longgokan data JSON

{% comment %}
Liquid tiada cara `Object.keys()` sepertimana JavaScript
ada, untuk pulangkan senarai ringkas data JSON. Untuk
mengatasi kekurangan ini, gunakan data berformat YAML dan
pastikan sekurang-kurangnya ada satu anu di aras teratas
sebelum mengisi blok maklumat lain.
{% endcomment %}

{% if site.data.size > 0 %}
{% for data in site.data %}

site.data.{{ data[0] }}
: bilangan {{ data.size }}
: kandungan {{ data | inspect }}

{% endfor %}
{% endif %}

{% if site.data.terbit %}
{% assign t = site.data.terbit.bagi.last %}

site.data.terbit
: bilangan {{ site.data.terbit.bagi.size }}
: terakhir tag {{ t.tag }} commit {{ t.id }} ({{ t.dev }})

{% endif %}

site.pages
: bilangan {{ site.pages.size }}

{% if site.html_pages.size > 0 %}

site.html_pages
: subset site.pages
: bilangan {{ site.html_pages.size }}

{% endif %}

site.static_files
: bilangan {{ site.static_files.size }}
: kandungan hadir sebagai longgokan data terbina Jekyll

{% comment %}
Jekyll ada cara untuk mencapai metadata bagi static files
seperti berikut: `file.path`, `file.modified_time`,
`file.name`, `file.basename`, `file.extname` bagi `file`
atau anu pilihan lain.
{% endcomment %}

{% if site.static_files.size > 0 %}
{% for file in site.static_files %}
  {{ file.modified_time }} {{ file.path }}
{% endfor %}
{% endif %}

{% if site.html_files.size > 0 %}

site.html_files
: subset site.static_files
: bilangan {{ site.html_files.size }}

{% endif %}

site.posts
: bilangan {{ site.posts.size }}

{% if site.related_posts.size > 0 %}

site.related_posts
: subset atau berkaitan site.posts
: bilangan {{ site.related_posts.size }}

{% endif %}

site.collections
: bilangan {{ site.collections.size }}
: kandungan {{ site.collections }}

{% if site.documents.size > 0 %}

site.documents
: subset site.collections
: bilangan {{ site.documents.size }}

{% endif %}

