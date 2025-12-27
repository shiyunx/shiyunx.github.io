---
layout: default
title: Data Projects
permalink: /projects/data/
---

# Category: Data

{% assign filtered = site.projects | where: "category", "Data" %}

{% for project in filtered %}
<div style="border: 1px solid #ddd; border-radius: 8px; padding: 1rem; margin-bottom: 1.5rem; box-shadow: 0 2px 5px rgba(0,0,0,0.05);">

  <a href="{{ project.url | relative_url }}" style="font-size: 1.2rem; font-weight: bold; color: #333; text-decoration: none;">
    {{ project.title }}
  </a><br>

  {% if project.category %}
    <span style="font-size: 0.8rem; color: #666;">Category: {{ project.category }}</span><br>
  {% endif %}

  {% if project.date %}
    <span style="color: #999; font-size: 0.9rem;">
      {{ project.date | date: "%B %-d, %Y" }}
    </span><br><br>
  {% endif %}
  
</div>
{% endfor %}

