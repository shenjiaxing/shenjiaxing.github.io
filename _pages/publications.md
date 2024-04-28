---
permalink: /publications
title: "Publications"
excerpt: ""
author_profile: true
---

# Publications 
<div class="bibtex_template" style="padding-left: 1em;padding-right: 5%; display: flex;">
    <div>
      <div class="if url" style="display: inline-block">
        <a class="bibtexVar" href="+URL+" extra="url" >
          <span class="title"></span>
        </a>
      </div>
      <div class="if !url" style="display: inline-block">
        <div class="if doi">
          <a class="bibtexVar" href="http://dx.doi.org/+DOI+" extra="doi" >
            <span class="title"></span>
          </a>
        </div>
        <div class="if !doi">
          <a href="">
            <span class="title"></span>
          </a>
        </div>
      </div> 
      <span class="if localpdf">[<a class="bibtexVar" href="/pdf/+LOCALPDF+.pdf" id="+LOCALPDF+" extra="localpdf">PDF</a>]</span>
      <!-- <div style="margin-right:0%; clear: both; float: right;"> -->
        <span class="if ccf==CCF A"><span class="ccfa">CCF-A</span></span>
        <span class="if ccf==CCF B"><span class="ccfb">CCF-B</span></span>
        <!-- <span class="if ccf==CCF C"><span class="ccfc">CCF-C</span></span> -->
        <span class="if jcr==JCR Q1"><span class="jcrq1">JCR-Q1</span></span>
        <!-- <span class="if jcr==JCR Q2"><span class="jcrq2">JCR-Q2</span></span> -->
        <span class="if note==Best Paper Award"><span class="best_paper">Best Paper🎉</span></span>
      <!-- </div> -->
    </div>
    <span class="author"></span>.
    <span class="journal" style="font-style: italic;"></span>,
    <span class="year"></span>.
    <br/>
    <br/>
</div>

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
    <div class="section misc|phdthesis|mastersthesis|bachelorsthesis|techreport|chapter">
      <h2>Other Publications</h2>
      <div class="sort year" extra="DESC number">
        <div class="templates"></div>
      </div>
    </div>
  </div>
</div>

<div id="bibtex_display" style="" ></div>

<p style="color: grey; text-align: right;">*:corresponding author(s) or co-first authors</p>

