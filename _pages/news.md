---
layout: page
title: news
permalink: /news/
description: Latest news
nav: true
nav_order: 2
---
<!-- pages/news.md -->
<div class="news">
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.news | sort: "importance" -%}
  {%- for project in sorted_projects -%}
      {% include news.html %}
  {%- endfor %}
</div>

