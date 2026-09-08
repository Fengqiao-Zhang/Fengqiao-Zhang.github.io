---
layout: default
title: "Research"
permalink: /research/
---

<section class="section" markdown="1">

## Scalable monitoring of localized corrosion in concrete bridges 
- 2027-2031
- Funding Source: Dutch Research Council (NWO) VENI(https://www.nwo.nl/en/researchprogrammes/nwo-talent-programme/projects-veni/veni-2025)
- With concrete responsible for 4–8% of global carbon emissions, extending the service life of existing infrastructure, rather than building new, is a key strategy. To do this safely, we need reliable safety assessments of ageing structures. This is difficult because deterioration such as localized corrosion develops randomly in space and can have serious safety consequences. This research will develop a scalable, adaptive, and reliable monitoring approach that reveals the spatial pattern of such deterioration and its structural safety relevance, enabling safe extension of structural service life.
</section>

<section class="section" markdown="1">
  
## Inspection and assessment of half-joint concrete bridges
- 2026-2030
- Funding source: Dutch Ministry of Transportation and Water Management
- Many existing concrete bridges contain half-joint (dapped-end) connections, a structural detail known to be vulnerable due to poor reinforcement detailing, cracking, and corrosion. The effect of these deficiencies is hard to be captured by the current analytical and FEM models. As a result, ensuring the safety of these structures is a priority for many countries. This research will combine advanced Non-Destructive Testing (NDT) methods with structural degradation models to assess the structural safety of half-joint concrete bridges.
</section>

<section class="section" markdown="1">
  
## Previous research
Check my [Google Scholar](https://scholar.google.com/citations?hl=en&user=xBCA5c4AAAAJ&view_op=list_works&sortby=pubdate) for the full and up-to-date list of papers. Selected papers below.

{% assign pubs_by_year = site.data.publications | group_by: "year" %}
{% assign recent_years = pubs_by_year | slice: 0, 3 %}
{% assign earlier_pubs = pubs_by_year | slice: 3, pubs_by_year.size %}

{% for group in recent_years %}
<details class="collapsible"{% if forloop.first %} open{% endif %}>
<summary>{{ group.name }}</summary>
<ul class="pubs">
{% for pub in group.items %}
<li class="pub">
<span class="venue{% if pub.award %} award{% endif %}">{% if pub.venue == "arxiv" %}arXiv{% else %}{{ pub.venue }}{% if pub.award %} — {{ pub.award }}{% endif %}{% endif %}</span>
{%- if pub.link %}<a class="title-paper" href="{{ pub.link }}">{{ pub.title }}</a>{% else %}<span class="title-paper">{{ pub.title }}</span>{% endif -%}
{%- if pub.status %} <span class="status">({{ pub.status }})</span>{% endif %}
<span class="authors">{{ pub.authors | replace: "Lichao Wu", '<span class="me">Lichao Wu</span>' }}.</span>
</li>
{% endfor %}
</ul>
</details>
{% endfor %}

{% if earlier_pubs.size > 0 %}
<details class="collapsible">
<summary>{{ earlier_pubs | first | map: "name" | first }} and earlier</summary>
<ul class="pubs">
{% for group in earlier_pubs %}
{% for pub in group.items %}
<li class="pub">
<span class="venue{% if pub.award %} award{% endif %}">{% if pub.venue == "arxiv" %}arXiv{% else %}{{ pub.venue }}{% if pub.award %} — {{ pub.award }}{% endif %}{% endif %}</span>
{%- if pub.link %}<a class="title-paper" href="{{ pub.link }}">{{ pub.title }}</a>{% else %}<span class="title-paper">{{ pub.title }}</span>{% endif -%}
{%- if pub.status %} <span class="status">({{ pub.status }})</span>{% endif %}
<span class="authors">{{ pub.authors | replace: "Lichao Wu", '<span class="me">Lichao Wu</span>' }}.</span>
</li>
{% endfor %}
{% endfor %}
</ul>
</details>
{% endif %}

</section>
