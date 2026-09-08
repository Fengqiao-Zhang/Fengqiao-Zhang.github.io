---
layout: default
permalink: /
---

<section class="section" markdown="1">

<!-- # Hi, I'm Lichao Wu. -->

I am a Lecturer (Assistant Professor) at the University of Bristol, working on hardware security and AI security. Before that, I was a postdoctoral researcher in the System Security Lab at TU Darmstadt, Germany, working with [Prof. Dr.-Ing. Ahmad-Reza Sadeghi](https://www.informatik.tu-darmstadt.de/systemsecurity/people_sys/people_details_sys_45184.en.jsp), and a postdoctoral research fellow at Radboud University, led by [Prof. Dr. Joan Daemen](https://cs.ru.nl/~joan/) and [Prof. Dr. Dr. Stjepan Picek](https://www.ru.nl/en/people/picek-s). I obtained my PhD from TU Delft, the Netherlands, in 2023, supervised by [Prof. Dr. ir. Inald Lagendijk](https://www.tudelft.nl/staff/r.l.lagendijk/) and [Prof. Dr. Dr. Stjepan Picek](https://www.ru.nl/en/people/picek-s).

My research focuses on AI-augmented physical and micro-architectural hardware security, as well as AI security. I have published in top-tier security and cryptography venues, including USENIX Security, NDSS, ASIACRYPT, TCHES, and TDSC. Several of my works have been referenced in [AIS 46 guidance](https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Zertifizierung/Interpretationen/AIS_46_AI_guide.pdf?__blob=publicationFile&v=7) by the German Federal Office for Information Security (BSI), and I have contributed as a main or co-applicant to several EU- and industry-funded projects.

Alongside academia, I worked as a Principal Security Evaluator at SGS Brightsight, the Netherlands (2017–2024), leading CC EAL5+ security evaluations for globally leading IC designers.

I am looking for motivated **PhD students** and **postdoctoral researchers** to join my group — see [Positions](/positions/) for details.

</section>

<section class="section" markdown="1">

## What's new

{% assign pub_news = site.data.publications | sort: "date" | reverse | slice: 0, 5 %}
{% assign serv_news = site.data.service | sort: "date" | reverse | slice: 0, 5 %}
{% assign news = pub_news | concat: serv_news | sort: "date" | reverse | slice: 0, 5 %}
{% for item in news %}
{%- if item.title -%}
- **{{ item.date | replace: "-", "." }}** {% if item.venue == "arxiv" %}[arxiv]{% else %}[**{{ item.venue }}{% if item.award %} — {{ item.award }}{% endif %}**]{% endif %}{% if item.link %} [*"{{ item.title }}"*]({{ item.link }}){% else %} *"{{ item.title }}"*{% endif %}{% if item.status %} ({{ item.status }}){% endif %}.
{%- else -%}
- **{{ item.date | replace: "-", "." }}** {{ item.text }}
{%- endif %}
{% endfor %}

</section>

<!-- <section class="section" markdown="1">

## Awards & recognition

- **2026** NDSS Distinguished Paper Award — *"Fuzzilicon: A Post-Silicon Microcode-Guided x86 CPU Fuzzer"*.
- **2023** Informatics Best PhD Dissertation Award.
- Several works referenced in [AIS 46 guidance](https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Zertifizierung/Interpretationen/AIS_46_AI_guide.pdf?__blob=publicationFile&v=7) by the German Federal Office for Information Security (BSI).

</section> -->

<!-- <section class="section" markdown="1">

## Experience

- **2026–present** Lecturer (Assistant Professor), University of Bristol, UK.
- **2024-2026** Postdoctoral researcher, System Security Lab, TU Darmstadt, Germany.
- **2023-2024** Postdoctoral research fellow, Radboud University, the Netherlands.
- **2019-2023** PhD, TU Delft, the Netherlands — supervised by Prof. Dr. ir. Inald Lagendijk and Prof. Dr. Dr. Stjepan Picek.
- **2017–2024** Principal Security Evaluator, SGS Brightsight, the Netherlands.

</section> -->

<section class="section" markdown="1">

## Research interests

- Hardware security (side-channel analysis, fault injection, hardware fuzzing)
- AI security (LLM safety, adversarial and mixture-of-experts attacks)
- AI-augmented physical and micro-architectural hardware security
- Cross-layer security across hardware and AI systems

</section>
