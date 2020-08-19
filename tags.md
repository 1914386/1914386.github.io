---
layout: page
permalink: /tags/
title: Tags
---

<ul class="tag-cloud">
{% for tag in site.tags %}
  <span style="font-size: {{ tag | last | size | times: 100 | divided_by: site.tags.size | plus: 70  }}%">
    <a href="#{{ tag | first | slugize }}">
      {{ tag | first }}
    </a> &nbsp;&nbsp;
  </span>
{% endfor %}
</ul>

<div id="archives">
{% for tag in site.tags %}
  <div class="archive-group">
    {% capture tag_name %}{{ tag | first }}{% endcapture %}
    <h3 id="#{{ tag_name | slugize }}">{{ tag_name }}</h3>
    <a name="{{ tag_name | slugize }}"></a>
    <ul class="archive-item">
      {% for post in site.tags[tag_name] %}
      <a href="{{ root_url }}{{ post.url }}">
      <li>
        {{ post.title }}
        <small class="post-date">{{ post.date | date_to_string }}</small>
      </li>
      </a>
      {% endfor %}
    </ul>
    {% endfor %}    
  </div>
</div>