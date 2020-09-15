{% comment %}
paparan kemas kini melalui objek Liquid 'include_relative'
dan tetapan anu 'site' melalui objek YAML di _config.yml
{% endcomment %}

&#8942; Kemas kini setakat {{ site.time }}  
&#8942; Terbitan {{ site.kini.xyz }} ({{ site.kini.dev }})

<!--cubaan objek Liquid memuat kandungan daripada fail YAML
yang tersimpan di _data/*.yml -->
<p style="color:#999999;">Data termuat
{% if site.data.daftar %} {{ site.data.daftar.size }}d {% endif %}
{% if site.data.lema %} {{ site.data.lema.size }}m {% endif %}
{% if site.data.terbit %} {{ site.data.terbit.size }}t {% endif %}
</p>
