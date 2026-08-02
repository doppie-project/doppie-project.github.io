---
layout: default
title: Testi
permalink: /testi/
section_num: (03) — Testi
title_main: Testi
lead: "Testi d'intervista, materiali e pubblicazioni da sfogliare e scaricare in PDF."
---

<section id="fanzine">
    <div class="section-head">
        <span class="section-num mono">{{ page.section_num }}</span>
        <h2 class="section-title">{{ page.title_main }}<em>.</em></h2>
        <p class="section-lead">{{ page.lead }}</p>
    </div>

    {% assign items = site.testi | sort: 'date' | reverse %}
    {% if items.size > 0 %}
    <div class="fanzine-list">
        {% for item in items %}
        <article class="fanzine-item">
            {% if item.cover_image %}
                <img class="fanzine-cover" src="{{ item.cover_image | relative_url }}" alt="{{ item.title }}" loading="lazy">
            {% else %}
                <span class="fanzine-num mono">{{ forloop.index | prepend: '0' | slice: -2, 2 }}</span>
            {% endif %}
            <div class="fanzine-main">
                <h3 class="fanzine-title">{{ item.title }}</h3>
                {% if item.date or item.category %}
                <span class="fanzine-meta">
                    {%- if item.category %}{{ item.category }}{% endif -%}
                    {%- if item.date and item.category %} — {% endif -%}
                    {%- if item.date %}{{ item.date | date: "%Y" }}{% endif -%}
                </span>
                {% endif %}
                {% if item.description %}<p class="fanzine-desc">{{ item.description }}</p>{% endif %}
            </div>
            {% if item.pdf %}
                <a class="fanzine-download" href="{{ item.pdf | relative_url }}" target="_blank" rel="noopener" download>Scarica PDF ↓</a>
            {% endif %}
        </article>
        {% endfor %}
    </div>
    {% else %}
    <p class="fanzine-empty">Presto disponibili — le pubblicazioni verranno caricate a breve.</p>
    {% endif %}
</section>
