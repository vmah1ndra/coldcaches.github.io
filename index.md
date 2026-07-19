---
title: "Holme"
---

## The Other Site
Find me [here](https://vmah1ndra.github.io).

## Posts
<ul>
  {% for post in site.posts %}
    {% assign url_parts = post.url | slice: 0, 26 %}
    {% capture new_url %}https://vmah1ndra.github.io/coldcaches/{{ url_parts }}{% endcapture %}
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
    {% capture new_url %}https://vmah1ndra.github.io/coldcaches/{{ url_parts }}{% endcapture %}
    <li>
      <a href="{{ new_url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
  </ul>
{% endfor %}
