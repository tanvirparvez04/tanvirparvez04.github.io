---
layout: projects
title: projects
permalink: /_hidden/projects-index/
description: Internal index placeholder (hidden).
nav: false
nav_order: 999
horizontal: false
published: false
sitemap: false
---

<div class="projects">
  {% assign sorted_projects = site.projects | sort: "importance" %}

  {% if sorted_projects.size > 0 %}
    <h2 class="category category-bar mb-3 mt-0">Projects</h2>
    <div class="row row-cols-1 row-cols-md-2">
      {% for project in sorted_projects %}
        {% include projects.liquid %}
      {% endfor %}
    </div>
  {% endif %}
</div>
