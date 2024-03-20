---
order: 6
layout: page
permalink: /publications/
title: publications
description: 
years_preprint: [2024, 2023]
years_publication: [2024, 2023, 2022, 2021]
years_thesis: [2023,2019,2016]
nav: true
---
&nbsp;
### preprints

<div class="publications">

{% for y in page.years_preprint %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f preprint -q @*[year={{y}}]* %}
{% endfor %}
</div>

---

&nbsp;


### publications

<div class="publications">

{% for y in page.years_publication %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f published -q @*[year={{y}}]* %}
{% endfor %}
</div>


___

&nbsp;


### theses

<div class="publications">

{% for y in page.years_thesis %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f thesis -q @*[year={{y}}]* %}
{% endfor %}
</div>

___