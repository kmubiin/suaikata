{% comment %}
paparan kemas kini melalui objek Liquid 'include_relative'
dan tetapan anu 'site' melalui objek YAML di _config.yml
{% endcomment %}

&#8942; Kemas kini setakat {{ site.time }}  
&#8942; Terbitan {{ site.kini.xyz }} ({{ site.kini.dev }})

{% if site.data.daftar %}
<!--cubaan objek Liquid memuat kandungan daripada fail YAML
yang tersimpan di _data/daftar.yml -->
<p style="color:#999999;">Data termuat {{ site.data.daftar.size }}</p>
{% endif %}

