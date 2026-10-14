---
layout: single
title: "Servizi"
permalink: /servizi/
author_profile: false
classes: wide
---

{% assign svc = site.servizi | sort: "ordine" %}
{% for s in svc %}
- **[{{ s.title }}]({{ s.url | relative_url }})** — {{ s.description | default: s.excerpt | strip_html | strip | truncatewords: 25 }}
{% endfor %}
