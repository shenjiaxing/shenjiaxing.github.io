---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

I am an Assistant Professor at The Department of Computing and Decision Sciences, Lingnan University. Previously, I was with the Department of Computing, The Hong Kong Polytechnic University as a Research Assistant Professor from 2020 to 2022. 
I obtained B.E. in Software Engineering and Ph.D. in Computer Science from Jilin University in 2014 and The Hong Kong Polytechnic University in 2019, respectively. I was also a visiting scholar at Media Lab, Massachusetts Institute of Technology in 2017. 

My central research theme is Human Dynamics which refers to interdisciplinary research studying human behavior and providing actionable insights. 
Under the theme, I have several research interests including Context Sensing, IoT Systems, Mobile Computing, and Data Mining. 
I have published over 25 papers in top-tier journals and conferences including TMC, TKDE, TOIS, IoT-J, INFOCOM, WWW, ICDM, and ICDCS. 
I have also won Best Paper Award twice including one from INFOCOM 2020. 

<!-- My research interest includes neural machine translation and computer vision. I have published more than 100 papers at the top international AI conferences with total 
<a href='https://scholar.google.com/citations?user=amJMlVoAAAAJ'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=citations"></a>).
 -->

# 🔥 News
- *2022.09*: &nbsp;🎉🎉 I joined The Department of Computing and Decision Sciences, Lingnan University as an Assistant Professor. 
<!-- - *2022.02*: &nbsp;🎉🎉 Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet.  -->

# 📝 Publications 

<div class="bibtex_template">
    <span class="year"></span>
    <div class="if url">
      <a class="bibtexVar" href="+URL+" extra="url">
        <span class="title"></span>
      </a>
    </div>
    <div class="if !url">
      <div class="if doi">
        <a class="bibtexVar" href="http://dx.doi.org/+DOI+" extra="doi">
          <span class="title"></span>
        </a>
      </div>
      <div class="if !doi">
        <a>
          <span class="title"></span>
        </a>
      </div>
    </div> 
    <!-- <span class="if author"> -->
    <span class="author"></span>
    <!-- <span class="title" style="color:blue;"></span> -->
    <span class="journal" style="font-style: italic;"></span>
    <!-- <span class="if BIBTEXTYPEKEY==ARTICLE">Journal</span>
    <span class="if BIBTEXTYPEKEY==PROCEEDINGS">Conference</span> -->
    <br/>
    <br/>
</div>

<!-- <div class="bibtex_structure">
  <div class="group BIBTEXTYPEKEY" extra="DESC string">
    <h2 class="title"><span class="bibtextype"></span></h2>
    <div class="group year" extra="DESC number">
        <h3 class="title"><span class='year'></span></h3>
        <div class="templates">
       </div>
    </div>
  </div>
</div> -->


<div class="bibtex_structure">
  <div class="sections BIBTEXTYPEKEY">
    <div class="section ARTICLE">
      <h2>Refereed Journal</h2>
      <div class="sort year" extra="DESC number">
        <h3 class="title"><span class='year'></span></h3>
        <div class="templates"></div>
      </div>
    </div>
    <div class="section PROCEEDINGS">
      <h2>Conference Papers</h2>
      <div class="sort year" extra="DESC number">
        <h3 class="title"><span class='year'></span></h3>
        <div class="templates"></div>
      </div>
    </div>
    <div class="section misc|phdthesis|mastersthesis|bachelorsthesis|techreport">
      <h2>Other Publications</h2>
      <div class="sort year" extra="DESC number">
        <div class="templates"></div>
      </div>
    </div>
  </div>
</div>

<!-- <div id="bibtex_display">
</div>
 -->

<div id="bibtex_display"></div>

<!-- <div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPR 2016</div><img src='images/500x300.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Deep Residual Learning for Image Recognition](https://openaccess.thecvf.com/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf)

**Kaiming He**, Xiangyu Zhang, Shaoqing Ren, Jian Sun

[**Project**](https://scholar.google.com/citations?view_op=view_citation&hl=zh-CN&user=DhtAFkwAAAAJ&citation_for_view=DhtAFkwAAAAJ:ALROH1vI_8AC) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
</div>
</div>

- [Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet](https://github.com), A, B, C, **CVPR 2020** -->

# 🎖 Honors and Awards
- *2013*, **National Scholarship of China**
- *2016*, **Best Paper Award** of _IEEE International Conferences on Ubiquitous Intelligence & Computing, Advanced and Trusted Computing, Scalable Computing and Communications, Cloud and Big Data Computing, Internet of People, and Smart World Congress_.
- *2020*, **Best Paper Award** of _IEEE International Conference on Computer Communications (INFOCOM)_.

# 📖 Education
- *2010 - 2014*, B.E., Software Engineering, Jilin University, China 
- *2014 - 2019*, Ph.D., Computer Science, The Hong Kong Polytechnic University, Hong Kong
- *2017 - 2018*, visiting Ph.D., Media Lab, Massachusetts Institute of Technology, US


# 👨‍🏫 Teaching
- *2020*, COMP1011 Programming Fundamentals (Undergraduate)
- *2021*, COMP4442 Service and Cloud Computing (Undergraduate)


# 🛎 Service
## Session Chair
- IEEE MASS 2022

## Journal Reviewer
- IEEE Transactions on Mobile Computing
- ACM Computing Surveys
- INFORMS Journal on Computing
- ACM Transactions on Intelligent Systems and Technology
- ACM Transactions on Cyber-Physical Systems
- IEEE Transactions on Big Data

## Conference Reviewer
- IJCAI 
- ICDCS 
- IEEE Percom 
- MOBIQUITOUS 


