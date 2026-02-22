---
layout: projects
title: projects
permalink: /projects/
description: A collection of my projects.
nav: true
nav_order: 3
horizontal: false
---

<div class="projects">
  {% assign sorted_projects = site.projects | where_exp: "p", "p.published != false" | sort: "importance" %}
  {% assign research_projects = sorted_projects | where: "research", true %}
  {% assign other_projects = sorted_projects | where_exp: "item", "item.research != true" %}

  {% if research_projects.size > 0 %}
    <h2 class="category category-bar mb-3 mt-0">Academic Research</h2>
    <div class="row row-cols-1 row-cols-md-2 mb-5">
      {% for project in research_projects %}
        {% include projects.liquid %}
      {% endfor %}
    </div>
  {% endif %}

  {% if other_projects.size > 0 %}
    <h2 class="category category-bar mb-3 mt-5">Academic Projects</h2>
    <div class="row row-cols-1 row-cols-md-2">
      {% for project in other_projects %}
        {% include projects.liquid %}
      {% endfor %}
    </div>
  {% endif %}
</div>
