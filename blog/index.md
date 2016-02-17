---
layout: page
title: Gündelik Yazılar
excerpt: "Gerekli,gereksiz tüm konularda gündelik yazılar"
search_omit: true
---

<ul class="post-list">
{% for post in site.categories.blog %} 
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></a></article></li>
{% endfor %}
</ul>
