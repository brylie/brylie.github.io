```html
---
layout: default
title: Home
---

<h1>Welcome to My Blog</h1>

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <h2>
        <a href="{{ post.url | relative_url }}">
          {{ post.title }}
        </a>
      </h2>
      <span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</span>
      {% if post.excerpt %}
        <p>{{ post.excerpt }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>

{% if site.posts.size > 5 %}
  <p><a href="/archive">View all posts</a></p>
{% endif %}
```
