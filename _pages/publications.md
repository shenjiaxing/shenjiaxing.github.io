---
permalink: /publications
title: "Publications"
excerpt: ""
author_profile: true
---

<style>
  .publications-layout {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }

  .publications-main {
    min-width: 0;
  }

  .publications-nav {
    order: -1;
  }

  .publications-nav.is-empty {
    display: none;
  }

  .publications-nav .toc {
    position: sticky;
    top: 1rem;
  }

  .publications-nav .toc__menu {
    max-height: calc(100vh - 8rem);
    overflow: auto;
  }

  .publications-nav .toc__menu a.is-active {
    color: #000;
    background: #f3f3f3;
  }

  .publication-year-group + .publication-year-group {
    margin-top: 2.5rem;
  }

  .publication-year-title {
    margin-bottom: 1rem;
  }

  .publication-type-block + .publication-type-block {
    margin-top: 1.5rem;
  }

  .publication-type-heading {
    margin: 0 0 0.75rem;
    padding-bottom: 0.35rem;
    border-bottom: 1px solid #e6e6e6;
    font-size: 1.1rem;
  }

  .publication-entry {
    display: flex;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 0.35rem;
    padding-left: 1em;
    padding-right: 5%;
  }

  .publication-entry + .publication-entry {
    margin-top: 0.9rem;
  }

  .publication-meta {
    display: none;
  }

  @media (min-width: 1100px) {
    .publications-layout {
      display: grid;
      grid-template-columns: minmax(0, 1fr) 13rem;
      gap: 2rem;
      align-items: start;
    }

    .publications-nav {
      order: 0;
    }
  }

  @media (max-width: 1099px) {
    .publications-nav .toc__menu {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      max-height: none;
      overflow: visible;
    }

    .publications-nav .toc__menu li {
      margin: 0;
    }

    .publications-nav .toc__menu a {
      border-bottom: 0;
      border: 1px solid #e6e6e6;
      border-radius: 999px;
      padding: 0.35rem 0.8rem;
    }
  }
</style>

<div class="publications-page">
  <div class="bibtex_template publication-entry">
    <div>
      <div class="if url" style="display: inline-block">
        <a class="bibtexVar" href="+URL+" extra="url">
          <span class="title"></span>
        </a>
      </div>
      <div class="if !url" style="display: inline-block">
        <div class="if doi">
          <a class="bibtexVar" href="http://dx.doi.org/+DOI+" extra="doi">
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
      <span class="if ccf==CCF A"><span class="ccfa">CCF-A</span></span>
      <span class="if ccf==CCF B"><span class="ccfb">CCF-B</span></span>
      <span class="if jcr==JCR Q1"><span class="jcrq1">JCR-Q1</span></span>
      <span class="if note==Best Paper Award"><span class="best_paper">🏆Best Paper</span></span>
      <span class="if note==Best Student Paper Runner-up"><span class="best_paper">Best Student Paper Runner-up</span></span>
    </div>
    <span class="author"></span>.
    <span class="journal" style="font-style: italic;"></span>,
    <span class="year"></span>.
    <span class="publication-meta publication-year year"></span>
    <span class="publication-meta publication-date date"></span>
    <span class="publication-meta publication-type-key bibtextypekey"></span>
  </div>

  <div class="bibtex_structure">
    <div class="sort year" extra="DESC number">
      <div class="templates"></div>
    </div>
  </div>

  <div class="publications-layout">
    <div class="publications-main">
      <div id="bibtex_display" callback="window.organizePublications(this)"></div>
      <p style="color: grey; text-align: right;">*:corresponding author(s) or co-first authors</p>
    </div>

    <aside class="publications-nav sticky is-empty" aria-label="Publication year navigation">
      <nav class="toc">
        <header class="nav__title">Browse Years</header>
        <ul class="toc__menu" id="publications-year-nav"></ul>
      </nav>
    </aside>
  </div>
</div>

<script>
  window.organizePublications = function (bibtexDisplay) {
    var $ = window.jQuery;
    var $display;
    var $nav;
    var $navMenu;
    var $entries;
    var groupsByYear = {};
    var years = [];
    var sectionOrder = [
      { key: "journal", label: "Journal Articles" },
      { key: "conference", label: "Conference Papers" },
      { key: "other", label: "Other Publications" }
    ];

    function yearId(year) {
      return "pub-year-" + String(year).replace(/[^a-zA-Z0-9_-]/g, "-");
    }

    function getYear($entry) {
      var year = $.trim($entry.find(".publication-year").first().text());
      var dateText;
      var match;

      if (year) {
        return year;
      }

      dateText = $.trim($entry.find(".publication-date").first().text());
      match = dateText.match(/(19|20)\d{2}/);
      return match ? match[0] : "Other";
    }

    function getBucket($entry) {
      var typeKey = $.trim($entry.find(".publication-type-key").first().text()).toUpperCase();

      if (typeKey === "ARTICLE") {
        return "journal";
      }

      if (typeKey === "INPROCEEDINGS" || typeKey === "PROCEEDINGS") {
        return "conference";
      }

      return "other";
    }

    function sortYearsDesc(a, b) {
      var aNum = parseInt(a, 10);
      var bNum = parseInt(b, 10);

      if (!isNaN(aNum) && !isNaN(bNum)) {
        return bNum - aNum;
      }

      if (!isNaN(aNum)) {
        return -1;
      }

      if (!isNaN(bNum)) {
        return 1;
      }

      return String(b).localeCompare(String(a));
    }

    function activateTocOnScroll() {
      var headings;
      var linksById = {};
      var observer;

      if (!("IntersectionObserver" in window)) {
        return;
      }

      headings = $display.find(".publication-year-title");
      if (!headings.length) {
        return;
      }

      $navMenu.find("a").each(function () {
        var href = $(this).attr("href");
        if (href && href.charAt(0) === "#") {
          linksById[href.slice(1)] = $(this);
        }
      });

      observer = new window.IntersectionObserver(function (entries) {
        var visibleId = null;

        entries.forEach(function (entry) {
          if (entry.isIntersecting) {
            visibleId = entry.target.id;
          }
        });

        if (!visibleId) {
          return;
        }

        $navMenu.find("a").removeClass("is-active");
        if (linksById[visibleId]) {
          linksById[visibleId].addClass("is-active");
        }
      }, {
        rootMargin: "-20% 0px -65% 0px",
        threshold: 0
      });

      headings.each(function () {
        observer.observe(this);
      });
    }

    if (!$ || !bibtexDisplay) {
      return;
    }

    $display = $(bibtexDisplay);
    $nav = $(".publications-nav").first();
    $navMenu = $("#publications-year-nav");
    $entries = $display.children(".bibtexentry").detach();

    if (!$entries.length) {
      $nav.addClass("is-empty");
      return;
    }

    $display.empty();
    $navMenu.empty();

    $entries.each(function () {
      var $entry = $(this);
      var year = getYear($entry);
      var bucket = getBucket($entry);

      if (!groupsByYear[year]) {
        groupsByYear[year] = {
          journal: [],
          conference: [],
          other: []
        };
        years.push(year);
      }

      groupsByYear[year][bucket].push($entry);
    });

    years.sort(sortYearsDesc);

    years.forEach(function (year) {
      var $section = $("<section>").addClass("publication-year-group");
      var $title = $("<h2>")
        .addClass("anchor publication-year-title")
        .attr("id", yearId(year))
        .text(year);

      $section.append($title);

      sectionOrder.forEach(function (sectionMeta) {
        var entries = groupsByYear[year][sectionMeta.key];
        var $block;
        var $heading;
        var $container;

        if (!entries.length) {
          return;
        }

        $block = $("<div>").addClass("publication-type-block");
        $heading = $("<h3>").addClass("publication-type-heading").text(sectionMeta.label);
        $container = $("<div>").addClass("publication-type-list");

        entries.forEach(function ($entry) {
          $container.append($entry);
        });

        $block.append($heading).append($container);
        $section.append($block);
      });

      $display.append($section);
      $navMenu.append(
        $("<li>").append(
          $("<a>").attr("href", "#" + yearId(year)).text(year)
        )
      );
    });

    $nav.removeClass("is-empty");
    activateTocOnScroll();
  };
</script>
