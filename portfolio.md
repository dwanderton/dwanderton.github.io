---
layout: default
title: Portfolio
permalink: /portfolio/
---

<div class="home">
  <h1 class="page-heading">Portfolio</h1>

  <ul class="post-list">
    {% for post in site.categories.portfolio %}

      {% if post.url %}
      <br>
        <li>
          <a href="{{ post.url | prepend: site.baseurl }}">
            <img src="{{site.url}}/assets/img/portfolio_header/{{post.img}}">
          </a>
          <h2>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          </h2>
          <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
          <p>{{ post.excerpt }}</p>
        </li>
        
        {% if forloop.last == false %}
          <hr>
        {% endif %}
      {% endif %}
    {% endfor %}
    </ul>
</div>
