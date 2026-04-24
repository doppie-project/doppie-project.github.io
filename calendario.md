---
layout: default
title: Calendario
permalink: /calendario/
section_num: "(03)"
heading_main: Coming
heading_italic: soon
subtext: "Stiamo preparando qualcosa di nuovo. Il prossimo capitolo di DOPPIE arriverà presto."
cta_text: Restiamo in contatto
---

<section id="calendario">
    <span class="section-num mono">{{ page.section_num }}</span>
    <h2 class="cs-huge">{{ page.heading_main }} <em>{{ page.heading_italic }}</em><em style="color:var(--black);font-style:normal;">.</em></h2>
    <p class="cs-sub">{{ page.subtext }}</p>
    <a href="{{ '/contatti' | relative_url }}" class="big-link">
        <em>{{ page.cta_text | split: ' ' | last }}</em>
        {{ page.cta_text | split: ' ' | first }} →
    </a>
</section>
