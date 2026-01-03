---
layout: page
title: photos
permalink: /photos/
nav: true
nav_order: 4
---

<style>
  .year-section { margin-bottom: 50px; }
  .event-title { font-size: 1.2rem; color: #444; margin-top: 20px; border-left: 4px solid #0056b3; padding-left: 10px; }
  
  /* 격자 레이아웃 (Grid) */
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); /* 화면 크기에 따라 자동 조절 */
    gap: 15px;
    margin-top: 15px;
  }
  
  .photo-card {
    border: 1px solid #eee;
    padding: 5px;
    background: #fff;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }
  
  .photo-card img {
    width: 100%;
    height: 200px; /* 사진 높이 통일 (필요 시 제거 가능) */
    object-fit: cover; /* 사진이 찌그러지지 않고 꽉 차게 */
    display: block;
  }
  
  .photo-caption {
    font-size: 0.85rem;
    color: #666;
    padding: 5px;
    text-align: center;
  }
</style>

{% assign grouped_photos = site.photos | group_by: "year" | sort: "name" | reverse %}

{% for year_group in grouped_photos %}
  <div class="year-section">
    <h1>{{ year_group.name }}</h1>
    <hr>

    {% for event in year_group.items %}
      <h3 class="event-title">
        {{ event.title }} <small style="color:#888; font-weight:normal; font-size:0.8em;">({{ event.date | date: "%Y.%m.%d" }})</small>
      </h3>

      <div class="gallery-grid">
        {% for img in event.images %}
          <div class="photo-card">
            <img src="{{ img.image_path }}" alt="{{ img.description }}">
            {% if img.description %}
              <div class="photo-caption">{{ img.description }}</div>
            {% endif %}
          </div>
        {% endfor %}
      </div>
    {% endfor %}
  </div>
{% endfor %}