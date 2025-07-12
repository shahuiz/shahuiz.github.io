---
layout: page
permalink: /projects/
title: projects
description: A list of my projects.
nav: true
nav_order: 3
---

<div class="projects">
{% if site.enable_masonry %}
  <div class="grid">
{% endif %}

{% assign sorted_projects = site.projects | sort: 'nav_order' %}
{% for project in sorted_projects %}
  {% include projects_horizontal.liquid %}
{% endfor %}

{% if site.enable_masonry %}
  </div>
{% endif %}
</div>