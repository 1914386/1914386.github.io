---
layout: default
title: Categories
permalink: /categories/
---

<h1 class="page-title">{{ page.title }}</h1>
<p>카테고리 전체보기</p>
<hr>
<div>
  {% for category in site.categories %}
    <h3 id="{{ category | first }}" class="categories-topic">{{ category | first }}</h3>
    {% for posts in category %}
      <ul class="categories-list">
        {% for post in posts %}
        {% if post.url %}
        <li>
          <a class="categories-title" href="{{ post.url | prepend: site.url }}">{{ post.title }}
          <small class="tag-date">{{ post.date | date:"%F" }}</small>
          </a>
        </li>
        {% endif %}
        {% endfor %}
      </ul>
    {% endfor %}
  {% endfor %}
</div>