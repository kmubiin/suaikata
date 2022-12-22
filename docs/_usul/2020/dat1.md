---
date: 2020-09-14
title: Kod cubaan awal memapar data
---

### Kod cubaan awal memapar data

Di sini, kod cubaan merujuk pada objek dan kenyataan Liquid
yang sebelum ini termuat di laman Jekyll. Semua kod telah
disalin semula seperti hasil paparan dan disusun semula
supaya mudah dibaca.

#### string menjadi array

Input:
{% raw %}
    {% assign s = "foo, bar" | split: ", " %}
    {% if s %}
        {{ s }} {{ s | size }} {{ s | sort }}
    {% else %}
        s tidak berhasil
    {% endif %}
{% endraw %}

Output:
{% raw %}
    foobar 2 barfoo
{% endraw %}

#### objek sebagai objek

Di sini, objek merujuk pada beberapa string yang dikumpul
dalam kurungan `{...}` pada input.

Input:
{% raw %}
    {% assign o = {'c','a','b'} %}
{% endraw %}

Output:
{% raw %}
    Liquid Warning: Liquid syntax error (line 126):
    Unexpected character { in "{{{'c','a','b'} }}" ...
{% endraw %}

Jadi, ternyata Liquid tidak boleh mencipta anu dengan objek
dan tidak berhasil juga seperti array.

#### objek sebagai string menjadi array

Di sini, objek adalah senarai objek kerana ada dua objek
yang tersenarai, dan senarai objek adalah string kerana
ada tanda petik `"..."` pada objek tersebut.

Input:
{% raw %}
    {% assign so = "{'foo'=>'x'},{'bar'=>nil}" | split: "," %}
    {% if so %}
        {{ so }} {{ so | size }} {{ so | sort }}
    {% else %}
        so tidak berhasil
    {% endif %}
{% endraw %}

Output:
{% raw %}
    {'foo'=>'x'}{'bar'=>nil} 2 {'bar'=>nil}{'foo'=>'x'}
{% endraw %}

#### data menjadi array

Data:
{% raw %}
    # kandungan data tersimpan di _data/b.yml
    ---
    -
      id: '0x011'
      num: 11
      test: true
    -
      id: '0x002'
      num: 2
      test: null
    ...
{% endraw %}

Data harus ditukar menjadi string, sebelum dapat ditukar
menjadi array. Pastikan aksara pilihan bagi split dan join
tidak diguna dalam string itu. Cuba satu atau dua aksara.

Input:
{% raw %}
    {% if site.data.b %}
        {{ site.data.b }}
        {% assign b = site.data.b | join: ";;" %}
    {% else %}
        tiada data
    {% endif %}
    {% if b %}
        {{ b }} {{ b | size }}
    {% else %}
        b tidak berhasil
    {% endif %}
{% endraw %}

Output:
{% raw %}
    {"id"=>"0x011", "num"=>11, "test"=>true};;{"id"=>"0x002", "num"=>2, "test"=>nil} 80
{% endraw %}

Seterusnya longgok senarai objek b menjadi array dan guna
aksara pilihan yang diguna dalam senarai objek tersebut.
Dalam input sebelum ini, aksara dua titik koma `;;`
digunakan sebagai aksara pilihan.

Input (akhir):
{% raw %}
    {% assign ba = b | split: ";;" %}
    {% if ba %}
        {{ ba }} {{ ba | size }}
        {{ ba | sort }}
    {% else %}
        ba tidak berhasil
    {% endif %}
{% endraw %}

Output (akhir):
{% raw %}
    {"id"=>"0x011", "num"=>11, "test"=>true}{"id"=>"0x002", "num"=>2, "test"=>nil} 2
    {"id"=>"0x002", "num"=>2, "test"=>nil}{"id"=>"0x011", "num"=>11, "test"=>true}
{% endraw %}

Akhirnya array ba boleh dipapar seperti site.data.b yang
asal. Beza antara dua data tersebut adalah ba boleh disusun,
dan ba mengandungi string dan bukan objek seperti asal.

> Komen: Kod `site.data.b | sort` mungkin sekali tidak sah
kerana data adalah objek dan bukan array. Juga disyaki punca
Github Pages gagal bina laman (a8d487e).

Input:
{% raw %}
    {% assign asal = site.data.b %}
    {% if asal %}
    {% for a1 in asal %}
        {{ a1 }} {{ a1 | size }}
    {% endfor %}
    {% endif %}

    {% assign baru = ba | sort %}
    {% if baru %}
    {% for a2 in baru %}
        {{ a2 }} {{ a2 | size }}
    {% endfor %}
    {% endif %}
{% endraw %}

Output:
{% raw %}
    {"id"=>"0x011", "num"=>11, "test"=>true} 3

    {"id"=>"0x002", "num"=>2, "test"=>nil} 3
    
    {"id"=>"0x002", "num"=>2, "test"=>nil} 38

    {"id"=>"0x011", "num"=>11, "test"=>true} 40
{% endraw %}

Bandingkan susunan data apabila dicapai melalui index
seperti berikut.

Input index:
{% raw %}
    {{ asal[0] }}
    {{ asal[1] }}

    {{ baru[0] }}
    {{ baru[1] }}
{% endraw %}

Output index:
{% raw %}
    {"id"=>"0x011", "num"=>11, "test"=>true}
    {"id"=>"0x002", "num"=>2, "test"=>nil}
    
    {"id"=>"0x002", "num"=>2, "test"=>nil}
    {"id"=>"0x011", "num"=>11, "test"=>true}
{% endraw %}

Berdasarkan kod cubaan di atas, Liquid tidak boleh memapar
data yang disusun secara langsung kerana data adalah objek.
Liquid boleh menyusun array, tetapi bukan objek.

Mengikut cara Liquid, data harus ditukar menjadi string
terlebih dahulu sebelum menjadi array. Hasilnya, data dapat
disusun tetapi bukan lagi objek seperti asal.
