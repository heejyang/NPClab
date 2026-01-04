---
layout: page
title: photos
permalink: /photos/
nav: true
nav_order: 4
---

<style>
   year-section { margin-bottom: 50px; }
  
  /* 격자 레이아웃 (Grid) */
   gallery-grid {
    display: grid;
    grid-template-columns: 1fr 1fr; 
    gap: 15px;
    margin-top: 15px;
  }
  
  photo-card {
    border: 1px solid #ddd;
    border-radius: 8px;
    overflow: hidden;
    background: #fff;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  }
  
   photo-card img {
    width: 100%;
    height: 250px; 
    object-fit: cover;
    display: block;
  }
  
   photo-caption {
    font-size: 0.9rem;
    color: #555;
    padding: 10px;
    text-align: center;
    background: #f9f9f9;
  }
</style>

{% assign grouped_photos = site.photos | group_by: "year" | sort: "name" | reverse %}

{% for year_group in grouped_photos %}
  <div class="year-section">
    <h1 class="year-header">{{ year_group.name }}</h1>
    <hr style="border: 1px solid #eee;">

    {% for event in year_group.items %}
      <div class="gallery-grid">
        {% for img in event.images %}
          <div class="photo-card">
            <img src="{{ img.image_path | relative_url }}" alt="{{ img.description }}">
            {% if img.description %}
              <div class="photo-caption">{{ img.description }}</div>
            {% endif %}
          </div>
        {% endfor %}
      </div>
    {% endfor %}
  </div>
{% endfor %}