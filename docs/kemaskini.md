{% comment %}
cubaan objek Liquid include_relative
{% endcomment %}

&#8942; Kemas kini setakat {{ site.time }}  
&#8942; Terbitan {{ site.terbitan }} ({{ site.peringkat }})

{% if page.name %}
<!--cubaan objek Liquid mengesan objek YAML iaitu page.name
yang mengandungi nama laman asal seperti index.md-->
<p style="color:#999999;">Kandungan hadir di {{ page.name }}</p>
{% endif %}

