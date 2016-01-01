---
layout: page
title: Portfolio
permalink: /portfolio/
---

<h1 class="page-heading">Portfolio</h1>

<ul class="post-list">
  {% for post in site.categories.portfolio %}
    {% if post.url %}
      <li>
        <img src="{{post.img}}">
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
         
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <p>{{ post.excerpt }}</p>
      </li>
    {% endif %}
  {% endfor %}
</ul>

        // if it's another category, we display the article
        <article>
            <hgroup>
                <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
            </hgroup>
                {{ post.excerpt }}
        </article>
          
  <ul class="post-list">
    {% for item in site.data.press %}
      <li>
        <span class="post-meta">{{ item.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>