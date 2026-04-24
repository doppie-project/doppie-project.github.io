---
layout: default
title: Contatti
permalink: /contatti/
section_num: "(04) — Partecipa"
title_main_1: Mettiamoci
title_main_2: in
title_italic: contatto
lead: "Portfolio, donazioni, collaborazioni — <em>scrivici</em>."
form_endpoint: "https://script.google.com/macros/s/AKfycbwSC36DQMW8Td1EG0a0ux0eupHyDkhTyZwunf_zklj6S39xD4K5MbooiQ5Ygc3y2oIo/exec"
---

<section id="contatti">
    <div class="section-head">
        <span class="section-num mono">{{ page.section_num }}</span>
        <h2 class="section-title">{{ page.title_main_1 }}<br>{{ page.title_main_2 }} <em>{{ page.title_italic }}</em>.</h2>
        <p class="section-lead">{{ page.lead }}</p>
    </div>

    <form id="doppie-form" class="form">
        <div class="form-row">
            <label for="email" class="mono">01 / Email</label>
            <input type="email" id="email" name="email" required placeholder="nome@email.com">
        </div>
        <div class="form-row">
            <label for="reason" class="mono">02 / Motivo</label>
            <select id="reason" name="reason" required>
                <option>Richiedi Preview / Portfolio</option>
                <option>Voglio Donare / Supportare</option>
                <option>Collaborazione</option>
                <option>Altro</option>
            </select>
        </div>
        <div class="form-row">
            <label for="message" class="mono">03 / Messaggio</label>
            <textarea id="message" name="message" rows="3" placeholder="Scrivi qui…"></textarea>
        </div>
        <button type="submit" id="submit-btn" class="submit">Invia <em>richiesta</em> →</button>
        <p id="form-status"></p>
    </form>
</section>

<script>
(function(){
    const form = document.getElementById('doppie-form');
    const statusText = document.getElementById('form-status');
    const submitBtn = document.getElementById('submit-btn');
    const scriptURL = '{{ page.form_endpoint }}';

    form.addEventListener('submit', e => {
        e.preventDefault();
        statusText.innerText = "Invio in corso...";
        statusText.style.color = "#7a7a7a";
        submitBtn.disabled = true;
        fetch(scriptURL, { method: 'POST', body: new FormData(form) })
            .then(() => {
                statusText.innerText = "→ Grazie, la tua richiesta è stata inviata.";
                statusText.style.color = "#000";
                form.reset();
                submitBtn.disabled = false;
            })
            .catch(() => {
                statusText.innerText = "Errore. Riprova più tardi.";
                statusText.style.color = "#c00";
                submitBtn.disabled = false;
            });
    });
})();
</script>
