---
title: "LHRS - Research"
layout: textlay
excerpt: "LHRS -- Research"
sitemap: false
permalink: /research/
---

{% assign categories = "遥感图像智能解译,积雪遥感" |split: ','  %}
{% assign data = site.data.research %}


{% for category in categories  %}
{% if category == categories[0]%}
{% assign subCategories = "多模态大模型,自监督模型,密集预测模型,时空预测模型" | split: ',' %}


<div>
{% include collapsible_panel.html subCat=subCategories categories=category resData=data  %}
</div>

{% endif %}

{% if category == categories[1]%}
{% assign subCategories = "积雪遥感" | split: ',' %}
<!-- {% assign appSubCategories = "Remote Sensing,3D Reconstruction,Poultry Science" | split: ',' %} -->

<!-- <div>
{% include collapsible_panel.html subCat=subCategories categories=category resData=data appSubCat=appSubCategories%}
</div> -->


<div>
{% include collapsible_panel.html subCat=subCategories categories=category resData=data%}
</div>

{% endif %}



{% endfor %}


