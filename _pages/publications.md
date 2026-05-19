---
layout: page
permalink: /publications/
title: Publications
description:
nav: true
nav_order: 2
---

<style>
  .publications ol.bibliography li {
    margin-bottom: 1.75rem;
    padding-bottom: 1.5rem;
    border-bottom: 1px solid var(--global-divider-color, #eee);
  }
  .publications ol.bibliography li:last-child { border-bottom: none; }
  .publications .title {
    font-size: 1.05rem;
    line-height: 1.35;
    margin-bottom: 0.5rem;
  }
  .publications .author {
    line-height: 1.65;
    margin-bottom: 0.5rem;
  }
  /* One underline only: keep italic for FarSight authors, override al-folio's
     border-bottom on .author > em so we don't get two underlines. */
  .publications .author > em.farsight-author {
    font-style: italic;
    border-bottom: none;
    text-decoration: underline;
    text-underline-offset: 2px;
    text-decoration-thickness: 1px;
  }
  .publications .periodical {
    line-height: 1.55;
    margin-bottom: 0.3rem;
  }
  .publications .links { margin-top: 0.55rem; }
  /* Award / highlight / oral / spotlight indicators */
  .publications .award-tag {
    color: #c0392b;
    font-weight: 700;
  }
  html[data-theme="dark"] .publications .award-tag {
    color: #ff6b5e;
  }
  .publications h2.pub-section {
    font-size: 1.1rem;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--global-text-color-light, #828282);
    margin-top: 2.25rem;
    margin-bottom: 1rem;
    padding-bottom: 0.5rem;
    border-bottom: 1px solid var(--global-divider-color, #eee);
    font-weight: 600;
  }
</style>

<!-- Bibsearch -->
{% include bib_search.liquid %}

<h2 class="pub-section">Preprints</h2>

<div class="publications">
{% bibliography --file preprints %}
</div>

<h2 class="pub-section">Publications</h2>

<div class="publications">
{% bibliography --file papers %}
</div>
