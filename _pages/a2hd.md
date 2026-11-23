---
permalink: /a2hd
title: ""
excerpt: ""
author_profile: true
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
    <div class="a2hd-intro-heading">
      <h1>Adaptive AI &amp; Human Dynamics Lab <span lang="zh-Hant">智動實驗室</span></h1>
      <img src="{{ '/images/a2hd%20logo.png' | relative_url }}" alt="" width="720" height="263">
    </div>
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
      <p>How do people’s behaviour and needs change across situations? We study signals such as speech, movement, and patterns of interaction to model how individuals and groups behave. We test which patterns carry across settings and which depend on context, so services can adapt the timing and type of support they offer.</p>
    </div>

    <div class="a2hd-direction" id="adaptive-intelligence" tabindex="-1">
      <h3>
        <span class="a2hd-panel-marker" aria-hidden="true"><i class="fas fa-sliders-h"></i></span>
        Adaptive intelligence
      </h3>
      <p>We design AI that adjusts to the user, the task, and the resources available. We develop ways to tailor responses, draw on relevant evidence, and vary how much computation a model spends on each request. We measure trade-offs among response quality, latency, and computing cost to understand where adaptation makes a system more useful.</p>
    </div>

    <div class="a2hd-direction" id="domain-specific-evaluation" tabindex="-1">
      <h3>
        <span class="a2hd-panel-marker" aria-hidden="true"><i class="fas fa-clipboard-check"></i></span>
        Domain-specific evaluation
      </h3>
      <p>We work with domain experts to turn real tasks and operating constraints into evaluation protocols. We test how AI handles routine and difficult cases and examine which failures have practical consequences. This gives partners evidence to decide where a system can support their workflow and what needs improvement before deployment.</p>
    </div>

    <div class="a2hd-direction" id="privacy-and-trust" tabindex="-1">
      <h3>
        <span class="a2hd-panel-marker" aria-hidden="true"><i class="fas fa-shield-alt"></i></span>
        Privacy &amp; trust
      </h3>
      <p>We study what AI systems retain or reveal about people, how to verify where models come from, and who may receive unfair results. We develop safeguards and test how well they protect people and how they affect system performance. This helps organisations choose protections suited to the data they handle and the decisions they support.</p>
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
- [Dr. Miao Hao](https://haomiao.website/) (now Full Professor of Computer Science at the Shenzhen Institute for Advanced Study, University of Electronic Science and Technology of China)
- [Mr. Zhao Haihong](https://haihongzhao.com/) (now PhD at HKUST)
- Mr. Shen Yifei (now PhD at LU)
- Mr. Gu Zepeng (now PhD at HKU)
- Mr. Liu Yuanjun (visiting Phd from Soochow University)
- Mr. Cheng Zhenkai


### Open Positions  
- **PhD students**: {{ site.data.a2hd_recruitment.phd_opening }}
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
