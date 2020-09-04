{% comment %}
cubaan objek Liquid include_relative
{% endcomment %}

&#8942; Kemas kini setakat {{ site.time }}  
&#8942; Terbitan {{ site.terbitan }} ({{ site.peringkat }})

{% if page.asal %}
<!--cubaan objek Liquid mengesan objek YAML di laman asal-->
<p style="color:#999999;">Kandungan hadir di {{ page.asal }}</p>
{% endif %}

