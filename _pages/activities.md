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
			            {% if event.talk %}
			              <br> Talk: <a class="events-talk">{{ event.talk }}</a>
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
			            {% if event.talk %}
			              <br> Talk: <a class="events-talk">{{ event.talk }}</a>
			            {% endif %}
		            </td>
		        </tr>
		    {% endif %}
			{% endfor %}
		</table>
	</div>
</div>