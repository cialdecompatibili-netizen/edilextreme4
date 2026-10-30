---
layout: single
title: "Servizi a Rieti e provincia"
permalink: /servizi/provincia/rieti/
description: "Tutti i servizi su fune a Rieti e provincia: pulizia vetri, grondaie, tetti, facciate e altro. Sopralluogo e preventivo gratuito."
seo_title: "Servizi su fune a Rieti e provincia | EdilExtreme"
seo_description: "Pulizia vetri, grondaie, tetti, facciate, potatura e altri lavori su fune a Rieti e provincia, senza ponteggi. Sopralluogo e preventivo gratuito."
author_profile: false
classes: wide
---

{%- assign pg = site.servizi | where: "citta", "Rieti" | sort: "title" -%}
{%- assign vetri = pg | where_exp: "s", "s.slug contains 'pulizia-vetri'" -%}

Lavoriamo a **Rieti e in tutta la provincia**, su fune e senza ponteggi. Scegli il servizio che ti serve, oppure mandaci su WhatsApp due foto e l'indirizzo: ti diciamo se serve un sopralluogo e ti diamo un preventivo gratuito.

<ul>
{%- for s in vetri %}
<li><a href="{{ s.url | relative_url }}">{{ s.title }}</a></li>
{%- endfor %}
{%- for s in pg %}{%- unless s.slug contains 'pulizia-vetri' %}
<li><a href="{{ s.url | relative_url }}">{{ s.title }}</a></li>
{%- endunless %}{%- endfor %}
</ul>

[Tutti i servizi]({{ '/servizi/' | relative_url }})