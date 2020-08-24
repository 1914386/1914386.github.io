---
layout: default
title: Categories
permalink: /category/
icon: th-list
type: page
---

<h1>{{ page.title }}</h1>
<hr>
<div>
  {% for category in site.categories %}
    <h3 id="{{ category | first }}" class="categories-topic">{{ category | first }}</h3>
    {% for posts in category %}
    {% for post in posts %}
    {% if post.url %}
      <ul class="categories-list">
        <li>
          <a class="categories-title" href="{{ post.url | prepend: site.url }}">{{ post.title }}
          <small class="tag-date">{{ post.date | date:"%F" }}</small>
          </a>
        </li>
      </ul>
    {% endif %}
    {% endfor %}
    {% endfor %}
  {% endfor %}
</div>

  