---
layout: single
title: "Servizi"
permalink: /servizi/
author_profile: false
classes: wide
---

{%- comment -%} Elenco principale: solo i servizi base (senza campo citta). Le pagine per citta/provincia stanno in /servizi/provincia/<citta>/ e nella sezione "Servizi per provincia" qui sotto. {%- endcomment -%}
{% assign base = site.servizi | where_exp: "s", "s.citta == nil" | sort: "ordine" %}
{% include ex-lista.html items=base vista="riga" cta="Scopri il servizio" %}

## Servizi per provincia

<ul>
<li><a href="{{ '/servizi/provincia/roma/' | relative_url }}">Roma e provincia</a></li>
<li><a href="{{ '/servizi/provincia/viterbo/' | relative_url }}">Viterbo e provincia</a></li>
<li><a href="{{ '/servizi/provincia/rieti/' | relative_url }}">Rieti e provincia</a></li>
<li><a href="{{ '/servizi/provincia/latina/' | relative_url }}">Latina e provincia</a></li>
<li><a href="{{ '/servizi/provincia/frosinone/' | relative_url }}">Frosinone e provincia</a></li>
</ul>
