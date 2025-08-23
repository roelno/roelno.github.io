---
layout: default
title: Projects
permalink: /projects/
---

# My Projects

<p class="hero-subtitle">A collection of my recent work and experiments</p>

<div class="projects-grid">
    {% for project in site.data.projects %}
    <a href="{{ project.url }}" class="project-card-link">
        <article class="project-card">
            <div class="project-image" 
                 {% if project.image_bg %}
                 style="background: {{ project.image_bg }};"
                 {% endif %}>
                {% if project.image %}
                <img src="{{ project.image }}" 
                     alt="{{ project.title }}"
                     loading="lazy">
                {% else %}
                <div class="image-placeholder">
                    <i class="fas fa-image fa-3x" style="color: #ccc;"></i>
                </div>
                {% endif %}
            </div>
            <div class="project-content">
                <h3 class="project-title">{{ project.title }}</h3>
                <p class="project-description">
                    {{ project.description }}
                </p>
                <div class="project-tech">
                    {% for tech in project.technologies %}
                    <span class="tech-tag">{{ tech }}</span>
                    {% endfor %}
                </div>
            </div>
        </article>
    </a>
    {% endfor %}
</div>