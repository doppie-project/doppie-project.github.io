---
layout: default
permalink: /
hero_top_left: Est. MMXXV
hero_top_center: Collettivo — Como / Milano
hero_statement_line_1: Il doppio come dispositivo curatoriale.
hero_statement_line_2: Opere, pensieri e spazi si incontrano tra Como e Milano,
hero_statement_line_3: <em> tra chi abita e chi attraversa <em>
scroll_cue_text: Scroll to explore
carousel_caption: Frammenti — Como / Milano
carousel_images:
  - image: /images/uploads/14.jpg
  - image: /images/uploads/img_4912.jpg
  - image: /images/uploads/009-cdf5-iparisi.tiff.tif
  - image: /images/uploads/img_0778-2.jpg
  - image: /images/uploads/19.jpg
  - image: /images/uploads/6.jpg
  - image: /images/uploads/001-cdf5-iparisi.tiff.jpg
  - image: /images/uploads/14.jpg
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

<section id="carousel">
    {% if page.carousel_caption %}
    <div class="carousel-head">
        <span class="mono">{{ page.carousel_caption }}</span>
        <span class="mono carousel-hint">Scroll →</span>
    </div>
    {% endif %}
    {% comment %} Images are managed from the CMS (Homepage → Carosello immagini). {% endcomment %}
    <div class="carousel-track">
        {% for slide in page.carousel_images %}
            {% if slide.image %}
            <figure class="carousel-slide">
                <img src="{{ slide.image | relative_url }}" alt="{{ slide.alt | default: 'DOPPIE' }}" loading="lazy">
            </figure>
            {% endif %}
        {% endfor %}
    </div>
</section>
