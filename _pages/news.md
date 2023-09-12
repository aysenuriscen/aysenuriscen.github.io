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
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include news.html %}
    {%- endfor %}
  </div>
