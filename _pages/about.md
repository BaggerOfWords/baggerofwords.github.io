---
layout: home
title: "Matthieu Dubois"
permalink: /
author_profile: true
---

My name is Matthieu Dubois, I am a Doctoral Candidate at the ISIR lab of Sorbonne Université in Paris, working on Natural Language Processing. My research subject is centered around Artificial Texts, texts produced by Large Language Models. My first works deal with detecting those, but my interest is piqued by anything related to text generation, such as diversity or model idiosyncracies.

<!-- ===== Recent Publications ===== -->
## Recent Publications
{%- assign pubs = site.publications | sort: 'date' | reverse | slice: 0, 3 -%}
{%- if pubs.size > 0 -%}
<ul>
{%- for pub in pubs -%}
  <li>
    <a href="{{ pub.url | relative_url }}">{{ pub.title }}</a>
    {%- if pub.venue %} — <em>{{ pub.venue }}</em>{% endif %}
    {%- if pub.date %} ({{ pub.date | date: "%Y" }}){% endif %}
    {%- if pub.authors %}<br/><small>{{ pub.authors }}</small>{% endif %}
  </li>
{%- endfor -%}
</ul>
<p><a href="{{ '/publications/' | relative_url }}">View all publications →</a></p>
{%- else -%}
<p>No publications yet.</p>
{%- endif -%}

<!-- ===== Recent Talks ===== -->
## Recent Talks
{%- assign talks = site.talks | sort: 'date' | reverse | slice: 0, 3 -%}
{%- if talks.size > 0 -%}
<ul>
{%- for talk in talks -%}
  <li>
    <a href="{{ talk.url | relative_url }}">{{ talk.title }}</a>
    {%- if talk.event or talk.venue %} — <em>{{ talk.event | default: talk.venue }}</em>{% endif %}
    {%- if talk.date %} ({{ talk.date | date: "%b %Y" }}){% endif %}
    {%- if talk.location %}<br/><small>{{ talk.location }}</small>{% endif %}
  </li>
{%- endfor -%}
</ul>
<p><a href="{{ '/talks/' | relative_url }}">View all talks →</a></p>
{%- else -%}
<p>No talks yet.</p>
{%- endif -%}
