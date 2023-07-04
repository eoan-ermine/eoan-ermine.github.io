---
layout: page
title: books
permalink: /books/
horizontal: true
---

<!-- pages/books.md -->
<div class="books">
<!-- Display books without categories -->
{%- assign sorted_books = site.books | sort: "date_to" | reverse -%}
<!-- Generate cards for each book -->
{% if page.horizontal -%}
<div class="container">
  <div class="row row-cols-2">
  {%- for book in sorted_books -%}
    {% include books_horizontal.html %}
  {%- endfor %}
  </div>
</div>
{%- else -%}
<div class="grid">
  {%- for book in sorted_books -%}
    {% include books.html %}
  {%- endfor %}
</div>
{%- endif -%}
</div>