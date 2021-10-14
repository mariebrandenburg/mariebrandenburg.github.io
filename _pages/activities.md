---
order: 4
layout: page
permalink: /activities/
title: activities
description:
nav: false
---
{% capture nowunix %}{{'now' | date: '%Y%m'}}{% endcapture %}  

&nbsp;

---

### upcoming events

---
<div class="events">
	<div class="table-responsive">
	      <table class="table table-sm table-borderless">
			{% for event in site.data.events reversed %}
			{% capture posttime %}{{event.date | date: '%Y%m'}}{% endcapture %}
			{% if nowunix < posttime %}
				<tr>
			        <th scope="row" class="events-date">{{ event.date | date: "%B %Y" }} </th>
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
			{% capture posttime %}{{event.date | date: '%Y%m'}}{% endcapture %}
			{% if nowunix >= posttime %}
				<tr>
			        <th scope="row" class="events-date">{{ event.date | date: "%B %Y" }} </th>
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