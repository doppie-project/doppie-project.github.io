---
layout: default
title: Chi Siamo
permalink: /chi-siamo/
section_num: "(01) — Il Collettivo"
title_main: Chi
title_italic_line: siamo
lead: "Quattro sguardi. Una visione condivisa. Un dialogo continuo tra <em>curatela, architettura</em> e <em>pratica artistica contemporanea</em>."
---

<section id="chi-siamo">
    <div class="section-head">
        <span class="section-num mono">{{ page.section_num }}</span>
        <h2 class="section-title">{{ page.title_main }}<br>{{ page.title_italic_line }}<em>.</em></h2>
        <p class="section-lead">{{ page.lead }}</p>
    </div>

    <div class="team-grid">
        {% assign members = site.team | sort: 'order' %}
        {% for member in members %}
        <article class="team-card{% if forloop.index0 | modulo: 2 == 1 %} offset{% endif %}">
            <div class="team-photo">
                {% if member.photo %}
                    <img src="{{ member.photo | relative_url }}" alt="{{ member.name }}" loading="lazy">
                {% else %}
                    <img src="https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?q=80&w=2400&auto=format&fit=crop" alt="{{ member.name }}" loading="lazy">
                {% endif %}
            </div>
            <div class="team-info">
                <span class="mono team-num">— {{ forloop.index | prepend: '0' | slice: -2, 2 }} / {{ forloop.length | prepend: '0' | slice: -2, 2 }}</span>
                <h3>{{ member.name | newline_to_br }}</h3>
                <span class="team-role">{{ member.role }}</span>
                {% if member.bio %}<p class="team-bio">{{ member.bio }}</p>{% endif %}
                <div class="team-links">
                    {% if member.email %}<a href="mailto:{{ member.email }}">Email →</a>{% endif %}
                    {% if member.social_link %}<a href="{{ member.social_link }}" target="_blank" rel="noopener">{{ member.social_label | default: 'Instagram' }} →</a>{% endif %}
                </div>
            </div>
        </article>
        {% endfor %}
    </div>
</section>
