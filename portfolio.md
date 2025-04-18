---
layout: default
title: Portfolio
---
# Mes Projets

Voici une sélection de mes projets réalisés dans le cadre de mes études et expériences professionnelles.

{% for project in site.data.projects %}
<div class="project" id="{{ project.id }}">
  <h2>{{ project.title }}</h2>
  <img src="{{ project.image }}" alt="{{ project.title }}" style="max-width: 100%;">
  <p>{{ project.description }}</p>
  {% if project.link %}<a href="{{ project.link }}">Voir le projet</a>{% endif %}
  {% if project.source %}| <a href="{{ project.source }}">Code source</a>{% endif %}
</div>
{% endfor %}
