---
permalink: /publications
title: "Publications"
excerpt: ""
author_profile: true
---

<style>
  #bibtex_display .publication-year-group + .publication-year-group {
    margin-top: 1.5rem;
  }

  #bibtex_display .publication-year {
    margin: 0 0 0.75rem;
    font-weight: 700;
  }

  #bibtex_display .conference-title-link,
  #bibtex_display .conference-title-link:visited {
    color: #2e8b57 !important;
  }

  #bibtex_display .conference-title-link:hover,
  #bibtex_display .conference-title-link:focus {
    color: #246b43 !important;
  }
</style>

<script>
  function rebuildPublicationList(root) {
    var entries = Array.from(root.querySelectorAll('.bibtexentry'));
    if (!entries.length) return;

    var typePriority = {
      ARTICLE: 0,
      PROCEEDINGS: 1,
      INPROCEEDINGS: 1
    };

    var groupedByYear = new Map();

    entries.forEach(function(entry, index) {
      var yearNode = entry.querySelector('.year');
      var typeNode = entry.querySelector('.bibtextypekey');
      var year = yearNode ? yearNode.textContent.trim() : 'Other';
      var type = typeNode ? typeNode.textContent.trim().toUpperCase() : '';

      entry.classList.remove('journal-entry', 'conference-entry', 'other-entry');

      if (type === 'ARTICLE') {
        entry.classList.add('journal-entry');
      } else if (type === 'PROCEEDINGS' || type === 'INPROCEEDINGS') {
        entry.classList.add('conference-entry');
        var title = entry.querySelector('.title');
        if (title && title.parentElement && title.parentElement.tagName.toLowerCase() === 'a') {
          title.parentElement.classList.add('conference-title-link');
        }
      } else {
        entry.classList.add('other-entry');
      }

      if (!year) {
        year = 'Other';
      }

      if (!groupedByYear.has(year)) {
        groupedByYear.set(year, []);
      }

      groupedByYear.get(year).push({
        entry: entry,
        index: index,
        priority: Object.prototype.hasOwnProperty.call(typePriority, type) ? typePriority[type] : 2
      });
    });

    var yearOrder = Array.from(groupedByYear.keys()).sort(function(a, b) {
      if (a === 'Other') return 1;
      if (b === 'Other') return -1;
      return Number(b) - Number(a);
    });

    var fragment = document.createDocumentFragment();

    yearOrder.forEach(function(year) {
      var section = document.createElement('section');
      section.className = 'publication-year-group';

      var heading = document.createElement('h2');
      heading.className = 'publication-year';
      heading.textContent = year;
      section.appendChild(heading);

      groupedByYear.get(year)
        .sort(function(left, right) {
          return left.priority - right.priority || left.index - right.index;
        })
        .forEach(function(item) {
          section.appendChild(item.entry);
        });

      fragment.appendChild(section);
    });

    root.innerHTML = '';
    root.appendChild(fragment);
  }
</script>

<!-- # Publications  -->
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
        <span class="if note==Best Paper Award"><span class="best_paper">🏆Best Paper</span></span>
        <span class="if note==Best Student Paper Runner-up"><span class="best_paper">Best Student Paper Runner-up</span></span>
      <!-- </div> -->
    </div>
    <span class="author"></span>.
    <span class="journal" style="font-style: italic;"></span>,
    <span class="year"></span>.
    <span class="bibtextypekey" style="display:none;"></span>
    <br/>
    <br/>
</div>

<div class="bibtex_structure">
  <div class="sections BIBTEXTYPEKEY">
    <div class="section ARTICLE">
      <div class="sort year" extra="DESC number">
        <h3 class="title"><span class='year'></span></h3>
        <div class="templates"></div>
      </div>
    </div>
    <div class="section PROCEEDINGS">
      <div class="sort year" extra="DESC number">
        <h3 class="title"><span class='year'></span></h3>
        <div class="templates"></div>
      </div>
    </div>
    <div class="section misc|phdthesis|mastersthesis|bachelorsthesis|techreport|chapter">
      <div class="sort year" extra="DESC number">
        <div class="templates"></div>
      </div>
    </div>
  </div>
</div>

<div id="bibtex_display" callback="rebuildPublicationList(bibtex_display);"></div>

<p style="color: grey; text-align: right;">*:corresponding author(s) or co-first authors</p>
