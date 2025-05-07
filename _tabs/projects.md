---
layout: projects
icon: fas fa-bars-progress
order: 4
title: Projects
permalink: /projects/
---

<div class="container py-5">
  <h1 class="mb-4 text-center">🚀 My Projects</h1>
  <div class="row row-cols-1 row-cols-md-3 g-4">
    {% for project in site.projects %}
      <div class="col">
        <div class="card h-100 shadow-sm">
          {% if project.image %}
            <img src="{{ project.image | relative_url }}" class="card-img-top" alt="{{ project.title }}">
          {% endif %}
          <div class="card-body d-flex flex-column">
            <h5 class="card-title">{{ project.title }}</h5>
            <p class="card-text">{{ project.excerpt | strip_html | truncate: 100 }}</p>
            <a href="{{ project.url | relative_url }}" class="btn btn-primary mt-auto">View Project</a>
          </div>
          <div class="card-footer text-muted">
            {{ project.date | date: "%B %d, %Y" }}
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
</div>
