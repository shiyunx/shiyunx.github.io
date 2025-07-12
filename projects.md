---
layout: page # Use the generic page layout for this listing page
title: Projects
permalink: /projects/
---

## My Projects & Creations

Here's an overview of the projects I've worked on, from web applications to data analysis tools. Each entry links to a dedicated page with more details.

{% assign projects = site.projects | sort: "date" | reverse %}
{% for project in projects %}
<div class="project-listing">
  <h3><a href="{{ project.url | relative_url }}">{{ project.title | escape }}</a></h3>
  <p class="project-meta">
    <time datetime="{{ project.date | date_to_xmlschema }}">
      {{ project.date | date: "%b %-d, %Y" }}
    </time>
    {% if project.categories %}
      • Categories:
      {% for category in project.categories %}
        <a href="{{ site.baseurl | append: '/categories/' | append: category | slugify }}/">{{ category }}</a>{% unless forloop.last %}, {% endunless %}
      {% endfor %}
    {% endif %}
  </p>
  {% if project.featured_image %}
    <img src="{{ project.featured_image | relative_url }}" alt="{{ project.title | escape }}" style="max-width: 100%; height: auto; margin-bottom: 10px;">
  {% endif %}
  <p>{{ project.excerpt | strip_html | truncatewords: 30 }} <a href="{{ project.url | relative_url }}">Read more...</a></p>
</div>
<hr> {% endfor %}
