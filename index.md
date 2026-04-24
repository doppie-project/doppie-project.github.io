---
layout: default
permalink: /
hero_top_left: Est. MMXXIV
hero_top_center: Collettivo Artistico — Milano / Como
hero_statement_line_1: Un collettivo che fa dialogare
hero_statement_line_2: "<em>arte contemporanea</em> e <em>architettura</em>."
hero_statement_line_3: Due luoghi, due artisti, due storie.
manifesto_text: "Ogni mostra è <em>un incontro</em> — tra spazio e opera, <em>tra materia e vuoto</em>, tra chi abita e chi attraversa."
---

<section id="hero">
    <div class="hero-top">
        <span class="mono ln_"><span class="ln">{{ page.hero_top_left }}</span></span>
        <span class="center mono ln_"><span class="ln delay-1">{{ page.hero_top_center }}</span></span>
        <span class="mono ln_" style="text-align:right;"><span class="ln delay-2">N° {{ site.mostre.size | prepend: '00' | slice: -3, 3 }}</span></span>
    </div>

    {% include hero-logo.html %}

    <div class="hero-bottom">
        <p class="hero-statement">
            <span class="ln_"><span class="ln delay-3">{{ page.hero_statement_line_1 }}</span></span>
            <span class="ln_"><span class="ln delay-4">{{ page.hero_statement_line_2 }}</span></span>
            <span class="ln_"><span class="ln delay-5">{{ page.hero_statement_line_3 }}</span></span>
        </p>
        <div class="hero-action">
            <span class="scroll-cue ln_"><span class="ln delay-5">Scroll to explore</span></span>
        </div>
    </div>
</section>

<section id="manifesto">
    <h2 class="manifesto-text">{{ page.manifesto_text }}</h2>
</section>
