---
layout: default
title: Max Lazarus - Portfolio
permalink: /projects/
---

<div class="gallery-container">
<div class="project-gallery">
    {% for project in site.projects %}
      <div class="gallery-item">
        <a href="{{ project.url | relative_url }}">
          <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" {% if project.image-position or project.image-fit %}style="{% if project.image-fit %}object-fit: {{ project.image-fit }};{% endif %} {% if project.image-position %}object-position: {{ project.image-position }};{% endif %}"{% endif %} />
          <p>{{ project.title}}</p>
        </a>
      </div>
    {% endfor %}
</div>
</div>