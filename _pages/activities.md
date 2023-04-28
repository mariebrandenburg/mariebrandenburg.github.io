---
order: 4
layout: page
permalink: /activities/
title: activities
description:
nav: true
---
{% capture nowunix %}{{'now' | date: '%Y%m%d'}}{% endcapture %}  

&nbsp;

---

### organizing

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
          <h2 class="card-title">{{ project.title }}</h2>
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

---

### current and upcoming activities

---
<div class="events">
	<div class="table-responsive">
	      <table class="table table-sm table-borderless">
			{% for event in site.data.events reversed %}
			{% capture posttime %}{{event.date | date : '%Y%m%d'}}{% endcapture %}
			{% if nowunix < posttime %}
				<tr>
					<th scope="row" class="events-date">
						{% if event.start-date %}
							{{ event.start-date | date: "%B %Y" }} - {{ event.date | date: "%B %Y" }} 
						{% else %}
			        		{{ event.date | date: "%B %Y" }} 
			        	{% endif %}
			        </th>
		            <td>
			            {% if event.url %}
			              <a class="events-title" href="{{ event.url }}">{{ event.title }}</a>
			            {% else %}
			              {{ event.title }}
			            {% endif %}
			            {% if event.location %}
			              <br> <a class="events-location">{{ event.location }}</a>
			            {% endif %}
		            </td>
		        </tr>
		    {% endif %}
			{% endfor %}
		</table>
	</div>
</div>

---

### past events

---

<div class="events">
	<div class="table-responsive">
	      <table class="table table-sm table-borderless">
			{% for event in site.data.events %}
			{% capture posttime %}{{event.date | date: '%Y%m%d'}}{% endcapture %}
			{% if nowunix >= posttime %}
				<tr>
			        <th scope="row" class="events-date">
						{% if event.start-date %}
							{{ event.start-date | date: "%B %Y" }} - {{ event.date | date: "%B %Y" }} 
						{% else %}
			        		{{ event.date | date: "%B %Y" }} 
			        	{% endif %}
			        </th>
		            <td>
			            {% if event.url %}
			              <a class="events-title" href="{{ event.url }}">{{ event.title }}</a>
			            {% else %}
			              {{ event.title }}
			            {% endif %}
			            {% if event.location %}
			              <br> <a class="events-location">{{ event.location }}</a>
			            {% endif %}
		            </td>
		        </tr>
		    {% endif %}
			{% endfor %}
		</table>
	</div>
</div>