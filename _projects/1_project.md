---
layout: page
title: Natural Products Discovery
description: Isolation & Structural Elucidations of Natural Products
img: assets/img/project1_main.jpeg
importance: 1
related_publications: true
---

<div class="row align-items-center">
<div class="col-sm-7">
        {% include figure.liquid loading="eager" path="assets/img/project1_1.jpg" title="Workflow of Natural Products Discovery" class="img-fluid rounded z-depth-1" style="width: 70%;" %}
        <p style="font-size: 0.8rem; color: #777; margin-top: 5px;">
            Figure 2: Instrumental setup for LC/MS-based quantitative analysis. Created by Biorender
        </p>
    </div>
    <div class="col-sm-5">
        <p><strong>연구 과정</strong></p>
    <strong>1. 추출 (Extraction)</strong>: 식물을 포함한 다양한 천연물(Natural Products)으로부터 유효성분을 효율적으로 얻어내기 위한 추출 과정
    <br>
    <strong>2. 분리 정제 (Isolation)</strong>: 분석용(Analytical) & 분리용(Preparative) 액체크로마토그래피(HPLC) 및 컬럼크로마토그래피 기술을 활용하여 복합적인 혼합물 상태의 추출물에서 개별성분들을 정밀하게 분리
    <br>
    <strong>3. 구조 규명 (Structural Elucidation)</strong>: 분리된 성분들의 화학적 구조를 밝히기 위해 질량분석(MS) 및 핵자기공명분광(NMR) 분석을 수행하고 화합물의 정확한 분자량과 원자 간 결합 형태를 분석
    <br>
    <strong>4. 신규 단일 화합물 확보 (Novel Single Compounds)</strong>: 구조가 규명된 단일 생리활성 화합물을 확보
    </div>
</div>

---

### 구조분석 기술: MS와 NMR의 역할

분리된 천연물의 정확한 화학 구조를 규명하기 위해서는 질량분석(Mass Spectrometry, MS)과 핵자기공명분광(Nuclear Magnetic Resonance, NMR)이 핵심적인 역할을 합니다. 이 두 분석법은 상호보완적으로 작용하여 화합물의 완전한 구조 정보를 제공합니다.

<div class="row mt-3 mb-4">
    <div class="col-sm-6">
        <h4 style="font-size: 1.1rem; color: #2c5f2d;">질량분석(MS)</h4>
        <p><strong>분자량 정보 제공</strong></p>
        <ul style="font-size: 0.95rem;">
            <li><strong>High-Resolution MS (HRMS)</strong>: 정밀한 분자량 측정을 통해 분자식(molecular formula)을 결정. 예를 들어, m/z 302.0447이 관찰되면 C₁₅H₁₀O₇의 분자식을 추정할 수 있음.</li>
            <li><strong>MS/MS (Tandem MS)</strong>: 화합물을 단편화(fragmentation)시켜 부분 구조 정보 확인. 특정 작용기의 존재 여부를 확인하고 구조 추정의 단서 제공.</li>
            <li><strong>Dereplication</strong>: MS 데이터를 데이터베이스와 비교하여 이미 알려진 화합물인지 신규 화합물인지 신속하게 판별.</li>
        </ul>
    </div>
    <div class="col-sm-6">
        <h4 style="font-size: 1.1rem; color: #2c5f2d;">핵자기공명분광(NMR)</h4>
        <p><strong>원자 수준의 구조 정보</strong></p>
        <ul style="font-size: 0.95rem;">
            <li><strong>¹H NMR</strong>: 수소 원자의 화학적 환경과 수를 파악하여 작용기의 종류와 위치 결정.</li>
            <li><strong>¹³C NMR</strong>: 탄소 골격 구조를 밝히고, 탄소의 화학적 환경(sp³, sp², carbonyl 등) 구분.</li>
            <li><strong>2D NMR (COSY, HSQC, HMBC 등)</strong>: 원자 간의 연결성(connectivity)을 밝혀 분자의 완전한 골격 구조결정. HMBC는 2-3 결합 떨어진 수소-탄소 상관관계를 제공하여 분자의 장거리 연결성 파악.</li>
            <li><strong>NOESY/ROESY</strong>: 공간적으로 가까운 원자들 간의 관계를 규명하여 입체화학(stereochemistry) 결정.</li>
        </ul>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <h4 style="font-size: 1.1rem; color: #2c5f2d;">통합 구조 규명 전략</h4>
        <p>MS와 NMR 데이터를 종합하여 다음과 같은 단계로 구조를 규명합니다:</p>
        <ol style="font-size: 0.95rem;">
            <li><strong>분자식 결정</strong>: HRMS로부터 정확한 분자량과 분자식 확인.</li>
            <li><strong>작용기 확인</strong>: ¹H, ¹³C NMR 스펙트럼과 필요시 IR 데이터를 통해 주요 작용기(hydroxyl, carbonyl, aromatic 등)의 존재 확인.</li>
            <li><strong>골격 구조 결정</strong>: 2D NMR (COSY, HSQC, HMBC)을 통해 원자 간 연결성을 파악하고 분자의 평면 구조 완성.</li>
            <li><strong>입체화학 결정</strong>: NOESY/ROESY와 커플링 상수(coupling constants) 분석을 통해 3차원 입체 구조 결정.</li>
            <li><strong>in silico 구조규명</strong>: 최신 연구에서는 NMR 데이터를 인공지능(AI)과 기계학습(ML) 알고리즘으로 구조규명의 정확도와 효율성을 높이고 있음.</li>
        </ol>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-8">
        {% include figure.liquid loading="eager" path="assets/img/project1_2.jpg" title="HPLC System Workflow" class="img-fluid rounded z-depth-1" %}
        <p style="font-size: 0.8rem; color: #777; margin-top: 5px;">
            Figure 3: HPLC 시스템의 구성 요소. 천연물 분리 정제에 필수적인 HPLC는 MS 및 NMR 분석을 위한 고순도 시료를 제공합니다.
        </p>
    </div>
    <div class="col-sm-4">
        <p style="font-size: 0.95rem;">
            <strong>분석 순서</strong><br>
            천연물 추출물 → HPLC 분리 정제 → 고순도 화합물 획득 → MS 분석 (분자량/분자식) → NMR 분석 (구조 결정) → 구조 확정
        </p>
    </div>
</div>

---

### Related Studies

우리 연구실은 다양한 약용식물로부터 생리활성 천연물을 발굴하고 구조를 규명해왔습니다. 주요 연구 성과를 다음 세 가지 주제로 분류하여 소개합니다.

---

#### **1. 신규화합물 연구** <span style="color: #666; font-size: 0.9em;">(Novel Compound Discovery)</span>

신규 천연물의 분리 및 구조 규명을 통해 화학적 다양성을 확대하고 있습니다.

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>산형과 약용식물로부터 신규 chromone 유도체 발굴</strong></p>
        <p>강활(Ostericum koreanum), 구릿대(Angelica dahurica, A. polymorpha) 등 산형과 식물에서 신규 chromone 화합물들을 분리 및 구조 규명하였습니다. 이들은 전통적으로 진통, 항염 등의 효능으로 사용되어 온 약재로부터 새로운 화학적 실체를 밝혀낸 연구입니다. {% cite lee2023new %} {% cite jeong2024new %} {% cite kim2024new %} {% cite kwon2022new %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>덜꿩나무에서 신규 α-glucosidic hydroquinone 유도체 발견</strong></p>
        <p>덜꿩나무(Viburnum erosum)에서 신규 α-glucosidic hydroquinone 유도체들을 발굴하고 구조를 규명하였습니다. 이는 당 결합 형태의 새로운 hydroquinone 골격을 가진 화합물로, 천연물 화학의 구조적 다양성을 확장하는 데 기여하였습니다. {% cite park2021alpha %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>다육식물 Stapelia gigantea의 신규 pregnane glycosides</strong></p>
        <p>아프리카 원산 다육식물인 Stapelia gigantea로부터 신규 pregnane 배당체들을 분리하고 입체화학을 포함한 완전한 구조를 규명하였습니다. Pregnane 골격은 스테로이드 계열의 독특한 화학 구조로, 다양한 생리활성의 기반이 됩니다. {% cite jang2022new %}</p>
    </div>
</div>

---

#### **2. 생리활성 탐색연구** <span style="color: #666; font-size: 0.9em;">(Bioactivity Exploration)</span>

분리된 천연물의 약리학적 효능을 규명하여 신약 개발 후보 물질을 발굴합니다.

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>기계학습 기반 RORγt 억제제 발굴 및 in vivo 검증</strong></p>
        <p>기계학습(Machine Learning), 가상 스크리닝(Virtual Screening), 그리고 in vivo 검증을 통합하여 천연물 유래 RORγt 억제제를 발견하였습니다. RORγt는 자가면역질환의 핵심 표적으로, AI 기반 신약 발굴 플랫폼의 성공적인 사례를 제시하였습니다. {% cite yoo2025discovery %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>Quercetin-3-Methyl Ether의 항바이러스 메커니즘 규명</strong></p>
        <p>HRV1B (Human Rhinovirus 1B) 바이러스에 대한 quercetin-3-methyl ether의 항바이러스 메커니즘을 규명하였습니다. 이 화합물은 초기 세포자멸사(apoptosis)를 유도하여 바이러스의 면역 회피를 극복하고, 바이러스 복제를 억제하며, 염증 병원성을 완화시키는 다면적 항바이러스 효과를 나타냈습니다. {% cite song2025quercetin %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>동백나무 뿌리 유래 Nrf2 활성화 triterpenoid saponins</strong></p>
        <p>동백나무(Camellia japonica) 뿌리에서 Nuclear Factor Erythroid 2-Related Factor-2 (Nrf2)를 활성화하는 triterpenoid saponin들을 분리하였으며, 항산화 유전자 발현을 증가시켜 산화 스트레스로부터 세포를 보호하는 효과를 확인하였습니다. {% cite ko2018nuclear %} {% cite kim2022camellia %}</p>
    </div>
</div>

---

#### **3. 동시분석 및 정량분석 연구** <span style="color: #666; font-size: 0.9em;">(Simultaneous & Quantitative Analysis)</span>

천연물 품질 관리 및 표준화를 위한 분석법 개발 연구입니다.

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>인삼 건조 정제 추출물의 ginsenoside 마커 동정</strong></p>
        <p>Dereplication 접근법과 UPLC-QTOF/MS 분석을 통해 Panax ginseng 건조 정제 추출물에서 ginsenoside 마커 성분들을 신속하게 동정하였습니다. 이는 고품질 인삼 제품의 품질 관리를 위한 효율적인 분석 전략을 제시하였습니다. {% cite yang2015identification %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>사철쑥과 인진쑥의 5가지 활성성분 동시 정량 및 판별</strong></p>
        <p>Artemisia princeps(사철쑥)와 A. capillaris(인진쑥)에서 5가지 활성 화합물의 동시 정량법을 UPLC-DAD 기반으로 확립하고, 다변량 분석을 통해 두 종을 명확히 판별하는 방법을 개발하였습니다. 이는 형태적으로 유사한 약용식물의 과학적 감별에 기여하였습니다. {% cite yang2014simultaneous %}</p>
    </div>
</div>

<div class="row align-items-center mb-4">
    <div class="col-sm-12">
        <p><strong>천궁(Cnidium Rhizome) 수추출물의 phthalic anhydride 유도체 동시 정량 및 안정성 시험</strong></p>
        <p>천궁 수추출물에서 senkyunolide A와 Z-ligustilide, 두 가지 phthalic anhydride 유도체의 동시 정량법을 확립하고 안정성 시험을 수행하였습니다. 이는 천궁의 품질 표준화 및 제제 개발에 필수적인 기초 자료를 제공하였습니다. {% cite jang2018simultaneous %}</p>
    </div>
</div>
