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
: kandungan adalah satu longgokan data JSON
(Liquid tidak ada cara `Object.keys()` untuk pulangkan
senarai mudah data seperti JavaScript)

{% if site.data.terbit %}
{% assign t = site.data.terbit.last %}

site.data.terbit
: bilangan {{ site.data.terbit.size }}
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
: kandungan adalah satu longgokan data object berpagar
(Jekyll ada cara untuk mencapai metadata berikut:
`file.path`, `file.modified_time`, `file.name`,
`file.basename`, `file.extname` bagi anu pilihan `file`)

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

