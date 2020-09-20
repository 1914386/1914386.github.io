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

<!--
<div class="common-header">
  <div class="common-header-title">
    <h1>Categories</h1>
  </div>
</div>

<div class="categories">
  <ul>
    {% for category in site.categories %}
      {% assign category_name = category[0] %}
      {% assign category_url = category[0] | prepend: page.url %}
      <li>
        <a href="{{ category_url }}">
          <i class="fas fa-folder fa-fw"></i>
          <span>{{ category_name }}</span>
          <span class="categories-post-count">{{ site.categories[category_name] | size }}</span>
        </a>
        <ul class="child">
          {% for child in category[1].children %}
            {% assign child_name = child[1].name %}
            {% assign child_url = child[0] | prepend: '/' | prepend: category_url %}
            <li>
              <a href="{{ child_url }}">
                <i class="fas fa-folder fa-fw"></i>
                <span>{{ child_name }}</span>
                <span class="categories-post-count">{{ site.categories[child_name] | size }}</span>
              </a>
            </li>
          {% endfor %}
        </ul>
      </li>
    {% endfor %}
  </ul>
</div>
-->