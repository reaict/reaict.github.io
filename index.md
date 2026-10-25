---
layout: home
---

<h2 class="section-title">Le fil</h2>

{%- assign sorted_posts = site.posts | sort: "date" | reverse -%}
<ol>
  {%- for post in sorted_posts -%}
    <li>
      <a class="entry-title" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      <span class="entry-date">{{ post.date | date: "%d/%m/%Y" }}</span>
    </li>
  {%- endfor -%}
</ol>
