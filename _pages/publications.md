---
layout: archive
title: "Research Experience"
permalink: /publications/
author_profile: true
---
<style>
.page__content {
  font-size: 17px;
  line-height: 1.8;
}
.page__content p {
  margin-bottom: 1.2em;
}
</style>

{% include base_path %}

### Selected Work in Progress:
* “Trade Dynamics and Regional Integration under Trump-era Tariffs: Evidence from Hengqin”  with Dr. Chen Huang, Tsinghua University 
* “Seigniorage and Monetary Policy Transmission” with Dr. Chen Huang, Tsinghua University 
* “CRA Enforcement and Racial Equity: Evidence from HMDA Mortgage Approvals” with peers, guided by Prof. Turken, Johns Hopkins University

### Research Experience:
Research Assistant – Tsinghua University, Center for International Finance and Economics  
*Jun 2024 – Present*
*Advised by Prof. Jiandong Ju & Dr. Chen Huang (International Trade, Capital Flows, AI Economics)*

---
Seigniorage & AI Research  
- Cleaned and organized central bank income statements (FRED & Fed Board) to support seigniorage modeling  
- Applied difference-in-differences and machine learning to simulate behavioral responses to monetary policy  
- Contributed to an AI-driven economic commentary system by aligning monetary, trade, and AI research teams
---
Trade Policy  
- Evaluated the short- and long-term effects of U.S. reciprocal tariffs on exchange rate volatility and equity markets  
- Synthesized insights from academic papers on trade friction, export response, and firm adaptation  
- Led editing and publication for *Paper Express* and *Report Study* research brief series  
---
Capital Market Policy – Hengqin Project  
- Conducted multi-country benchmarking (Hong Kong, Thailand, ASEAN) on capital account openness  
- Drafted strategic recommendations for phased capital account reform and regulatory harmonization  
- Produced **policy-facing visualizations** and internal briefs using Python and Excel to communicate capital flow bottlenecks and risks


### Poster
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



