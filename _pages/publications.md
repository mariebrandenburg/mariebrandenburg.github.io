---
order: 6
layout: page
permalink: /research/
title: research
description: 
years_pre: [2022, 2021]
years_the: [2019,2016]
nav: true
---
&nbsp;
### preprint and publication

<div class="publications">

{% for y in page.years_pre %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
</div>

---

&nbsp;


### thesis

<div class="publications">

{% for y in page.years_the %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f thesis -q @*[year={{y}}]* %}
{% endfor %}
</div>

___