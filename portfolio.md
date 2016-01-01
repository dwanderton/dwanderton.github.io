---
layout: page
title: Portfolio
permalink: /portfolio/
---

## Soon to be the portfolio page...!
_How exciting!_

 <h1 class="page-heading">Portfolio</h1>

  <ul class="post-list">
    {% for item in site.portfolio %}
      <li>
        <span class="post-meta">{{ item.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>