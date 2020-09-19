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

  {% if data[1].size > 2 %}

  site.data.{{ data[0] }}
  : bilangan {{ data[1].size }}
  : terakhir {{ data[1].last }}

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

Cuba longgok string menjadi array?

{% assign s = "foo, bar" | split: ", " %}

raw code:

{% raw %}
    {% assign s = "foo, bar" | split: ", " %}
{% endraw %}

output size sort:

{% if s %}
    {{ s }} {{ s | size }} {{ s | sort }}
{% else %}
    s tidak berhasil
{% endif %}

Cuba longgok objek tanpa tanda petik?

raw code:

{% raw %}
    {% assign o = {'c','a','b'} %}
{% endraw %}

output:

{% raw %}
    Liquid Warning: Liquid syntax error (line 126):
    Unexpected character { in "{{{'c','a','b'} }}" ...
{% endraw %}

Jadi, ternyata Liquid tidak boleh mencipta anu dengan objek
dan tidak berhasil juga seperti array.

Cuba longgok senarai objek sebagai string menjadi array?

{% assign so = "{'foo'=>'x'},{'bar'=>nil}" | split: "," %}

raw code:

{% raw %}
    {% assign so = "{'foo'=>'x'},{'bar'=>nil}" | split: "," %}
{% endraw %}

output size sort:

{% if so %}
    {{ so }} {{ so | size }} {{ so | sort }}
{% else %}
    so tidak berhasil
{% endif %}

Cuba longgok data menjadi senarai objek sebagai string?
Pastikan aksara pilihan bagi split dan join tidak diguna
dalam string tersebut. Cuba dengan satu atau dua aksara.

input:

{% if site.data.b %}
    {{ site.data.b }}
    {% assign b = site.data.b | join: ";;" %}
{% else %}
    tiada data
{% endif %}

raw code:

{% raw %}
    {% assign b = site.data.b | join: ";;" %}
{% endraw %}

output string size:

{% if b %}
    {{ b }} {{ b | size }}
{% else %}
    b tidak berhasil
{% endif %}

Seterusnya longgok senarai objek b menjadi array dan guna
aksara selain yang diguna dalam senarai objek tersebut.

{% assign ba = b | split: ";;" %}

raw code:

{% raw %}
    {% assign ba = b | split: ";;" %}
{% endraw %}

output array size sort:

{% if ba %}
    {{ ba }} {{ ba | size }}
    {{ ba | sort }}
{% else %}
    ba tidak berhasil
{% endif %}

Akhirnya array ba boleh dipapar seperti site.data.b yang
asal. Beza antara dua data tersebut adalah ba boleh disusun,
dan ba mengandungi string dan bukan objek seperti asal.

{% assign asal = site.data.b %}
{% assign baru = ba | sort %}

{% comment %}
Kod `site.data.b | sort` mungkin sekali tidak sah kerana
data adalah objek dan bukan array. Juga disyaki punca github
pages gagal bina laman (a8d487e). Tiada petunjuk lain.
{% endcomment %}

raw code:

{% raw %}
    {% assign asal = site.data.b %}
    {% assign baru = ba | sort %}
{% endraw %}

output asal:

{% if asal %}
{% for a1 in asal %}
    {{ a1 }} {{ a1 | size }}
{% endfor %}
{% endif %}

output baru:

{% if baru %}
{% for a2 in baru %}
    {{ a2 }} {{ a2 | size }}
{% endfor %}
{% endif %}

output index `asal[0] asal[1]`:

    {{ asal[0] }}
    {{ asal[1] }}

output index `baru[0] baru[1]`:

    {{ baru[0] }}
    {{ baru[1] }}
