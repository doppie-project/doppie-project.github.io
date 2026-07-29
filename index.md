---
layout: default
permalink: /
hero_top_left: Est. MMXXV
hero_top_center: Collettivo — Milano / Como
hero_statement_line_1: Il doppio come dispositivo curatoriale.
hero_statement_line_2: Ogni incontro è <em>un sistema critico e sensibile</em>
  dove opere, pensieri e ambienti costruiscono nuove possibilità di esperienza
  collettiva,
hero_statement_line_3: " <em>creando un ponte tra la città di Milano e la città
  di Como</em>, tra chi abita e chi attraversa."
scroll_cue_text: Scroll to explore
manifesto_text: >
  "Abitare significa lasciare tracce. Nell’intèriur queste tracce vengono messe
  in rilievo" Walter Benjamin
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
            <span class="scroll-cue ln_"><span class="ln delay-5">{{ page.scroll_cue_text }}</span></span>
        </div>
    </div>
</section>

<section id="manifesto">
    <h2 class="manifesto-text">{{ page.manifesto_text }}</h2>
</section>
