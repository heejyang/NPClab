---
layout: page
title: photos
permalink: /photos/
nav: true
nav_order: 4
---

<style>
   photo-container {
    margin-bottom: 50px;
  }
   year-title {
    font-weight: bold;
    margin-bottom: 20px;
    border-bottom: 2px solid #eee;
    padding-bottom: 10px;
  }
  /* 카드 스타일 */
   custom-card {
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    overflow: hidden;
    background: #fff;
    margin-bottom: 20px; /* 아래쪽 카드와의 간격 */
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
  }
  /* 이미지 강제 리사이징 (중요) */
   custom-card img {
    width: 100% !important;  /* 가로를 무조건 카드 크기에 맞춤 */
    height: 300px !important; /* 세로 높이 고정 (원하는대로 수정 가능) */
    object-fit: cover;       /* 비율 유지하며 꽉 채우기 */
    display: block;
  }
  caption {
    padding: 10px;
    font-size: 0.9rem;
    color: #666;
    text-align: center;
    background-color: #fafafa;
  }
</style>

{% assign grouped_photos = site.photos | group_by: "year" | sort: "name" | reverse %}

{% for year_group in grouped_photos %}
  <div class="photo-container">
    <h1 class="year-title">{{ year_group.name }}</h1>

    {% for event in year_group.items %}
      <div class="row">
        {% for img in event.images %}
          <div class="col-6 col-md-6">
            <div class="custom-card">
              <img src="{{ img.image_path | relative_url }}" alt="{{ img.description }}">
              {% if img.description %}
                <div class="caption">{{ img.description }}</div>
              {% endif %}
            </div>
          </div>
        {% endfor %}
      </div>
      <br> 
    {% endfor %}
  </div>
{% endfor %}