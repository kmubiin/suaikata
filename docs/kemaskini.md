{% comment %}
paparan kemas kini melalui objek Liquid 'include_relative'
dan tetapan anu 'site' melalui objek YAML di _config.yml
{% endcomment %}

&#8942; Kemas kini setakat {{ site.time }}  
&#8942; Terbitan {{ site.kini.xyz }} ({{ site.kini.dev }})

<!--cubaan objek Liquid memuat kandungan daripada fail YAML
yang tersimpan di _data/daftar.yml -->
<p style="color:#999999;">Data termuat
{% if site.data.daftar %}
<span> {{ site.data.daftar.size }}dt</span>
{% endif %}
{% if site.data.lema %}
<span> {{ site.data.lema.size }}lm</span>
{% endif %}
</p>
