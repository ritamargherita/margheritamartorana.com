---
layout: page
title: Publications
permalink: /publications/
---

<div class="publication-page">
  <p class="publication-page__intro"><a href="https://scholar.google.com/citations?user=_ba0GhwAAAAJ&hl=en&oi=ao" target="_blank" rel="noopener noreferrer">View Google Scholar profile -&gt;</a></p>
  <div class="publication-list">
    {% assign publications = site.data.publications | sort: "year" | reverse %}
    {% for publication in publications %}
      <article class="publication-item">
        <div>
          <h2>{{ publication.title }}</h2>
          <p>{{ publication.authors }} / {{ publication.venue }} / {{ publication.year }}</p>
        </div>
        <div class="publication-links" aria-label="Publication links">
          {% if publication.doi %}
            <a href="{{ publication.doi }}">DOI</a>
          {% endif %}
          {% if publication.pdf %}
            <a href="{{ publication.pdf }}">PDF</a>
          {% endif %}
          {% if publication.code %}
            <a href="{{ publication.code }}">Code</a>
          {% endif %}
          {% if publication.url %}
            <a href="{{ publication.url }}">Publication</a>
          {% endif %}
        </div>
      </article>
    {% endfor %}
  </div>
</div>
