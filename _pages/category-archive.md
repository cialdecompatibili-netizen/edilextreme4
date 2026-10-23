---
title: "Categorie"
layout: single
permalink: /categorie/
author_profile: false
classes: wide
---

<style>
.cg-sec{margin:0 0 2.5rem}
.cg-head h2{margin:0 0 .25rem !important;text-transform:capitalize;font-size:1.6rem}
.cg-head p{margin:0 0 1.1rem !important;color:#666;max-width:46rem}
/* lista leggera: miniatura piccola a sinistra, testo a destra */
.cg-sec .exr{gap:.75rem;max-width:none}
.cg-sec .exr-i{grid-template-columns:minmax(0,240px) minmax(0,1fr);gap:1.25rem;padding:.6rem;box-shadow:none}
.cg-sec .exr-i:hover{box-shadow:0 4px 14px rgba(0,0,0,.07)}
.cg-sec .exr-t{font-size:1.15rem}
.cg-sec .exr-d{font-size:.95rem}
@media(max-width:760px){.cg-sec .exr-i{grid-template-columns:1fr;gap:.75rem}}
</style>

{% assign cats = site.categories | sort %}
{% for cat in cats %}
{% assign cat_data = site.data.categorie | where: "nome", cat[0] | first %}
{% assign items = cat[1] | sort: "ordine" %}
<section class="cg-sec" id="{{ cat[0] | slugify }}">
  <div class="cg-head">
    <h2>{{ cat[0] }}</h2>
    {% if cat_data.descrizione and cat_data.descrizione != "" %}<p>{{ cat_data.descrizione | strip_html }}</p>{% endif %}
  </div>
  {% include ex-lista.html items=items vista="riga" thumb=true cta="Scopri" %}
</section>
{% endfor %}
