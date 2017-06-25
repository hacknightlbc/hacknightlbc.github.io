---
title: Home
layout: index
---

<ul>
  {% for post in site.posts %}
    <li>
      <h2><i class="fa fa-terminal"></i> <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
      	<p class="postdate">{{ post.date | date: '%B %d, %Y' }}
      <a class="readmore" href="{{ site.baseurl }}{{ post.url }}"> >> Read More</a></p>
        {% if forloop.index == 1 %}
        {{ post.excerpt }}
        {% endif %}
    </li>
  {% endfor %}
</ul>
