---
layout: page
title: research
permalink: /research/
description:
nav: true
nav_order: 3
display_categories: [work, fun]
horizontal: false
---

I work at the intersection of theory and observations in astrophysics. Most of my work has focused on understanding the formation and evolution of galaxies in the early universe, including those formed just a few hundred million years after the Big Bang, their connections to the dark matter halos they form in, and their relationship to the reionization of intergalactic hydrogen in the universe's first billion years. I typically combine empirical and semi-analytical theoretical modelling with statistical analyses of observations to ask what our frontier observations of galaxies tell us about the early universe. For more details see the themes below and [my papers on ADS](https://ui.adsabs.harvard.edu/search/filter_author_facet_hier_fq_author=NOT&filter_author_facet_hier_fq_author=*%3A*&filter_author_facet_hier_fq_author=author_facet_hier%3A%221%2FMason%2C%20C%2FMason%2C%20Christopher%20E%22&fq=%7B!type%3Daqp%20v%3D%24fq_database%7D&fq=%7B!type%3Daqp%20v%3D%24fq_bibstem_facet%7D&fq=%7B!type%3Daqp%20v%3D%24fq_author%7D&fq_author=(*%3A*%20NOT%20author_facet_hier%3A%221%2FMason%2C%20C%2FMason%2C%20Christopher%20E%22)&fq_bibstem_facet=(((((*%3A*%20NOT%20bibstem_facet%3A%22E%26PSL%22%20NOT%20bibstem_facet%3A%22LPICo%22%20NOT%20bibstem_facet%3A%22ESASP%22)%20NOT%20bibstem_facet%3A%22cosp%22%20NOT%20bibstem_facet%3A%22LPI%22)%20NOT%20bibstem_facet%3A%22JDSO%22)%20NOT%20bibstem_facet%3A%22NewSp%22)%20NOT%20bibstem_facet%3A%22IJAsB%22%20NOT%20bibstem_facet%3A%22IMAFu%22)&fq_database=((database%3A%22astronomy%22)%20NOT%20database%3A%22earthscience%22)&p_=0&q=author%3A%22mason%2C%20c%22%20year%3A2011-2099&sort=date%20desc%2C%20bibcode%20desc){:target="\_blank"} or my [CV](/assets/pdf/CV-CharlotteMason.pdf).

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
