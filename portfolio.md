---
layout: page
title: Portfolio
permalink: /portfolio/
---

<ul class="post-list">
  {% for post in site.categories.portfolio %}
  
    {% if post.url %}
    <br>
      <li>
        <img src="{{post.img}}">
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <p>{{ post.excerpt }}</p>
      </li>
      <hr>
    {% endif %}
  {% endfor %}
</ul>