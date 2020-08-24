---
layout: default
title: Categories
permalink: /category/
type: page
---
{% assign esc_title="{{ p.title }}" %}
{% assign esc_date="{{ p.date }}" %}
{% assign esc_ctgname="{{ hash }}" %}

<h1>{{ page.title }}</h1>
<hr>
<div>
    <h3 id="{{ category | first }}" class="categories-topic">{{ esc_ctgname }}</h3>
      <ul class="categories-list">
        <li v-for="p in posts" v-if="p.categories.indexOf(hash) != -1">
        <a v-bind:href="p.url">{{ esc_title }}</a>
        <small class="tag-date">{{ esc_date }}</small>
        </li>
      </ul>
</div>

<script>
  var hash = decodeURI(window.location.hash.substr(1));
 
  var postList = new Vue({
    el: '#post-list',
    data: {
      posts: []
    }
  });

  axios.get('/posts.json')
  .then(function (response) {
    postList.posts = response.data.posts;
  })
  .catch(function (error) {
    console.log(error);
  });
</script>
  