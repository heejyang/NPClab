---
layout: page
title: photos
permalink: /photos/
nav: true
nav_order: 4
---

<style>
   year-section { margin-bottom: 60px; }
   year-header { 
    font-size: 2.2rem; 
    font-weight: 800; 
    margin-bottom: 15px; 
    color: #333;
  }
  
  /* 한 라인에 2장씩 배치하는 설정 */
   gallery-grid {
    display: grid;
    grid-template-columns: 1fr 1fr; /* 1:1 비율로 두 칸 생성 */
    gap: 20px; /* 사진 사이의 간격 */
    margin-top: 20px;
  }
  
   photo-card {
    border: 1px solid #eee;
    border-radius: 12px;
    overflow: hidden;
    background: #fff;
    transition: transform 0.2s; /* 살짝 커지는 효과 (선택사항) */
  }
  
   photo-card:hover {
    transform: translateY(-5px);
  }
  
   photo-card img {
    width: 100%;
    height: 350px; /* 한 줄에 두 장이므로 높이를 조금 더 키웠습니다 */
    object-fit: cover;
    display: block;
  }
  
   photo-caption {
    font-size: 0.95rem;
    color: #444;
    padding: 12px;
    text-align: center;
    background: #fdfdfd;
    border-top: 1px solid #eee;
  }

  /* 모바일(작은 화면)에서도 두 장을 유지할지, 한 장으로 바꿀지 결정 */
  @media (max-width: 600px) {
     gallery-grid {
      grid-template-columns: 1fr 1fr; /* 모바일에서도 2장을 유지하려면 그대로 둠 */
      /* 만약 모바일에서 너무 작아 보이면 1fr; 로 바꾸시면 됩니다 */
    }
     photo-card img { height: 200px; } /* 모바일용 높이 조절 */
  }
</style>

{% assign grouped_photos = site.photos | group_by: "year" | sort: "name" | reverse %}

{% for year_group in grouped_photos %}
  <div class="year-section">
    <h1 class="year-header">{{ year_group.name }}</h1>
    <hr>

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