---
layout: default
title: Projects
permalink: /projects/
nav: true
nav_order: 4
---

<section class="project-portfolio" aria-labelledby="projects-heading">
  <header class="project-intro">
    <p class="project-eyebrow">Featured work</p>
    <h1 id="projects-heading">Projects</h1>
  </header>
  <div class="project-grid">
    {% for project in site.data.featured_projects %}
      <a class="project-tile" href="{{ project.url | relative_url }}">
        <div class="project-image{% if project.contain %} project-image-contain{% endif %}">
          <img src="{{ project.image | relative_url }}" alt="{{ project.alt | escape }}" width="800" height="600" loading="lazy">
        </div>
        <h2>{{ project.title }} <span aria-hidden="true">↗</span></h2>
        <p>{{ project.description }}</p>
      </a>
    {% endfor %}
  </div>
</section>
