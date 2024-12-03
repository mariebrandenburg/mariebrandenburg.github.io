---
order: 7
layout: page
permalink: /cv/
title: cv
description:
nav: true
---

[Click here for my full CV.](/assets/pdf/CV.pdf)

&nbsp;

---

## short cv
---

<div class="table-responsive">
	<table class="table table-sm table-borderless">
		<tr>
			<th scope="row">
				currently
			</th>
			<td>
				  Juniorprofessor for Combinatorics at RUB
			</td>
		</tr>
		<tr>
			<th scope="row">
				2024
			</th>
			<td>
				  Postdoc at KTH Stockholm in the <a href="https://www.kth.se/math/act/comb">Combinatorics Group</a> and the group of <a href="https://people.kth.se/~jochemko/">Katharina Jochemko</a>
			</td>
		</tr>
		<tr>
			<th scope="row">
				2023
			</th>
			<td>
				  Postdoc at MPI MiS (Leipzig) in the <a href="https://www.mis.mpg.de/montufar/index.html">Math Machine Learning Group</a> of <a href="https://personal-homepages.mis.mpg.de/montufar/">Guido Montúfar</a> 
			</td>
		</tr>
		<tr>
			<th scope="row">
				2020 -- 2022
			</th>
			<td>
				  PhD Student at MPI MiS (Leipzig) in the <a href="https://www.mis.mpg.de/nlalg/research.html">Nonlinear Algebra Group</a> of <a href="https://math.berkeley.edu/~bernd/">Bernd Sturmfels</a> <br>
				  PhD Advisor: <a href="http://www.math.uni-leipzig.de/~sinn/index_en.html">Rainer Sinn</a>
			</td>
		</tr>
		</table>
	</div>

&nbsp;

---

### organized events

---


<div class="events grid">
  {% assign sorted_projects = site.projects | sort: "importance" %}
  {% for project in sorted_projects %}
  {% if project.category == "event" %}
  <div class="grid-item">
    {% if project.redirect %}
    	<a href="{{ project.redirect }}" target="_blank">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          {{ project.title }}
          <p class="card-text">{{ project.description }}</p>
        </div>
      </div>
     {% if project.redirect %}
    	</a>
    {% endif %}
  </div>
{% endif %}
{% endfor %}

</div>

&nbsp;
