---
permalink: /rpgadmission
title: "Join the A2HD Lab"
excerpt: "PhD and postdoctoral opportunities in human-centred AI at Lingnan University."
author_profile: true
favicon: /images/a2hd-icon.png
---

{% assign lab_url = '/a2hd' | relative_url %}
{% assign recruitment = site.data.a2hd_recruitment %}
{% assign phd_subject = 'RPG Application – Your Name – Research Area' %}
{% assign phd_subject_encoded = phd_subject | url_encode | replace: '+', '%20' %}

<link rel="stylesheet" href="{{ '/assets/css/a2hd.css' | relative_url }}">
<link rel="stylesheet" href="{{ '/assets/css/rpgadmission.css' | relative_url }}">

<div class="a2hd-overview recruitment">
  <header class="a2hd-intro">
    <div class="a2hd-intro-heading">
      <h1>{{ page.title }}</h1>
      <img src="{{ '/images/a2hd%20logo.png' | relative_url }}" alt="" width="720" height="263">
    </div>
    <p>At Lingnan University’s <a href="{{ lab_url }}" target="_self">Adaptive AI &amp; Human Dynamics Lab</a>, we study how people behave and build AI that adapts to their needs in real settings.</p>
  </header>

  <nav class="recruitment-grid recruitment-opportunities" aria-label="Opportunities">
    <a class="recruitment-card recruitment-opportunity" href="#phd-opportunities" target="_self" data-ss-opts='{"excludeWithin":[".recruitment-opportunities"]}'>
      <span class="recruitment-role">
        <span>PhD opportunities</span>
        <span aria-hidden="true">↓</span>
      </span>
      <span>{{ recruitment.phd_opening }}</span>
    </a>
    <a class="recruitment-card recruitment-opportunity" href="#postdoc-opportunities" target="_self" data-ss-opts='{"excludeWithin":[".recruitment-opportunities"]}'>
      <span class="recruitment-role">
        <span>Postdoctoral opportunities</span>
        <span aria-hidden="true">↓</span>
      </span>
      <span>Enquire about current openings</span>
    </a>
  </nav>

  <section class="recruitment-section" aria-labelledby="research-directions">
    <h2 id="research-directions">Research directions</h2>
    <ul class="recruitment-grid" role="list">
      <li class="recruitment-card recruitment-direction">
        <h3>
          <span class="a2hd-panel-marker" aria-hidden="true"><i class="fas fa-users"></i></span>
          <a href="{{ lab_url }}#human-dynamics" target="_self">Human dynamics</a>
        </h3>
        <p>Study speech, movement, and interaction to understand how people’s behaviour and needs change across settings.</p>
      </li>
      <li class="recruitment-card recruitment-direction">
        <h3>
          <span class="a2hd-panel-marker" aria-hidden="true"><i class="fas fa-sliders-h"></i></span>
          <a href="{{ lab_url }}#adaptive-intelligence" target="_self">Adaptive intelligence</a>
        </h3>
        <p>Build AI that adapts to users, tasks, and computing constraints. Explore how language models can draw on relevant knowledge and adjust how much computation they use for each task.</p>
      </li>
      <li class="recruitment-card recruitment-direction">
        <h3>
          <span class="a2hd-panel-marker" aria-hidden="true"><i class="fas fa-clipboard-check"></i></span>
          <a href="{{ lab_url }}#domain-specific-evaluation" target="_self">Domain-specific evaluation</a>
        </h3>
        <p>Work with domain experts to evaluate how AI handles real tasks and difficult cases in areas such as education, mobility, and intelligent services.</p>
      </li>
      <li class="recruitment-card recruitment-direction">
        <h3>
          <span class="a2hd-panel-marker" aria-hidden="true"><i class="fas fa-shield-alt"></i></span>
          <a href="{{ lab_url }}#privacy-and-trust" target="_self">Privacy &amp; trust</a>
        </h3>
        <p>Develop and test ways to protect personal data, verify where models come from, and measure how fairly AI serves different groups.</p>
      </li>
    </ul>
  </section>

  <section class="recruitment-section" aria-labelledby="why-a2hd">
    <h2 id="why-a2hd">Why A2HD?</h2>
    <p id="what-you-can-expect">You’ll receive close mentorship in Lingnan University’s School of Data Science and have access to computing resources and datasets from applied projects. You can shape your own research questions, contribute to funded projects, and develop your work for peer-reviewed publication.</p>
    <p id="selected-strengths">Our work has appeared in ACM TOIS, IEEE TMC, IEEE TKDE, The Web Conference, and IEEE INFOCOM, and has received Best Paper Awards at IEEE INFOCOM and IEEE ICNP. Explore our <a href="{{ '/projects' | relative_url }}" target="_self">projects</a> and <a href="{{ '/publications' | relative_url }}" target="_self">publications</a>.</p>
  </section>

  <section class="recruitment-section" aria-labelledby="phd-opportunities">
    <h2 id="phd-opportunities" tabindex="-1">PhD opportunities</h2>
    <p id="a-good-fit-for-this-position">We welcome applicants who enjoy building systems, connecting machine learning to questions about people and their needs, and carrying a research idea through evaluation and writing.</p>

    <h3 id="what-we-look-for">What we look for</h3>
    <ul>
      <li>A strong undergraduate or master’s background in computer science, data science, artificial intelligence, statistics, or a related field.</li>
      <li>Solid programming skills and experience implementing technical ideas.</li>
      <li>Evidence of research potential through a thesis, publications, internships, competitions, or substantial projects.</li>
      <li>Motivation for sustained research and clear written and spoken English.</li>
    </ul>

    <div class="recruitment-card recruitment-application">
      <h3 id="how-to-apply">How to apply</h3>
      <p>Email Dr. Jiaxing Shen at <a href="mailto:{{ site.author.email }}?subject={{ phd_subject_encoded }}" target="_self">{{ site.author.email }}</a> with the following materials.</p>
      <ol>
        <li>A CV highlighting relevant coursework, research experience, and technical skills.</li>
        <li>Transcripts for all degree programmes, with class ranking if available.</li>
        <li>A one-page statement explaining what you want to investigate and how it fits the lab’s research.</li>
        <li>Representative publications, thesis chapters, or writing samples, if available.</li>
      </ol>
      <p>It helps to use the subject line <strong>{{ phd_subject }}</strong> and include a short paragraph on why you want to join A2HD.</p>
      <p>We may invite shortlisted candidates to discuss research fit. For the formal application, see Lingnan University’s <a href="https://www.ln.edu.hk/rpg/admission/requirement/admission-criteria-and-requirements">eligibility and English-language requirements</a> and <a href="https://www.ln.edu.hk/rpg/admission/application-for-admission">application routes and deadlines</a>.</p>
    </div>
  </section>

  <section class="recruitment-section" aria-labelledby="postdoc-opportunities">
    <h2 id="postdoc-opportunities" tabindex="-1">Postdoctoral opportunities</h2>
    <p>Postdoctoral fellows pursue independent and collaborative research with an emphasis on publication and limited administrative duties.</p>
    <ul>
      <li><strong>Computing.</strong> Access to high-performance computing, including at least eight NVIDIA H100 NVL GPUs with 94 GB of memory each.</li>
      <li><strong>Data.</strong> Mobility datasets for transportation research, automotive repair data for predictive maintenance, and datasets for interdisciplinary projects.</li>
      <li><strong>Remuneration.</strong> Competitive compensation based on qualifications and experience.</li>
    </ul>
    <p>To ask about current openings and research fit, <a href="mailto:{{ site.author.email }}?subject=Postdoctoral%20Enquiry" target="_self">email Dr. Jiaxing Shen</a>.</p>
  </section>
</div>
