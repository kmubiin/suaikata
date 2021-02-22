{{ '---' }}
Laman termuat berada di `{{ page.name }}`

{% comment %}
Laman termuat adalah laman khas untuk menyelidik kandungan
yang boleh dicapai dengan anu terbina bagi Jekyll.
{% endcomment %}

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
kandungan data hadir sebagai longgokan data JSON,
bagaimanapun Liquid tiada cara `Object.keys()` sepertimana
JavaScript untuk pulangkan senarai ringkas data JSON;
gunakan gelung `for d in site.data` untuk memapar data
{% endcomment %}

{% if site.data.size > 0 %}
{% for d in site.data %}
{% if d[1].size > 2 %}
site.data.{{ d[0] }}
: bilangan {{ d[1].size }}
: terakhir {{ d[1].last }}
{% else %}
site.data.{{ d[0] }}
: tunggal {{ d[1] | default: '(tiada data)' }}
{% endif %}
{% endfor %}
{% endif %}

site.pages
: bilangan {{ site.pages.size }}
: bilangan html {{ site.html_pages.size | default: 0 }}
{% if site.pages.size > 0 %}: senarai url
{% for f in site.pages %}{{ f.url }}, {% endfor %}
{% endif %}

{% comment %}
kandungan `site.static_files` hadir sebagai longgokan data
terbina Jekyll; gunakan `for f in site.static_files` dan
capai objek `f` dengan `f.path`, `f.modified_time`,
`f.name`, `f.basename`, `f.extname` bagi metadata fail
{% endcomment %}

site.static_files
: bilangan {{ site.static_files.size }}
: bilangan html {{ site.html_files.size | default: 0 }}
{% if site.static_files.size > 0 %}: senarai fail
{% for f in site.static_files %}{{ f.path }}, {% endfor %}
{% endif %}

site.posts
: bilangan {{ site.posts.size }}
{% if site.posts.size > 0 %}: senarai url
{% for f in site.posts %}{{ f.url }}, {% endfor %}
{% endif %}

{% comment %}
nilai bagi site.collections.size ialah `1` meskipun
kandungan adalah array kosong `[]`, maka uji subset yang
sedia ada `site.documents.size > 0` untuk pasti
{% endcomment %}

{% if site.documents.size > 0 %}
site.collections
: bilangan {{ site.collections.size }}
: senarai label
{% for f in site.collections %}{{ f.label }}, {% endfor %}

site.documents
: subset site.collections
: bilangan {{ site.documents.size }}
: senarai url
{% for f in site.documents %}{{ f.url }}, {% endfor %}
{% endif %}
