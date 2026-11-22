---
permalink: /a2hd
title: ""
excerpt: ""
author_profile: true
favicon: /images/a2hd-icon.png
---
<style>

/* h3 {
    padding-left: 0;
    text-indent: 0;
    margin-bottom: 0.0rem;
} */

.support-section {
    margin-top: 3rem;
    padding-top: 1.5rem;
    border-top: 1px solid #e8e8e8;
}

.support-section h2 {
    margin-bottom: 0.5rem;
}

.support-logos {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 1.25rem 2rem;
    margin-top: 1rem;
}

.support-logos img {
    max-height: 56px;
    max-width: 220px;
    width: auto;
    height: auto;
    object-fit: contain;
}

.support-logos img.support-logo-tall {
    max-height: 72px;
}

@media (max-width: 600px) {
    .support-logos {
        gap: 1rem;
    }

    .support-logos img {
        max-width: 45%;
        max-height: 48px;
    }
}
</style>

<link rel="stylesheet" href="{{ '/assets/css/a2hd.css' | relative_url }}">

<div class="a2hd-overview">
  <header class="a2hd-intro">
    <img src="{{ '/images/a2hd%20logo.png' | relative_url }}" alt="" width="720" height="263">
    <h1>Adaptive AI &amp; Human Dynamics Lab <span lang="zh-Hant">智動實驗室</span></h1>
    <p>We study human-centred AI at Lingnan University, combining machine learning with research on how people behave, interact, and make decisions. <a href="{{ '/rpgadmission' | relative_url }}">Join the lab</a>.</p>
  </header>

  {% include a2hd-research-map.html %}

  <section class="a2hd-directions" aria-labelledby="research-directions">
    <h2 id="research-directions">Research directions</h2>

    <div class="a2hd-direction" id="human-dynamics" tabindex="-1">
      <h3>
        <span class="a2hd-panel-marker" aria-hidden="true"><i class="fas fa-users"></i></span>
        Human dynamics
      </h3>
      <p>We study how speech and interaction patterns reveal individual traits and group behaviour. We use nonlinguistic audio for personality profiling, study how groups form and move in public spaces, and model how personality shapes emotion in dialogue.</p>
    </div>

    <div class="a2hd-direction" id="adaptive-intelligence" tabindex="-1">
      <h3>
        <span class="a2hd-panel-marker" aria-hidden="true"><i class="fas fa-sliders-h"></i></span>
        Adaptive intelligence
      </h3>
      <p>We adapt language models to the user and the task. PeLA steers how a model expresses personality traits, MRM retrieves evidence in stages for questions that require multiple reasoning steps, and QAQ adjusts inference precision to the complexity of each query.</p>
    </div>

    <div class="a2hd-direction" id="domain-specific-evaluation" tabindex="-1">
      <h3>
        <span class="a2hd-panel-marker" aria-hidden="true"><i class="fas fa-clipboard-check"></i></span>
        Domain-specific evaluation
      </h3>
      <p>We evaluate models on the tasks they will perform. LLM4Rail supports personalised railway services, AutoRepairBench tests automotive repair reasoning with models such as RepairLLM, and PreConfig automates network configuration. In CCC8015, we develop hints tailored to each student’s learning progress.</p>
    </div>

    <div class="a2hd-direction" id="privacy-and-trust" tabindex="-1">
      <h3><span class="a2hd-panel-marker" aria-hidden="true">d</span> Privacy &amp; trust</h3>
      <p>Across our research, we study how models can unlearn trajectory data, how to watermark models trained through continuous prompt learning, and whether anonymous LLM sessions can be linked to the same person. In education, we compare AI-generated feedback across students to assess bias.</p>
    </div>

    <p class="a2hd-more">Explore our <a href="{{ '/projects' | relative_url }}">projects</a> and <a href="{{ '/publications' | relative_url }}">publications</a>.</p>
  </section>
</div>

# Lab Members

### Director
- Dr. Shen Jiaxing

### Staff
- [Dr. Zhou Yuzhi](https://www.ln.edu.hk/sds/dai/division/people/professor-zhou-yuzhi), Research Assistant Professor

### PhD Students
- Mr. Shen Yifei (25 intake)
- Mr. Wang Wenxuan (25 intake)
- Ms. Liu Zirui (25 intake)
- Mr. Kou Haoxuan (25 intake)
- Mr. Li Shuxing (26 intake)
- Mr. Liu Xinpeng (26 intake)
- Mr. Bian You (26 intake)
- Mr. Zuo Chenyu (27 Spring intake)
- Mr. Wang Haopeng (27 Spring intake)

### Research Assistants
- Mr. Zuo Chenyu

### UG Students
- Mr. Wu Ruiqing (26 intake)

### Alumni & Collaborators
- [Dr. Miao Hao](https://haomiao.website/) (now Research Assistant Professor at The Hong Kong Polytechnic University)
- [Mr. Zhao Haihong](https://haihongzhao.com/) (now PhD at HKUST)
- Mr. Shen Yifei (now PhD at LU)
- Mr. Gu Zepeng (now PhD at HKU)
- Mr. Liu Yuanjun (visiting Phd from Soochow University)
- Mr. Cheng Zhenkai


### Open Positions  
- **PhD students**: 3 quotas for 2027 Fall intake
<!-- - **Postdoctoral fellows**: 1 quota left -->


<section class="support-section">
  <h2>Acknowledgements</h2>
  <p>We gratefully acknowledge support from UGC, JHMUA, Lingnan University, The Hong Kong Polytechnic University, and 雲伽.</p>

  <div class="support-logos" aria-label="Supporting organizations">
    <img src="/images/ugc.png" alt="UGC" loading="lazy">
    <img src="/images/rgc.jpg" alt="RGC" loading="lazy">
    <img src="/images/jhmua.jpg" alt="JHMUA" loading="lazy">
    <img src="/images/ln.png" alt="Lingnan University" loading="lazy">
    <img src="/images/polyu.png" alt="PolyU" loading="lazy">
    <img class="support-logo-tall" src="/images/yjzn.png" alt="雲伽" loading="lazy">
  </div>
</section>
