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
carousel_caption: Frammenti — Milano / Como
carousel_images:
  - image: /images/uploads/banner_lombracheresta.jpg
  - image: /images/uploads/opening_lombracheresta_spaziomilesi_251023-62.jpg
  - image: /images/uploads/opening_lombracheresta_spaziomilesi_251023-46.jpg
  - image: /images/uploads/mostra_lombracheresta_spaziomilesi_251023-04.jpg
  - image: /images/uploads/banner.png
  - image: /images/uploads/616a8732.jpg
  - image: /images/uploads/7l9a0814.jpg
  - image: /images/uploads/7l9a0944.jpg
  - image: /images/uploads/progetto-senza-titolo.jpg
  - image: /images/uploads/img_0131.jpg
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
