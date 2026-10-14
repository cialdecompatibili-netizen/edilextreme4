---
layout: single
title: "Lavori svolti"
permalink: /progetti/
author_profile: false
classes: wide
---

{% assign prj = site.progetti | sort: "importance" %}
{% for p in prj %}
- **[{{ p.title }}]({{ p.url | relative_url }})** — {{ p.description | default: p.excerpt | strip_html | strip | truncatewords: 25 }}
{% endfor %}
