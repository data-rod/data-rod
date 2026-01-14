---
layout: page
title: Projetos
permalink: projetos/
---

<p class="lead">Explorações em análise espacial, sensoriamento remoto e ciência de dados florestais.</p>

<div class="projects-grid">
  {% for projeto in site.projetos %}
    <a href="{{ projeto.url | relative_url }}" class="project-card">
      
      <div class="project-image" 
           style="background-image: url('{{ projeto.image | default: "https://via.placeholder.com/400x200/052615/64ffda?text=DATA+ROD" }}');">
      </div>

      <div class="project-content">
        <h3>{{ projeto.title }}</h3>
        <p>{{ projeto.description }}</p>
        
        <div class="project-tags">
          {% for tool in projeto.tools %}
            <span class="tech-tag">{{ tool }}</span>
          {% endfor %}
        </div>
      </div>
    </a>
  {% endfor %}
</div>
