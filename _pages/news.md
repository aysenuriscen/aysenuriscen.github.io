---
layout: page
title: news
permalink: /news/
description: Latest news
nav: true
nav_order: 2
horizontal: false
---
<!-- pages/news.md -->

<!-- Display projects without categories -->
  {%- assign sorted_projects = site.news | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include news.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
