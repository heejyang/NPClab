---
layout: page
title: Natural Products Discovery
description: Isolation & Structural Elucidations of Natural Products
img: assets/img/12.jpg
importance: 1
related_publications: true
---

Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm-12">
        {% include figure.liquid loading="eager" path="assets/img/project1_1.jpg" title="Workflow of Natural Products Discovery" class="img-fluid rounded z-depth-1" style="width: 100%;" %}
    </div>
</div>
<div class="caption">
    이곳에 첫 번째 이미지(project1_1.jpg)에 대한 설명을 입력하세요. 천연물 유래 성분의 분리 및 구조 규명 연구 데이터 등을 설명하기 좋습니다.
</div>

<br>

<div class="row align-items-center">
    <div class="col-sm-7">
        {% include figure.liquid loading="eager" path="assets/img/project1_2.jpg" title="Quantitative study of Natural Products" class="img-fluid rounded z-depth-1" style="width: 100%;" %}
    </div>
    <div class="col-sm-5">
        <p><strong>연구 데이터 분석</strong></p>
        <p>이곳에 두 번째 이미지(project1_2.jpg)에 대한 설명을 입력하세요. 이미지 너비를 전체의 약 60%(7/12)로 설정하고, 오른쪽에 상세 설명을 배치했습니다.</p>
    </div>
</div>