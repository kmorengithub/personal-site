---
title: Посты по категориям
layout: default
---

{% for category in site.categories %}
  <h3>{{ category | first }}</h3>
  <ul class="w3-ul">
	{% for posts in category %}
	{% for post in posts %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
    {% endfor %}
  </ul>
{% endfor %}
