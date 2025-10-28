---
layout: archive
title: "Matthieu Dubois"
permalink: /
author_profile: true
---

My name is Matthieu Dubois, I am a Doctoral Candidate at the ISIR lab of Sorbonne Université in Paris, working on Natural Language Processing. My research subject is centered around Artificial Texts, texts produced by Large Language Models. My first works deal with detecting those, but my interest is piqued by anything related to text generation, such as diversity or model idiosyncracies.


## Recent Publications
{% assign pubs = site.publications | sort: 'date' | reverse | slice: 0, 3 %}
{% if pubs.size > 0 %}
{% for pub in pubs %}
- [{{ pub.title }}]({{ pub.url | relative_url }}){% if pub.venue %} — *{{ pub.venue }}*{% endif %}{% if pub.date %} ({{ pub.date | date: "%Y" }}){% endif %}{% if pub.authors %}<br/><small>{{ pub.authors }}</small>{% endif %}
{% endfor %}
[View all publications →]({{ '/publications/' | relative_url }})
{% else %}
_No publications yet._
{% endif %}

## Recent Talks
{% assign talks = site.talks | sort: 'date' | reverse | slice: 0, 3 %}
{% if talks.size > 0 %}
{% for talk in talks %}
- [{{ talk.title }}]({{ talk.url | relative_url }}){% if talk.event or talk.venue %} — *{{ talk.event | default: talk.venue }}*{% endif %}{% if talk.date %} ({{ talk.date | date: "%b %Y" }}){% endif %}{% if talk.location %}<br/><small>{{ talk.location }}</small>{% endif %}
{% endfor %}
[View all talks →]({{ '/talks/' | relative_url }})
{% else %}
_No talks yet._
{% endif %}
