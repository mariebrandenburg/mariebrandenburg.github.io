---
order: 6
layout: page
permalink: /research/
title: research
description: 
years_pre: [2022, 2021]
years_pub: [2023, 2022, 2021]
years_the: [2019,2016]
nav: true
---
&nbsp;
### preprint

<div class="publications">

{% for y in page.years_pre %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f preprint -q @*[year={{y}}]* %}
{% endfor %}
</div>

---

&nbsp;


### publication

<div class="publications">

{% for y in page.years_pub %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f published -q @*[year={{y}}]* %}
{% endfor %}
</div>

___

&nbsp;


### thesis

<div class="publications">

{% for y in page.years_the %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f thesis -q @*[year={{y}}]* %}
{% endfor %}
</div>

___