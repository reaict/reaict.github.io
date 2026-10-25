---
layout: home
---

<h2 class="section-title">chroniques</h2>

<div class="chroniques-logo">
  <img src="{{ '/assets/' | append: site.logo | relative_url }}"
       alt="Logo"
       style="width: 2.65px; height: 2.65px;">
</div>

{%- assign sorted_posts = site.posts | sort: "date" | reverse -%}
<ol>
  {%- for post in sorted_posts -%}
    <li>
      <a class="entry-title" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      <span class="entry-date">{{ post.date | date: "%d/%m/%Y" }}</span>
    </li>
  {%- endfor -%}
</ol>
