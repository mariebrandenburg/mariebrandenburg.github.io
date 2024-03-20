---
order: 1
layout: page
title: topics
permalink: /topics/
description:
nav: true
---

This site gives an overview over the various topics I have worked on and activities I am involved in.

&nbsp;

## Research ##
(Click on a tile for more information, slides of talks or publications)
{: style="color:gray; font-size: 90%; text-align: center;"}

<div class="projects grid">

  {% assign sorted_projects = site.projects | sort: "importance" | reverse %}
  {% for project in sorted_projects %}
  {% if project.category == "research" %}
  <div class="grid-item">
    {% if project.redirect %}
    <a href="{{ project.redirect }}" target="_blank">
    {% else %}
    <a href="{{ project.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title text-lowercase">{{ project.title }}</h2>
          <p class="card-text">{{ project.description }}</p>
          <div class="row ml-1 mr-1 p-0 icon-wrapper">
            {% if project.arxiv %}
              <div class="icon" data-toggle="tooltip" title="ArXiv Link">
                <a href="{{ project.arxiv }}" target="_blank"><i class="ai ai-arxiv ai"></i></a>
              </div>
            {% endif %}
            {% if project.github %}
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            {% endif %}
            {% if project.mathrepo %}
              <div class="icon" data-toggle="tooltip" title="MathRepo Link">
                <a href="{{ project.mathrepo }}" target="_blank"><i class="fas fa-code"></i></a>
              </div>
            {% endif %}
            {% if project.website %}
              <div class="icon" data-toggle="tooltip" title="website">
                <a href="{{ project.website }}" target="_blank"><i class="fas fa-code"></i></a>
              </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
{% endif %}
{% endfor %}

</div>


&nbsp;  

## Network and Math Communication ##
(Click on a tile for more information)
{: style="color:gray; font-size: 90%; text-align: center;"}

<div class="projects grid">

  {% assign sorted_projects = site.projects | sort: "importance" | reverse %}
  {% for project in sorted_projects %}
  {% if project.category == "other" %}
  <div class="grid-item">
    {% if project.redirect %}
    <a href="{{ project.redirect }}" target="_blank">
    {% else %}
    <a href="{{ project.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title text-lowercase">{{ project.title }}</h2>
          <p class="card-text">{{ project.description }}</p>
          <div class="row ml-1 mr-1 p-0 icon-wrapper">
            {% if project.arxiv %}
              <div class="icon" data-toggle="tooltip" title="ArXiv Link">
                <a href="{{ project.arxiv }}" target="_blank"><i class="ai ai-arxiv ai"></i></a>
              </div>
            {% endif %}
            {% if project.github %}
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            {% endif %}
            {% if project.mathrepo %}
              <div class="icon" data-toggle="tooltip" title="MathRepo Link">
                <a href="{{ project.mathrepo }}" target="_blank"><i class="fas fa-code"></i></a>
              </div>
            {% endif %}
            {% if project.website %}
              <div class="icon" data-toggle="tooltip" title="website">
                <a href="{{ project.website }}" target="_blank"><i class="fas fa-code"></i></a>
              </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}

</div>

