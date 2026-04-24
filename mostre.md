---
layout: default
title: Mostre
permalink: /mostre/
section_num: "(02) — Archivio"
title_main: Mostre
lead: "Un dialogo tra <em>arte contemporanea</em> e <em>spazio architettonico</em>, costruito una mostra alla volta."
---

<section id="mostre">
    <div class="section-head">
        <span class="section-num mono">{{ page.section_num }}</span>
        <h2 class="section-title">{{ page.title_main }}<em>.</em></h2>
        <p class="section-lead">{{ page.lead }}</p>
    </div>

    {% assign mostre = site.mostre | sort: 'order' %}
    {% for mostra in mostre %}
        {% include mostra.html mostra=mostra index=forloop.index %}
    {% endfor %}
</section>
