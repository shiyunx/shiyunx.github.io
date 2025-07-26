---
layout: default
title: Posts
permalink: /post/
---
# Posts

{% for post in site.posts %}
<div style="
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.05);
  padding: 1rem 1.5rem;
  margin-bottom: 1.5rem;
">

  <a href="{{ post.url | relative_url }}" style="font-size: 1.2rem; font-weight: bold; color: #333; text-decoration: none;">
    {{ post.title }}
  </a><br>

  <span style="color: #999; font-size: 0.9rem;">
    {{ post.date | date: "%B %-d, %Y" }}
  </span><br><br>

  {{ post.excerpt }}

</div>
{% endfor %}
