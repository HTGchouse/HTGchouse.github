---
layout: archive
title: "信息可视化作品集"
date: 
modified:
excerpt: ""
tags: []
image: tableau.jpg
---
[信息可视化期末专案详细版](https://htgchouse.github.io/infovis/portfolio/%E6%95%B0%E6%8D%AE%E5%8F%AF%E8%A7%86%E5%8C%96/)
<img src="https://HTGchouse.github.io/images/仪表盘.png" alt="teaser" itemprop="image">
<br/>信息可视化作品
<div class="tiles">
{% for post in site.categories.infovis %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles 把所有categories 有 infovis 的列出来-->

