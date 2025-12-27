---
layout: default
title: Uncategorised Posts
permalink: /posts/uncategorised/
---

# Category: Uncategorised

{% assign filtered = site.posts | where: "category", "Uncategorised" %}

{% for post in filtered %}
<div style="border: 1px solid #ddd; border-radius: 8px; padding: 1rem; margin-bottom: 1.5rem; box-shadow: 0 2px 5px rgba(0,0,0,0.05);">

  <a href="{{ post.url | relative_url }}" style="font-size: 1.2rem; font-weight: bold; color: #333; text-decoration: none;">
    {{ post.title }}
  </a><br>

  {% if post.category %}
    <span style="font-size: 0.8rem; color: #666;">Category: {{ post.category }}</span><br>
  {% endif %}

  <span style="color: #999; font-size: 0.9rem;">
    {{ post.date | date: "%B %-d, %Y" }}
  </span><br><br>

</div>
{% endfor %}
