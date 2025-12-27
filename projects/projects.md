---
layout: default
title: Projects
permalink: /projects/
---
# Projects
[Automations](/projects/automations/){: .filter-link } [Applications](/projects/applications/){: .filter-link }[Data](/projects/data/){: .filter-link } [Uncategorised](/projects/uncategorised/){: .filter-link }

{% for project in site.projects %}
<div style="
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.05);
  padding: 1rem 1.5rem;
  margin-bottom: 1.5rem;
">

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

  {% if post.excerpt %}
    {{ post.excerpt }}
  {% endif %}

</div>
{% endfor %}

