---
layout: default
title: Projects
permalink: /projects/
---

# Projects
[Automation](/projects/automation/){: .filter-link } 
[Applications](/projects/applications/){: .filter-link }
[Data](/projects/data/){: .filter-link } 
[Uncategorised](/projects/uncategorised/){: .filter-link }

{% comment %}
  Step 1: Filter by category if page.category exists
{% endcomment %}
{% if page.category %}
  {% assign filtered_projects = site.projects | where: "category", page.category %}
{% else %}
  {% assign filtered_projects = site.projects %}
{% endif %}

{% comment %}
  Step 2: Ensure all dates are properly handled
  - Projects without a date are given a minimal date so they appear last
{% endcomment %}
{% assign projects_with_dates = "" | split: "" %}
{% for project in filtered_projects %}
  {% if project.date %}
    {% assign projects_with_dates = projects_with_dates | push: project %}
  {% else %}
    {% assign dummy_project = project %}
    {% assign dummy_project.date = "1970-01-01" %}
    {% assign projects_with_dates = projects_with_dates | push: dummy_project %}
  {% endif %}
{% endfor %}

{% comment %}
  Step 3: Sort by date descending
{% endcomment %}
{% assign sorted_projects = projects_with_dates | sort: "date" | reverse %}

{% comment %}
  Step 4: Display projects
{% endcomment %}
{% for project in sorted_projects %}
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

  {% if project.date and project.date != "1970-01-01" %}
    <span style="color: #999; font-size: 0.9rem;">
      {{ project.date | date: "%B %-d, %Y" }}
    </span><br><br>
  {% endif %}

</div>
{% endfor %}