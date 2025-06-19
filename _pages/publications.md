---
layout: page
title: "Research Experience"
permalink: /publications/
author_profile: true
---

{% include base_path %}

Thanks for visiting! Below is a summary of my RA work and academic contributions.

Selected Work in Progress:
* “Trade Dynamics and Regional Integration under Trump-era Tariffs: Evidence from Hengqin”  with Dr. Chen Huang, Tsinghua University 
* “Seigniorage and Monetary Policy Transmission” with Dr. Chen Huang, Tsinghua University 
* “CRA Enforcement and Racial Equity: Evidence from HMDA Mortgage Approvals” with peers, guided by Prof. Turken, Johns Hopkins University

Research Experience:
Tsinghua Unviersity，2024

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}



