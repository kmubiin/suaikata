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
ada, untuk pulangkan senarai ringkas data JSON. Gunakan
`for data in site.data` untuk memapar data. Capai objek
`data[0]` untuk senarai ringkas data, dan objek `data[1]`
untuk kandungan data selebihnya.
{% endcomment %}

{% if site.data.size > 0 %}
{% for data in site.data %}

  {% if data[0] == "terbit" %}
  {% assign t = data[1].last %}

  site.data.{{ data[0] }}
  : bilangan {{ data[1].size }}
  : terakhir tag {{ t.tag }} commit {{ t.id }} ({{ t.dev }})

  {% elsif data[1].size > 2 %}

  site.data.{{ data[0] }}
  : bilangan {{ data[1].size }}

  {% else %}

  site.data.{{ data[0] }}
  : {{ data[1] }}

  {% endif %}

{% endfor %}
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

  {{ file.path }}
  : {{ file.modified_time }} {{ file.name }}

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

--------- **sempadan kod cubaan bermula** ---------

Longgok site.data:

{{ site.data }}

Cuba longgok string menjadi array
seperti `assign s = "foo, bar" | split: ", "`

{% assign s = "foo, bar" | split: ", " %}
{% if s %}
output size sort:
{{ s }} {{ s | size }} {{ s | sort }}
{% else %}
s tidak berhasil
{% endif %}

Cuba longgok objek tanpa tanda petik
seperti `assign o = {'c','a','b'}`

{% assign o = {'c','a','b'} %}
{% if o %}
output size sort:
{{ o }} {{ o | size }} {{ o | sort }}
{% else %}
o tidak berhasil
{% endif %}

Cuba longgok senarai objek sebagai string menjadi array
seperti `assign so = "{'foo'=>'x'},{'bar'=>nil}" | split: ","`

{% assign so = "{'foo'=>'x'},{'bar'=>nil}" | split: "," %}
{% if so %}
output size sort:
{{ so }} {{ so | size }} {{ so | sort }}
{% else %}
so tidak berhasil
{% endif %}

Cuba longgok data menjadi senarai objek sebagai string
seperti `assign b = site.data.b | join: ";;"` dan pastikan
aksara pilihan bagi split dan join tidak diguna dalam string
tersebut. Boleh cuba dengan satu atau dua aksara.

{% if site.data.b %}
input size:
{{ site.data.b }} {{ site.data.b | size }}
{% else %}
site.data.b tidak ada
{% endif %}

{% assign b = site.data.b | join: ";;" %}
{% if b %}
output string size:
{{ b }} {{ b | size }}
{% else %}
b tidak berhasil
{% endif %}

Seterusnya longgok senarai objek b menjadi array
seperti `assign ba = b | split: ";;"` dan harus guna aksara
selain aksara yang diguna dalam senarai objek tersebut.

{% assign ba = b | split: ";;" %}
{% if ba %}
output array size:
{{ ba }} {{ ba | size }}

output array sort:
{{ ba | sort }}
{% else %}
ba tidak berhasil
{% endif %}

Akhirnya array ba boleh dipapar seperti site.data.b, beza
antara dua data tersebut adalah ba disusun terlebih dahulu.

output for site.data.b:

{% for a1 in site.data.b %}
{{ a1 }} {{ a1 | size }}
{% endfor %}

output for ba:

{% for a2 in ba %}
{{ a2 }} {{ a2 | size }}
{% endfor %}

Atau papar terus dengan index array:

output index `site.data.b[0]`: {{ site.data.b[0] }}  
output index `ba[0]`: {{ ba[0] }}

output index `site.data.b[1]`: {{ site.data.b[1] }}  
output index `ba[1]`: {{ ba[1] }}
