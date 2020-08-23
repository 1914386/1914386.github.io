---
layout: page
permalink: /tags/
title: Tags
---

<div class="tag-cloud">
{% for tag in site.tags %}
  <a class="tag-list" href="#{{ tag | first | slugize }}">{{ tag | first }}</a>
{% endfor %}
</div>
<hr/>

<div id="archives">
{% for tag in site.tags %}
  <div class="archive-group">
    {% capture tag_name %}{{ tag | first }}{% endcapture %}
    <h3 id="#{{ tag_name | slugize }}">{{ tag_name }}</h3>
    <a name="{{ tag_name | slugize }}"></a>
    <ul class="archive-item">
      {% for post in site.tags[tag_name] %}
      <li>
      <a href="{{ root_url }}{{ post.url }}">
        {{ post.title }}
        <small class="tag-date">{{ post.date | date:"%F" }}</small>
      </a>
      </li>
      {% endfor %}
    </ul>
  </div>
  {% endfor %}
</div>