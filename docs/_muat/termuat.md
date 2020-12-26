--- SELIDIK MULA ---

Laman ini adalah laman khas untuk menyelidik kandungan yang
boleh dicapai dengan anu terbina bagi Jekyll.

site.repository
: {{ site.repository }}

site.url
: {{ site.url }}

site.time
: {{ site.time }}

site.timezone
: {{ site.timezone }}

site.data
: bilangan {{ site.data.size }}

{% comment %}
kandungan hadir sebagai longgokan data JSON, bagaimanapun
Liquid tiada cara `Object.keys()` sepertimana JavaScript
ada, untuk pulangkan senarai ringkas data JSON; gunakan
`for d in site.data` untuk memapar data; capai objek `d[0]`
untuk bina senarai ringkas data, dan objek `d[1]` untuk
kandungan data selebihnya
{% endcomment %}

{% if site.data.size > 0 %}
{% for d in site.data %}
{% if d[1].size > 2 %}
site.data.{{ d[0] }}
: bilangan {{ d[1].size }}
: terakhir {{ d[1].last }}
{% else %}
site.data.{{ d[0] }}
: {{ d[1] }}
{% endif %}
{% endfor %}
{% endif %}

site.pages
: bilangan {{ site.pages.size }}
: bilangan html {{ site.html_pages.size }}

site.static_files
: bilangan {{ site.static_files.size }}
: bilangan html {{ site.html_files.size }}

{% comment %}
kandungan `site.static_files` hadir sebagai longgokan data
terbina Jekyll; gunakan `for f in site.static_files` dan
capai objek `f` dengan `f.path`, `f.modified_time`,
`f.name`, `f.basename`, `f.extname` bagi metadata fail
{% endcomment %}

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
--- SELIDIK TAMAT ---
