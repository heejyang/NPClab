---
layout: page
title: Metabolomics
description: Mass Spectrometry-based Plant Metabolomics
img: assets/img/project2_main.jepg
importance: 2
related_publications: true
---

<div class="row justify-content-center">
    <div class="col-sm-12 text-center">
        {% include figure.liquid loading="eager" path="assets/img/project2_metabolites.jpg" title="Metabolomics Overview" class="img-fluid rounded z-depth-1" style="width: 90%;" %}
        <p style="font-size: 0.8rem; color: #777; margin-top: 5px;">
            Figure 1: 대사체학 연구 개요 - 1차/2차 대사산물 및 이종생물질의 포괄적 분석
        </p>
    </div>
</div>

<div class="caption text-justify">
    <p><strong>Metabolomics란?</strong></p>
    대사체학(Metabolomics)은 생물체 내에 존재하는 저분자량 대사산물(metabolites)을 포괄적으로 분석하는 학문입니다. 우리 연구실은 질량분석(Mass Spectrometry) 기반 기술을 활용하여 약용식물의 화학적 다양성을 체계적으로 탐구합니다.

    <p><strong>연구 과정</strong></p>
    1. 시료 준비 (Sample Preparation): 약용식물을 용매로 추출하여 대사산물을 추출합니다.
    <br><br>
    2. LC-MS 분석 (LC-MS Analysis): 액체 크로마토그래피-질량분석(LC-MS)을 통해 수백-수천 개의 대사산물을 동시에 검출합니다.
    <br><br>
    3. 데이터 전처리 (Data Processing): MZmine, MS-DIAL 등의 소프트웨어를 사용하여 피크를 검출하고 정렬합니다.
    <br><br>
    4. 분자 네트워킹 (Molecular Networking): GNPS 플랫폼을 활용하여 구조적으로 유사한 화합물들을 네트워크로 시각화합니다.
    <br><br>
    5. 통계 분석 및 화합물 동정 (Statistical Analysis & Annotation): 다변량 통계 분석과 데이터베이스 검색을 통해 바이오마커를 발굴하고 화합물을 동정합니다.
    <br><br>
    6. 생물학적 해석 (Biological Interpretation): 동정된 대사산물의 생리활성과 약리 작용을 해석합니다.

</div>

<br>

<div class="row justify-content-center">
    <div class="col-sm-12 text-center">
        {% include figure.liquid loading="eager" path="assets/img/project2_1.jpg" title="MS-based Metabolomics Workflow" class="img-fluid rounded z-depth-1" style="width: 70%;" %}
        <p style="font-size: 0.8rem; color: #777; margin-top: 5px;">
            Figure 2: Mass Spectrometry-based Metabolomics 연구 흐름도
        </p>
    </div>
</div>

<br>

<div class="row align-items-center">
    <div class="col-sm-7">
        {% include figure.liquid loading="eager" path="assets/img/project2_2.jpg" title="Molecular Networking" class="img-fluid rounded z-depth-1" style="width: 100%;" %}
        <p style="font-size: 0.8rem; color: #777; margin-top: 5px;">
            Figure 3: Molecular Networking을 통한 천연물 화학 프로파일링
        </p>
    </div>
    <div class="col-sm-5">
        <p><strong>Molecular Networking의 장점</strong></p>
        <p>
        - 대규모 데이터 시각화: 수천 개의 화합물을 네트워크 형태로 시각화하여 구조적 유사성을 한눈에 파악할 수 있습니다.
        <br>
        - 신규 화합물 발견 가속화: 기지 화합물과의 유사성을 기반으로 신규 유도체를 효율적으로 예측할 수 있습니다.
        <br>
        - 표적 분리 전략 수립: 생리활성이 있는 화합물 군집을 선별하여 분리 정제의 우선순위를 결정합니다.
        <br>
        - 식물 화학분류학: 식물 종 간의 화학적 차이를 비교하여 분류학적 관계를 규명합니다.
        </p>
    </div>
</div>

### Related Studies

질량분석 기반 대사체학 연구를 통해 천연물의 화학적 다양성을 체계적으로 탐구하고 있습니다. 주요 연구 성과를 다음 세 가지 주제로 분류하여 소개합니다.

---

#### **1. 분자네트워크 방법론 연구** <span style="color: #666; font-size: 0.9em;">(Molecular Networking Methodology)</span>

천연물 연구를 위한 혁신적인 분석 플랫폼과 도구를 개발하고 있습니다.

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>GNPS Feature-based Molecular Networking 방법론 개발</strong></p>
        <p>Global Natural Products Social Molecular Networking (GNPS) 플랫폼의 Feature-based Molecular Networking 방법론 개발에 핵심 참여자로 기여하였습니다. 이 기술은 질량분석 데이터에서 분자 구조 유사성을 자동으로 시각화하고, 신규 화합물 발견을 가속화하는 혁신적인 도구로 전 세계 천연물 연구자들이 널리 사용하고 있습니다. {% cite nothias2020feature %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Repository-scale Open Access Spectral Library 구축</strong></p>
        <p>대규모 천연물 대사체 동정을 위한 open access spectral library 구축 프로젝트에 참여하였습니다. 이 라이브러리는 propagated nearest neighbor suspect spectral matching을 활용하여 untargeted metabolomics에서 화합물 동정의 정확도와 커버리지를 획기적으로 향상시켰습니다. {% cite bittremieux2023library %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>plantMASST: 커뮤니티 주도형 식물 화학분류학 디지털화 플랫폼</strong></p>
        <p>커뮤니티 주도형 식물 화학분류학(chemotaxonomy) 디지털화 플랫폼 plantMASST 개발에 참여하였습니다. 이 플랫폼은 MASST (Mass Spectrometry Search Tool) 기술을 활용하여 식물의 화학적 특성을 체계적으로 분류하고 비교할 수 있게 하며, 전 세계 연구자들이 데이터를 공유하고 협력할 수 있는 생태계를 구축하였습니다. {% cite gomes2024plantmasst %}</p>
    </div>
</div>

---

#### **2. 식물대사체학 연구** <span style="color: #666; font-size: 0.9em;">(Plant Metabolomics)</span>

약용식물의 화학적 다양성을 규명하고 품질 관리 기술을 개발합니다.

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>용매 극성에 따른 약용식물 대사체 변화 데이터베이스</strong></p>
        <p>다양한 용매 극성이 약용식물의 1차 및 2차 대사산물 추출에 미치는 영향을 체계적으로 분석한 질량분석 데이터를 구축하여 Scientific Data에 공개하였습니다. 이 연구는 천연물 추출 시 최적의 용매 선택에 필수적인 기초 자료를 제공하며, 연구자들이 목적에 맞는 추출 조건을 설계하는 데 활용됩니다. {% cite park2025mass %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>후추(Piper nigrum)의 신규 dimer 화합물 발굴 및 acid amide alkaloid 프로파일링</strong></p>
        <p>후추에서 신규 dimer 화합물들을 발견하고, acid amide alkaloid의 전체적인 화학 프로파일을 대사체학 기법으로 체계적으로 분석하였습니다. 이 연구는 향신료로 널리 사용되는 후추의 화학적 복잡성과 구조적 다양성을 규명하여, 후추의 매운맛과 생리활성의 화학적 기반을 이해하는 데 기여하였습니다. {% cite jung2024piper %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>감귤 4종의 판별 마커 신속 동정 기술</strong></p>
        <p>Molecular networking과 다변량 분석을 결합한 통합 접근법을 활용하여 4종의 감귤(Citrus species)을 명확하게 구별할 수 있는 판별 마커를 간단하고 효율적으로 동정하였습니다. 이 기술은 형태적으로 유사한 감귤류의 과학적 감별과 품질 관리에 실용적으로 활용될 수 있습니다. {% cite choi2023simple %}</p>
    </div>
</div>

---

#### **3. 생체물질 대사체학 연구** <span style="color: #666; font-size: 0.9em;">(Biomatrix Metabolomics)</span>

생체 시스템과 천연물의 상호작용을 multi-omics로 규명합니다.

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Artemisinin과 인간 장내 미생물의 ex vivo 상호작용 연구</strong></p>
        <p>Multi-omics 접근법(metabolomics, proteomics, metagenomics)을 통합하여 항말라리아제인 artemisinin과 인간 장내 미생물 간의 복잡한 상호작용을 체계적으로 분석하였습니다. 이 연구는 천연물이 장내 미생물에 의해 어떻게 대사되고, 역으로 장내 미생물 조성에 어떤 영향을 미치는지를 규명하였습니다. {% cite gomes2025artemisinin %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>동아시아 전통 약용식물의 specialized metabolome 데이터베이스</strong></p>
        <p>동아시아 전통의학에서 사용되는 약용식물의 specialized metabolome에 대한 대규모 질량분석 데이터를 구축하고 Scientific Data를 통해 공개하였습니다. 이 데이터베이스는 100여 종 이상의 약용식물에 대한 표준화된 대사체 정보를 제공하며, 천연물 연구자들이 약용식물의 화학적 특성을 이해하고 비교하는 데 필수적인 참고 자료로 활용됩니다. {% cite kang2022mass %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>장미과 종자의 항산화 특성과 페놀 프로파일 분석</strong></p>
        <p>Molecular networking을 활용하여 장미과(Rosaceae) 식물 종자 4종의 항산화 특성과 페놀 화합물 프로파일을 체계적으로 분석하였습니다. 이 연구는 식물 종자라는 생체 매트릭스에서 항산화 활성과 화학 조성의 상관관계를 규명하여, 기능성 식품 소재 개발의 과학적 근거를 제시하였습니다. {% cite lim2025molecular %}</p>
    </div>
</div>

---

### **연구 의의** <span style="color: #666; font-size: 0.9em;">(Research Significance)</span>

우리 연구실의 대사체학 연구는 다음과 같은 기여를 하고 있습니다:

<ul style="line-height: 1.9;">
  <li><strong>방법론 혁신</strong>: GNPS 플랫폼의 핵심 기술 개발에 참여하여 전 세계 천연물 연구자들이 사용할 수 있는 도구를 제공</li>
  <li><strong>데이터 공유</strong>: 동아시아 약용식물의 대규모 질량분석 데이터를 Scientific Data를 통해 공개하여 학계에 기여</li>
  <li><strong>생체시스템 이해</strong>: Multi-omics 접근을 통해 천연물과 장내 미생물 간의 상호작용을 규명</li>
  <li><strong>품질 관리 기술</strong>: 약용식물의 신속한 판별 및 품질 평가 기술 개발로 한약재 표준화에 기여</li>
</ul>
