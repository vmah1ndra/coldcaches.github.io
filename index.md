---
title: "Holme"
---

## The Other Site
Find me [here](https://vmah1ndra.github.io).

## Posts
<ul>
  {% for post in site.posts %}
    {% assign sliced_array = post.url | slice: 0, 26 %}
    {% assign url_parts = post.url | slice: 0, 26 %}
    {% assign new_url = url_parts | join: "/coldcaches" %}
    <li>
      <a href="{{ new_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

## Tags

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
    {% assign url_parts = post.url | slice: 0, 26 %}
    {% assign new_url = url_parts | join: "/coldcaches" %}
    <li>
      <a href="{{ new_url }}">{{ post.title }} {{ url_parts }}</a>
    </li>
    {% endfor %}
  </ul>
{% endfor %}
