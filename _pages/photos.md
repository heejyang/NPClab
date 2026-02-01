---
layout: page
title: photos
permalink: /photos/
nav: true
nav_order: 4
---

<style>
  /* 갤러리 컨테이너: 무조건 Flex 모드로 작동 */
  .lab-gallery-row {
    display: flex !important;
    flex-wrap: wrap !important;
    margin: 0 -10px !important; /* 좌우 여백 보정 */
    width: 100% !important;
  }

  /* 개별 사진 카드: 무조건 50% 너비 고정 */
  .lab-gallery-item {
    width: 50% !important; 
    padding: 0 10px !important; /* 사진 사이 간격 */
    margin-bottom: 20px !important;
    box-sizing: border-box !important; /* 테두리 포함 크기 계산 */
    display: block !important; /* 숨겨짐 방지 */
  }

  /* 모바일(화면 폭 600px 이하)에서는 한 줄에 1개로 변경 */
  @media (max-width: 600px) {
    .lab-gallery-item {
      width: 100% !important;
    }
  }

  /* 이미지 스타일 강제 지정 */
  .lab-photo-card {
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 8px;
    overflow: hidden;
    height: 100%; /* 카드 높이 맞춤 */
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
  }

  .lab-photo-card img {
    width: 100% !important; /* 카드 안에서는 꽉 차게 */
    height: 300px !important; /* 높이 고정 (원하시면 수정 가능) */
    object-fit: cover !important; /* 찌그러짐 방지 */
    margin: 0 !important; /* 테마의 기본 여백 제거 */
    padding: 0 !important;
  }

  .lab-caption {
    padding: 10px;
    font-size: 0.9rem;
    color: #555;
    text-align: center;
    background: #f9f9f9;
    border-top: 1px solid #eee;
  }
  
  .year-header {
    margin-top: 40px;
    margin-bottom: 20px;
    font-weight: bold;
    border-bottom: 2px solid #eee;
    padding-bottom: 10px;
  }
</style>

{% assign grouped_photos = site.photos | group_by: "year" | sort: "name" | reverse %}

{% for year_group in grouped_photos %}

  <div class="lab-gallery-section">
    <h1 class="year-header">{{ year_group.name }}</h1>

    {% for event in year_group.items %}
      <div class="lab-gallery-row">
        {% for img in event.images %}
          <div class="lab-gallery-item">
            <div class="lab-photo-card">
              <img src="{{ img.image_path | relative_url }}" alt="{{ img.description }}">
              {% if img.description %}
                <div class="lab-caption">{{ img.description }}</div>
              {% endif %}
            </div>
          </div>
        {% endfor %}
      </div>
    {% endfor %}

  </div>
{% endfor %}
