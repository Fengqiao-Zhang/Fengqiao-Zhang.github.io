---
layout: default
title: "Publications"
permalink: /publications/
---

<section class="section" markdown="1">

Check my [Google Scholar](https://scholar.google.com/citations?user=1cteIHQAAAAJ&hl=en) for the full and up-to-date list of papers. Selected papers below.

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
