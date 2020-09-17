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
: kandungan {{ site.data }}

{% if site.data.terbit %}
{% for t in site.data.terbit reversed %}

site.data.terbit
: bilangan {{ site.data.terbit.size}}
: terakhir tag {{ t.tag }} commit {{ t.id }} ({{ t.dev }})

{% break %}
{% endfor %}
{% endif %}

site.pages
: bilangan {{ site.pages.size }}

site.html_pages
: subset site.pages
: bilangan {{ site.html_pages.size }}

site.static_files
: bilangan {{ site.static_files.size }}
: kandungan {{ site.static_files }}

site.html_files
: subset site.static_files
: bilangan {{ site.html_files.size }}
: kandungan {{ site.html_files }}

site.posts
: bilangan {{ site.posts.size }}

site.related_posts
: bilangan {{ site.related_posts.size }}

site.collections
: bilangan {{ site.collections.size }}
: kandungan {{ site.collections }}

site.documents
: subset site.collections
: bilangan {{ site.documents.size }}

