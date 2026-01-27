---
layout: page
title: Chemoproteomics & AI/ML
description: Target Identification using Chemoproteomics & AI/ML
img: assets/img/project1_2.jpg
importance: 3
related_publications: true
---

<div class="row justify-content-center">
    <div class="col-sm-12 text-center">
        {% include figure.liquid loading="eager" path="assets/img/project1_2.jpg" title="Chemoproteomics and AI/ML Workflow" class="img-fluid rounded z-depth-1" style="width: 70%;" %}
        <p style="font-size: 0.8rem; color: #777; margin-top: 5px;">
            Figure 1: AI/ML 기반 천연물 타겟 발굴 연구 흐름도
        </p>
    </div>
</div>

<div class="caption text-justify">
    <p><strong>Chemoproteomics & AI/ML이란?</strong></p>
    케모프로테오믹스(Chemoproteomics)는 화학(Chemistry)과 단백체학(Proteomics)을 결합한 학문으로, 천연물이 결합하는 단백질 타겟을 대규모로 동정하는 기술입니다. 우리 연구실은 여기에 인공지능(AI)과 머신러닝(ML)을 융합하여 천연물 기반 신약 개발을 가속화합니다.

    <p><strong>연구 과정</strong></p>
    1. 천연물 라이브러리 구축 (Natural Product Library): 다양한 약용식물로부터 추출한 천연물 화합물 라이브러리를 구축합니다.
    2. AI/ML 기반 활성 예측 (AI/ML-based Activity Prediction): 머신러닝 모델을 학습시켜 화합물의 생리활성과 타겟 단백질을 예측합니다.
    3. 가상 스크리닝 (Virtual Screening): 분자 도킹(Molecular Docking)과 약물동력학 예측을 통해 유망 화합물을 선별합니다.
    4. 생화학적 검증 (Biochemical Validation): In vitro assay를 통해 예측된 활성을 실험적으로 검증합니다.
    5. 프로테오믹스 분석 (Proteomics Analysis): LC-MS/MS 기반 프로테오믹스로 천연물이 결합하는 타겟 단백질을 동정합니다.
    6. 네트워크 약리학 (Network Pharmacology): 약용식물-타겟-질병 네트워크를 구축하여 다중타겟 효과와 작용 메커니즘을 규명합니다.
    7. In vivo 검증 (In vivo Validation): 동물 모델에서 치료 효능을 검증하고 작용 기전을 확인합니다.
</div>

<br>

<div class="row align-items-center">
    <div class="col-sm-7">
        {% include figure.liquid loading="eager" path="assets/img/project2_2.jpg" title="Network Pharmacology" class="img-fluid rounded z-depth-1" style="width: 100%;" %}
        <p style="font-size: 0.8rem; color: #777; margin-top: 5px;">
            Figure 2: 네트워크 약리학을 통한 약용식물-타겟-질병 관계 분석
        </p>
    </div>
    <div class="col-sm-5">
        <p><strong>AI/ML과 Chemoproteomics의 시너지</strong></p>
        <p>
        - 효율적인 후보 물질 발굴: AI 모델이 수만 개의 화합물 중에서 활성이 높은 후보를 우선 선별하여 실험 비용과 시간을 획기적으로 단축합니다.
        <br>
        - 타겟 예측 정확도 향상: 머신러닝이 화합물-단백질 상호작용 패턴을 학습하여 새로운 타겟을 예측합니다.
        <br>
        - 다중타겟 효과 규명: 네트워크 분석을 통해 약용식물의 복합적인 약리 작용을 체계적으로 이해합니다.
        <br>
        - 정밀 의학 구현: 개별 화합물의 명확한 분자 타겟을 규명하여 정밀 의학 기반 천연물 치료제를 개발합니다.
        </p>
    </div>
</div>

---

### **핵심 연구 분야**

#### **1. AI/ML 기반 신약 후보 물질 발굴**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Machine Learning과 Virtual Screening을 이용한 RORγt 억제제 발굴</strong></p>
        <p>머신러닝, 가상 스크리닝(virtual screening), 그리고 in vivo 검증을 결합하여 천연물 유래 RORγt (Retinoic acid receptor-related Orphan Receptor gamma t) 억제제를 발굴하였습니다. RORγt는 자가면역질환의 핵심 타겟으로, 본 연구는 AI 기반 천연물 신약 개발의 성공 사례를 제시합니다. {% cite yoo2025discovery %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>불균형 데이터를 위한 최적화 알고리즘 개발</strong></p>
        <p>이진 분류에서 불균형 데이터(imbalanced data)의 F_β score 최적화를 위한 surrogate loss function을 개발하였습니다. 이 방법은 천연물 활성 예측과 같이 양성 데이터가 적은 상황에서 모델 성능을 향상시킵니다. {% cite lee2021surrogate %}</p>
    </div>
</div>

#### **2. 바이오인포매틱스 및 네트워크 분석**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>약용식물-타겟 네트워크의 군집 분석</strong></p>
        <p>Multipartite network 기반 군집 분석을 통해 약용식물과 약리 타겟 간의 관계를 체계적으로 분석하였습니다. 이 연구는 약용식물의 다중타겟(multi-target) 효과를 이해하고, 새로운 약리 작용을 예측하는 데 활용됩니다. {% cite lee2021cluster %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>문헌 기반 생물학적 개체 네트워크 분석</strong></p>
        <p>문헌에서 동시 출현하는 생물학적 개체(약물, 단백질, 질병 등)의 계층적 네트워크 분석(Hierarchical network analysis)을 수행하였습니다. 이를 통해 숨겨진 약물-타겟-질병 간의 연관성을 발굴할 수 있습니다. {% cite yang2022hierarchical %}</p>
    </div>
</div>

#### **3. 프로테오믹스 및 통계 분석 방법론**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>정량 프로테오믹스를 위한 Shrinkage-based 통계 검정법</strong></p>
        <p>Bottom-up 정량 프로테오믹스에서 그룹 간 평균 차이를 검정하기 위한 shrinkage-based 통계 방법을 개발하였습니다. 이 방법은 적은 샘플 수에서도 높은 검정력(statistical power)을 제공하여, 케모프로테오믹스 연구에서 신뢰도 높은 타겟 동정을 가능하게 합니다. {% cite lee2025shrinkage %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>SLC46A3의 간 구리 항상성 조절 메커니즘 규명</strong></p>
        <p>Lysosomal transporter SLC46A3가 간세포의 세포질 구리 항상성을 조절하는 메커니즘을 프로테오믹스 및 대사체학 접근법으로 규명하였습니다. 이 연구는 Nature Communications에 발표되었으며, 금속 이온 대사와 관련된 질환 치료 타겟 발굴에 기여합니다. {% cite kim2021lysosomal %}</p>
    </div>
</div>

---

### **타겟 검증 및 메커니즘 연구**

#### **1. 천연물의 분자 타겟 및 신호 경로 규명**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>인삼 사포닌 Ginsenoside 20(S)-Rh2의 항암 메커니즘</strong></p>
        <p>Ginsenoside 20(S)-Rh2가 IL-6로 유도된 JAK2/STAT3 신호 경로를 표적으로 하여 대장암 세포 증식을 억제함을 규명하였습니다. 이는 인삼 사포닌의 명확한 분자 타겟을 제시한 연구입니다. {% cite han2016ginsenoside %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Amentoflavone의 Nrf2 활성화 경로</strong></p>
        <p>Amentoflavone이 p38 MAPK-AKT 경로를 통해 산화 스트레스를 유발하고, 이것이 Nrf2 (Nuclear Factor Erythroid 2-Related Factor 2)를 활성화하여 항산화 방어 시스템을 증진시킴을 규명하였습니다. {% cite wahyudi2018amentoflavone %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>E-p-Methoxycinnamoyl-α-L-rhamnopyranosyl ester의 Nrf2 안정화 메커니즘</strong></p>
        <p>Scrophularia buergeriana에서 분리한 phenylpropanoid가 ubiquitination을 억제하여 Nrf2의 안정성을 증가시키는 메커니즘을 밝혔습니다. {% cite jeong2018epmethoxycinnamoyl %}</p>
    </div>
</div>

#### **2. Inflammasome 및 면역 조절 타겟**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Obovatol의 다중 inflammasome 억제 효과</strong></p>
        <p>후박(Magnolia obovata)에서 분리한 obovatol이 NLRP3, AIM2, 그리고 non-canonical inflammasome을 모두 억제하는 광범위한 항염증 효과를 나타냄을 규명하였습니다. {% cite kim2019obovatol %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Panaxydol의 NLRP3 inflammasome 억제를 통한 NASH 개선</strong></p>
        <p>인삼에서 추출한 panaxydol이 NLRP3 inflammasome 활성화를 억제하여 비알코올성 지방간염(NASH)으로 인한 간 손상을 개선시킴을 확인하였습니다. {% cite kim2024panaxydol %}</p>
    </div>
</div>

#### **3. 대사 질환 관련 타겟**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>복합 천연물 처방의 지방간 개선 메커니즘</strong></p>
        <p>여러 복합 천연물 처방(Gangjihwan, GGEx18, Gambigyeongsinhwan 등)이 SREBP1C, PPARγ, C/EBPα 등의 지방 생성 전사인자를 조절하여 지방간 및 염증을 개선시키는 메커니즘을 규명하였습니다. {% cite jang2018gangjihwan %} {% cite roh2017effect %} {% cite yoon2017effects %} {% cite lim2018polyherbal %}</p>
    </div>
</div>

---

### **정량 분석 및 품질 관리**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>천연물 표준화를 위한 HPLC 정량 분석법 개발</strong></p>
        <p>다양한 약용식물 추출물의 지표성분을 동시 정량하는 HPLC 분석법을 개발하여 천연물 의약품의 품질 관리에 기여하였습니다. {% cite yoo2020simultaneous %} {% cite jang2018simultaneous %} {% cite jeong2018determination %}</p>
    </div>
</div>

---

### **연구 의의 및 미래 방향**

우리 연구실의 chemoproteomics 및 AI/ML 연구는 다음과 같은 혁신을 추구합니다:

1. **AI 기반 신약 발굴**: 머신러닝과 가상 스크리닝을 활용하여 방대한 천연물 라이브러리에서 효율적으로 활성 화합물을 발굴
2. **다중 오믹스 통합**: 프로테오믹스, 대사체학, 트랜스크립토믹스 데이터를 통합하여 천연물의 작용 메커니즘을 종합적으로 이해
3. **네트워크 약리학**: 약용식물-타겟-질병 네트워크 분석을 통해 천연물의 다중타겟 효과와 시너지 작용을 규명
4. **정밀 의학**: 개별 천연물 성분의 명확한 분자 타겟을 규명하여 정밀 의학 기반 천연물 치료제 개발에 기여

우리는 전통 천연물 화학과 최첨단 AI/오믹스 기술을 융합하여, 천연물 기반 신약 개발의 새로운 패러다임을 제시하고 있습니다.

{% bibliography --cited %}
