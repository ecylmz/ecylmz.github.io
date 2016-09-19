---
layout: page
title: Teknik Yazılar
excerpt: "Çoğunlukla GNU/Linux Teknolojileriyle İlgili Yazılar"
search_omit: true
---

<ul class="post-list">
{% for post in site.categories.articles %} 
  <li>
    <a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
{% endfor %}
</ul>
