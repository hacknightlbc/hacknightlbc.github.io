---
title: Home
layout: index
---

<ul>
  {% for post in site.posts %}
    <li>
      <h2><i class="fa fa-terminal"></i> <a href="{{ post.url }}">{{ post.title }}</a></h2>
      	<p class="postdate">{{ post.date | date: '%B %d, %Y' }}</p>
      {{ post.excerpt }}
      <p class="readmore"><a href="{{ post.url }}">Read More</a></p>
    </li>
  {% endfor %}
</ul>
