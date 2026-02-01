---
layout: page
title: Metabolomics
description: Mass Spectrometry-based Plant Metabolomics
img: assets/img/project2_1.jpg
importance: 2
related_publications: true
---

<div class="row justify-content-center">
    <div class="col-sm-12 text-center">
        {% include figure.liquid loading="eager" path="assets/img/project2_1.jpg" title="Metabolomics Workflow" class="img-fluid rounded z-depth-1" style="width: 70%;" %}
        <p style="font-size: 0.8rem; color: #777; margin-top: 5px;">
            Figure 1: Mass Spectrometry-based Metabolomics 연구 흐름도
        </p>
    </div>
</div>

<div class="caption text-justify">
    <p><strong>Metabolomics란?</strong></p>
    대사체학(Metabolomics)은 생물체 내에 존재하는 저분자량 대사산물(metabolites)을 포괄적으로 분석하는 학문입니다. 우리 연구실은 질량분석(Mass Spectrometry) 기반 기술을 활용하여 약용식물의 화학적 다양성을 체계적으로 탐구합니다.

    <p><strong>연구 과정</strong></p>
    1. 시료 준비 (Sample Preparation): 약용식물을 용매로 추출하여 대사산물을 추출합니다.
    2. LC-MS 분석 (LC-MS Analysis): 액체 크로마토그래피-질량분석(LC-MS)을 통해 수백-수천 개의 대사산물을 동시에 검출합니다.
    3. 데이터 전처리 (Data Processing): MZmine, MS-DIAL 등의 소프트웨어를 사용하여 피크를 검출하고 정렬합니다.
    4. 분자 네트워킹 (Molecular Networking): GNPS 플랫폼을 활용하여 구조적으로 유사한 화합물들을 네트워크로 시각화합니다.
    5. 통계 분석 및 화합물 동정 (Statistical Analysis & Annotation): 다변량 통계 분석과 데이터베이스 검색을 통해 바이오마커를 발굴하고 화합물을 동정합니다.
    6. 생물학적 해석 (Biological Interpretation): 동정된 대사산물의 생리활성과 약리 작용을 해석합니다.

</div>

<br>

<div class="row align-items-center">
    <div class="col-sm-7">
        {% include figure.liquid loading="eager" path="assets/img/project2_2.jpg" title="Molecular Networking" class="img-fluid rounded z-depth-1" style="width: 100%;" %}
        <p style="font-size: 0.8rem; color: #777; margin-top: 5px;">
            Figure 2: Molecular Networking을 통한 천연물 화학 프로파일링
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

---

### **핵심 연구 방법론**

#### **1. Molecular Networking을 활용한 천연물 화학 프로파일링**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>GNPS Feature-based Molecular Networking</strong></p>
        <p>Global Natural Products Social Molecular Networking (GNPS) 플랫폼의 Feature-based Molecular Networking 방법론 개발에 참여하였습니다. 이 기술은 질량분석 데이터에서 자동으로 분자 구조 유사성을 시각화하고, 신규 화합물 발견을 가속화합니다. {% cite nothias2020feature %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Repository-scale Suspect Spectral Library</strong></p>
        <p>대규모 천연물 대사체 동정을 위한 open access spectral library 구축에 기여하였습니다. 이 라이브러리는 untargeted metabolomics에서 화합물 동정의 정확도를 크게 향상시킵니다. {% cite bittremieux2023library %}</p>
    </div>
</div>

#### **2. 식물 대사체 데이터베이스 구축**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>동아시아 전통 약용식물의 대사체 데이터</strong></p>
        <p>동아시아 전통의학에서 사용되는 약용식물의 specialized metabolome에 대한 대규모 질량분석 데이터를 구축하고 공개하였습니다. 이 데이터는 천연물 연구자들이 약용식물의 화학적 특성을 이해하는 데 중요한 자원입니다. {% cite kang2022mass %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>용매 극성에 따른 약용식물 대사체 변화</strong></p>
        <p>다양한 용매 극성이 약용식물의 1차 및 2차 대사산물 추출에 미치는 영향을 체계적으로 분석한 질량분석 데이터를 구축하였습니다. 이 연구는 최적의 추출 조건 선택에 중요한 기초 자료를 제공합니다. {% cite park2025mass %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>plantMASST: 식물 화학분류학의 디지털화</strong></p>
        <p>커뮤니티 주도형 식물 화학분류학(chemotaxonomy) 디지털화 플랫폼 plantMASST 개발에 참여하였습니다. 이 플랫폼은 질량분석 데이터를 활용하여 식물의 화학적 특성을 체계적으로 분류하고 비교할 수 있게 합니다. {% cite gomes2024plantmasst %}</p>
    </div>
</div>

---

### **응용 연구**

#### **1. 표적 화합물 분리 (Targeted Isolation)**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>NMR Annotation Tool (SMART 2.0)을 이용한 표적 분리</strong></p>
        <p>택란(Eupatorium fortunei)에서 NMR annotation tool인 SMART 2.0을 활용하여 세포독성 sesquiterpene lactone들을 효율적으로 분리하였습니다. {% cite lee2020targeted %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Molecular Networking과 Hierarchical Clustering을 이용한 lignan 분리</strong></p>
        <p>마삭줄(Trachelospermum asiaticum)에서 molecular networking과 계층적 군집분석을 결합하여 lignan 화합물들을 표적 분리하였습니다. {% cite lee2020targeted_lignans %}</p>
    </div>
</div>

#### **2. 식물 종 판별 및 품질 평가**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>감귤 4종의 판별 마커 발굴</strong></p>
        <p>Molecular networking과 다변량 분석을 결합하여 4종의 감귤(Citrus species)을 명확하게 구별할 수 있는 판별 마커를 간단하게 동정하였습니다. {% cite choi2023simple %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>¹H NMR을 이용한 산초 3종의 신속 판별</strong></p>
        <p>¹H NMR 분광법을 활용하여 3종의 산초(Zanthoxylum species)를 신속하게 판별하고 품질을 평가하는 방법을 개발하였습니다. {% cite jang2020rapid %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Molecular Network를 이용한 산초 판별 마커의 in silico annotation</strong></p>
        <p>Molecular network derived annotation propagation 기법을 활용하여 산초 3종의 판별 마커를 in silico로 동정하였습니다. {% cite lee2019insilico %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Conduritol F: 천마와 이엽우피소의 판별 마커</strong></p>
        <p>¹H NMR 분광법을 이용하여 천마(Cynanchum wilfordii)와 이엽우피소(C. auriculatum)를 구별할 수 있는 판별 마커로 conduritol F를 발굴하였습니다. {% cite jang2017conduritol %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>LC/MS를 이용한 안토시아닌 함유 베리류 판별</strong></p>
        <p>LC/MS spectral 데이터를 활용하여 안토시아닌을 함유한 베리류를 빠르고 간단하게 판별하는 분석법을 개발하였습니다. {% cite yang2017fast %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>인진호와 사철쑥의 동시 정량 분석</strong></p>
        <p>UPLC-DAD를 이용하여 인진호(Artemisia capillaris)와 사철쑥(A. princeps)의 5가지 활성 성분을 동시에 정량하고, 다변량 분석으로 두 종을 판별하였습니다. {% cite yang2014simultaneous %}</p>
    </div>
</div>

#### **3. 복합 추출물의 화학 프로파일 분석**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>뽕나무(Morus alba) 부위별 화학 성분 프로파일</strong></p>
        <p>LC/MS의 두 가지 이온화 모드(positive/negative)를 결합한 molecular networking 방법을 사용하여 뽕나무의 다양한 부위(잎, 가지, 뿌리 등)에 따른 화학 성분 차이를 체계적으로 분석하였습니다. {% cite choi2021investigation %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>후추(Piper nigrum)의 acid amide alkaloid 프로파일링</strong></p>
        <p>후추에서 신규 dimer 화합물들을 발굴하고, acid amide alkaloid의 전체적인 화학 프로파일을 분석하였습니다. {% cite jung2024piper %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Cleistocalyx operculatus의 phloroglucinol meroterpenoids</strong></p>
        <p>¹H-NMR과 molecular networking을 결합한 dereplication 접근법을 사용하여 Cleistocalyx operculatus 꽃봉오리에서 neuraminidase 억제제인 phloroglucinol meroterpenoid들을 효율적으로 동정하였습니다. {% cite mai2025phloroglucinol %}</p>
    </div>
</div>

#### **4. 장내 미생물과 천연물의 상호작용**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Artemisinin과 장내 미생물의 ex vivo 상호작용</strong></p>
        <p>Multi-omics 접근법을 사용하여 항말라리아제인 artemisinin과 인간 장내 미생물 간의 상호작용을 분석하였습니다. 이 연구는 천연물의 체내 대사와 장내 미생물의 역할을 이해하는 데 기여합니다. {% cite gomes2025artemisinin %}</p>
    </div>
</div>

#### **5. 신규 대사체 발굴**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>전처리된 질량분석 데이터를 이용한 신규 이차대사산물 탐색</strong></p>
        <p>천연물에서 신규 이차대사산물을 발굴하기 위해 전처리된 질량분석 데이터를 활용하는 새로운 접근법을 개발하였습니다. {% cite kim2019exploring %}</p>
    </div>
</div>

#### **6. 항산화 활성 평가**

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>장미과 종자 4종의 항산화 특성과 페놀 프로파일</strong></p>
        <p>Molecular networking을 활용하여 장미과(Rosaceae) 식물 종자 4종의 항산화 특성과 페놀 화합물 프로파일을 체계적으로 분석하였습니다. {% cite lim2025molecular %}</p>
    </div>
</div>

---

### **연구 의의**

우리 연구실의 metabolomics 연구는 다음과 같은 기여를 하고 있습니다:

1. **방법론 혁신**: GNPS 플랫폼의 핵심 기술 개발에 참여하여 전 세계 천연물 연구자들이 사용할 수 있는 도구를 제공
2. **데이터 공유**: 동아시아 약용식물의 대규모 질량분석 데이터를 공개하여 학계에 기여
3. **효율적 연구**: Molecular networking을 활용한 표적 분리로 천연물 발굴 과정을 획기적으로 단축
4. **품질 관리**: 약용식물의 신속한 판별 및 품질 평가 기술 개발로 한약재 표준화에 기여

{% bibliography --cited %}
