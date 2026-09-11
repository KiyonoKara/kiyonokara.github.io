---
layout: default
title: Blog
---

<section>
  <h2>Blog</h2>
  {% if site.posts.size == 0 %}
    <p class="tagline">No posts to see.</p>
  {% else %}
    <ul class="posts">
      {% for post in site.posts %}
        <li>
          <span class="date">{{ post.date | date: "%b %d, %Y" }}</span>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </li>
      {% endfor %}
    </ul>
  {% endif %}
</section>
