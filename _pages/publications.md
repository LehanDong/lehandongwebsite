---
layout: archive
title: "Research Experience"
permalink: /publications/
author_profile: true
---

{% include base_path %}

### 💡Selected Work in Progress
* “Trade Dynamics and Regional Integration under Trump-era Tariffs: Evidence from Hengqin”  with Dr. Chen Huang, Tsinghua University 
* “Seigniorage and Monetary Policy Transmission” with Dr. Chen Huang, Tsinghua University 
* “CRA Enforcement and Racial Equity: Evidence from HMDA Mortgage Approvals” with peers, guided by Prof. Turken, Johns Hopkins University

### 🔬 Research Assistant  
**Tsinghua University, Center for International Finance and Economics**  
*Jun 2024 – Present | Beijing, China*

At Tsinghua, I assist Professors Jiandong Ju and Dr. Chen Huang in research spanning monetary policy, capital flows, and international trade.

***Seigniorage & AI-Based Commentary***
* Structured and cleaned central bank income statement data (FRED & Fed)
* Applied difference-in-differences and machine learning methods to simulate
* Contributes to an AI-driven macroeconomic commentary system.

***U.S.–China Trade Policy***
* Conducted policy impact analysis on U.S. reciprocal tariffs, reviewing papers on trade frictions and firm-level responses. 
* Editing and publishing the *Paper Express* and *Report Study* brief series.

***Capital Account Liberalization***
* Benchmarked capital regimes in Hong Kong, Thailand, and ASEAN, and co-authored internal briefs on cross-border regulatory harmonization.
* Developed policy-facing visualizations using Python and Excel.

### 💹 Poster
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



