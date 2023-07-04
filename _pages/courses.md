---
layout: page
title: courses
permalink: /courses/
horizontal: true
---

<!-- pages/courses.md -->
<div class="courses">
<!-- Display courses without categories -->
{%- assign sorted_courses = site.courses -%}
<!-- Generate cards for each course -->
{% if page.horizontal -%}
<div class="container">
  <div class="row row-cols-2">
  {%- for course in sorted_courses -%}
    {% include courses_horizontal.html %}
  {%- endfor %}
  </div>
</div>
{%- else -%}
<div class="grid">
  {%- for course in sorted_courses -%}
    {% include courses.html %}
  {%- endfor %}
</div>
{%- endif -%}
</div>