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
{% assign subCategories = "多模态大模型,自监督学习,密集预测,时空预测" | split: ',' %}


<div>
{% include collapsible_panel.html subCat=subCategories categories=category resData=data  %}
</div>

{% endif %}

{% if category == categories[1]%}
{% assign subCategories = "积雪遥感" | split: ',' %}
{% assign appSubCategories = "积雪遥感建模与参数反演,积雪变化及其生态与气候效应" | split: ',' %}

<!-- <div>
{% include collapsible_panel.html subCat=subCategories categories=category resData=data appSubCat=appSubCategories%}
</div> -->


<div>
{% include collapsible_panel.html subCat=subCategories categories=category resData=data%}
</div>

{% endif %}



{% endfor %}


