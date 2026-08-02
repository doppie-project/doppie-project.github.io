# DOPPIE Project — Website

Sito ufficiale di **DOPPIE**, collettivo artistico.
Live su: [doppie-website.netlify.app](https://doppie-website.netlify.app)

---

# 🍕PER IL TEAM — INIZIA DA QUI

> **Questa è la tua sezione.** Tutto quello che devi sapere per modificare il sito è qui sotto. **Non leggere la parte in inglese più in basso — è solo per l'admin tecnico.**

Ciao! Se sei qui per aggiungere una mostra, modificare la tua bio o cambiare un testo del sito, **non serve sapere niente di codice**. Vai direttamente alla sezione che ti serve:

- [Come accedere al CMS](#-come-accedere-al-cms)
- [Come aggiungere una nuova mostra](#-come-aggiungere-una-nuova-mostra)
- [Come modificare il tuo profilo del team](#-come-modificare-il-tuo-profilo-del-team)
- [Come modificare i testi delle pagine](#-come-modificare-i-testi-delle-pagine)
- [Cose da sapere prima di pubblicare](#-cose-da-sapere-prima-di-pubblicare)
- [Se qualcosa non funziona](#-se-qualcosa-non-funziona)

---

## 🔑 Come accedere al CMS

1. Vai su [doppie-website.netlify.app/admin/](https://doppie-website.netlify.app/admin/)
2. Clicca **Login with Netlify Identity**
3. Usa l'email a cui hai ricevuto l'invito + la tua password

**Hai dimenticato la password?** Clicca **Forgot password?** sulla schermata di login.

**Non hai mai ricevuto l'invito?** Chiedi all'admin del sito di invitarti tramite Netlify.

---

## 🖼️ Come aggiungere una nuova mostra

Una volta fatto il login, vedrai una barra laterale con queste sezioni:
- **Pagine del Sito** — testi modificabili di ogni pagina
- **Team (Chi Siamo)** — profili dei membri del team
- **Mostre** — tutte le mostre

### Passo per passo

1. Clicca **Mostre** nella sidebar → **New Mostra** (in alto a destra)
2. Compila i campi:

| Campo | Cosa scrivere | Esempio |
|---|---|---|
| **Titolo (prima parte)** | Prima parola del titolo | `Sentimento` |
| **Titolo (parte in corsivo)** | Seconda parola — apparirà in corsivo grigio | `carsico` |
| **Anno** | Anno della mostra | `2025` |
| **Ordine di visualizzazione** | 1 = prima mostra mostrata. Le mostre più nuove di solito vanno per prime | `1` |
| **Status** | Menu a tendina | `Concluso`, `In corso`, o `Prossimo` |
| **Luogo completo** | Indirizzo completo della sede | `Spazio Milesi, Milano` |
| **Luogo breve** | Solo la città — apparirà come tag sull'immagine | `Milano` |
| **Curatela** | Nomi dei curatori, uno per riga | `Attilio A. Terragni` |
| **Immagine principale** | L'immagine grande di copertina. Click Upload e scegli una foto | (upload) |
| **Descrizione** | Paragrafo lungo sulla mostra | (testo libero) |

3. Scorri a **Artisti** → clicca **Add Artista** per ogni artista. Compila:
   - **Nome** e **Cognome**
   - **Origine** (es. `Milano, 1995`)
   - **Biografia** (paragrafo breve)
4. Dentro l'artista → clicca **Add Opera** per ogni opera:
   - **Immagine** → carica la foto dell'opera
   - **Titolo dell'opera** (es. `Eclisse`)
   - **Anno** (es. `2020`)
   - **Descrizione dell'opera** (facoltativa)
5. Clicca **Save** quante volte vuoi mentre stai lavorando — niente va online ancora.
6. Quando è tutto pronto, clicca **Publish** (in alto a destra).

La mostra apparirà sul sito live entro circa 1 minuto. 🍕

### Suggerimenti per le immagini

- L'immagine di copertina della mostra funziona meglio in formato **orizzontale** (lunga/larga, non quadrata)
- Le immagini delle opere funzionano meglio in formato **verticale** (più alte che larghe) — saranno tutte ritagliate in quella forma
- Puoi caricare quante opere vuoi per artista. Il layout si adatta automaticamente:
  - 1 opera = una grande immagine singola
  - 2 opere = affiancate
  - 3 opere = tre in fila
  - 4+ opere = griglia 2x2

### Più artisti nella stessa mostra

Clicca **Add Artista** di nuovo dopo aver compilato il primo. Ogni artista diventa il suo blocco con le sue opere. Nessun limite al numero di artisti per mostra.

---

## 👤 Come modificare il tuo profilo del team

1. Login → clicca **Team (Chi Siamo)** nella sidebar
2. Clicca sul tuo nome nella lista
3. Modifica:
   - **Nome** — il tuo nome (usa `\n` se vuoi andare a capo tra nome e cognome)
   - **Ruolo** — il tuo ruolo (es. `Curatore`)
   - **Ordine** — la tua posizione nella griglia (da 1 a 4)
   - **Foto** — carica una nuova foto se vuoi
   - **Biografia** — bio breve
   - **Email** — email pubblica di contatto
   - **Link social** — il tuo URL Instagram (o altro)
4. Clicca **Publish**.

Si può aggiungere un quinto membro se serve — basta cliccare **New Membro** in alto a destra.

---

## ✏️ Come modificare i testi delle pagine

Tutto il testo delle pagine (Homepage, intro Chi Siamo, intro Mostre, ecc.) si trova sotto **Pagine del Sito**.

1. Clicca **Pagine del Sito** → scegli quale pagina vuoi modificare
2. Modifica i campi (ogni campo è etichettato in italiano per essere chiaro)
3. **Publish**

### Per rendere parti di una frase in corsivo

Metti `<em>parole</em>` attorno alle parole che vuoi far apparire in corsivo grigio.

Esempio:
- Scrivi: `Un collettivo di <em>arte contemporanea</em>.`
- Apparirà come: *Un collettivo di* ***arte contemporanea****.* (con la parte in corsivo in grigio)

---

## ⚠️ Cose da sapere prima di pubblicare

### "Save" vs "Publish"
- **Save** — salva la tua bozza, non va online niente. Puoi salvare quante volte vuoi.
- **Publish now** — pubblica davvero sul sito live.

Solo **Publish** fa ricostruire il sito. Quindi scrivi liberamente, salva spesso, pubblica una volta sola alla fine. 🍕

### Ci vuole circa 1 minuto per andare online
Dopo aver cliccato Publish, il sito si ricostruisce automaticamente. Aspetta ~60 secondi, poi ricarica il sito live.

### Le immagini hanno un limite di dimensione
Se carichi una foto enorme (tipo 10MB+), funzionerà ancora ma potrebbe rallentare il sito. Punta a foto sotto i 2MB. Puoi ridimensionare le immagini prima di caricarle usando [tinypng.com](https://tinypng.com) o [squoosh.app](https://squoosh.app).

---

## 🆘 Se qualcosa non funziona

| Problema | Cosa provare |
|---|---|
| Non riesco a fare login | Assicurati di essere su `/admin/` (con lo slash). Prova "Forgot password?". Se sei ancora bloccato, chiedi all'admin di reinvitarti. |
| Ho pubblicato ma sul sito non è cambiato niente | Aspetta 60 secondi e ricarica. Se ancora niente, chiedi all'admin di controllare Netlify. |
| Ho caricato un'immagine ma sembra sbagliata | Controlla l'orientamento. Per le opere: verticale (più alta che larga). Per le copertine delle mostre: orizzontale (più larga che alta). |
| Ho cancellato una mostra per sbaglio | Chiedi all'admin — la versione vecchia si può recuperare dalla cronologia di GitHub. |
| Le submissions del form di contatto non arrivano nel foglio | Il collegamento tra il sito e Google Sheets è gestito tramite Apps Script — chiedi all'admin di controllare. |

---

# ⚠️ STOP — Da qui in poi è solo per l'admin tecnico

> **Tu del team, hai finito.** Tutto quello che devi sapere è sopra. La parte in inglese qui sotto è documentazione per chi gestisce il codice del sito — non ti serve. Buon lavoro! 🍕

---
---

# Developer Documentation 🔧

**This entire section is for the site admin only. If you're a team member just editing content via the CMS — you don't need anything down here. Stop reading.**

## Tech stack

- **Jekyll 4.x** — static site generator
- **Decap CMS** (formerly Netlify CMS) — content editing interface at `/admin/`
- **Netlify Identity** — authentication for CMS login
- **Netlify** — hosting and auto-deploy from `main`
- **Google Apps Script** — receives contact form POSTs and appends to a Google Sheet

## File structure

```
doppie-project.github.io/
├── _config.yml              # Jekyll config + collection declarations
├── Gemfile                  # Ruby dependencies (jekyll, jekyll-seo-tag)
├── style.css                # All styling, single file
│
├── _layouts/
│   └── default.html         # Page shell: head, nav, preloader, footer, JS
│
├── _includes/
│   ├── nav.html             # Top nav + mobile hamburger overlay
│   ├── footer.html          # Black footer with SVG logo
│   ├── hero-logo.html       # Wraps logo-svg.html with hero sizing
│   ├── logo-svg.html        # The DOPPIE SVG, uses `fill="currentColor"`
│   ├── mostra.html          # Auto-replicating template for ANY mostra
│   └── artist.html          # Auto-replicating template for ANY artist block
│
├── _team/                   # Collection: team member profiles
├── _mostre/                 # Collection: exhibitions
├── _testi/                  # Collection: testi (PDF publications)
│
├── index.md                 # Homepage (hero + image carousel)
├── chi-siamo.md             # Team page (loops _team/)
├── mostre.md                # Archive (loops _mostre/ through mostra.html)
├── testi.md                 # Testi listing (loops _testi/, PDF downloads)
├── contatti.md              # Contact form (POSTs to Google Apps Script)
│
├── documents/               # Uploaded PDFs (testi)
│
├── admin/
│   ├── config.yml           # Decap CMS field definitions
│   └── index.html           # CMS entry point
│
└── images/uploads/          # CMS-uploaded media
```

### Why the structure is the way it is

- **`_mostre/` and `_team/` are Jekyll collections**, defined in `_config.yml`. Each `.md` file in the folder becomes one exhibition/member. The CMS creates/edits these files when users add content.
- **`_includes/mostra.html`** is the single template that renders every exhibition — `mostre.md` loops `site.mostre | sort: 'order'` and passes each to this partial. Adding a new mostra = new `.md` file in `_mostre/`, no template changes needed.
- **`_includes/artist.html`** is called from inside `mostra.html` for each artist in the `artists:` list of a mostra's frontmatter. Infinitely nestable.
- The `.single`, `.three`, `.four` classes on `.artist-works` adjust the grid based on how many works an artist has.

## Making code changes

**⚠️ Do not commit directly to `main`.** Every commit to `main` triggers a production Netlify rebuild, which costs credits on the free plan (15 credits per deploy, 300 credits/month).

### Workflow

1. Create a feature branch:
   ```bash
   git checkout -b fix-whatever
   ```
   Or via GitHub web: pencil icon → Commit changes → "Create a new branch".

2. Make ALL your changes across as many files as needed on this branch. Commit freely to the branch.

3. Open a Pull Request when done. Netlify auto-builds a preview URL (unless you've disabled deploy previews to save credits — check Netlify → Site configuration → Build & deploy → Deploy Previews).

4. Test on the preview URL, including mobile (DevTools → device toolbar).

5. Merge the PR → **this is the one production deploy** that costs credits.

### Editorial workflow for CMS

`admin/config.yml` uses `publish_mode: editorial_workflow`, which means CMS saves create PR branches instead of direct commits. Each content edit = one PR. When the editor clicks **Publish**, the PR merges to main → 1 deploy.

**Known issue**: if a CMS entry seems to be stuck with a "SHA must identify a commit or a tree" error, the cause is typically a stale state reference. Fixes:
1. Rename the entry's `name:` field in `admin/config.yml` (forces Decap to treat it as a fresh entry).
2. As a fallback, disable + re-enable Git Gateway in Netlify Identity settings.

### Local development

```bash
bundle install
bundle exec jekyll serve
# Visit http://localhost:4000
```

The CMS won't work locally (needs Netlify Identity), but everything else will render.

## Deployment

Pushes/merges to `main` auto-trigger a Netlify build → deploys to the live URL in ~60 seconds.

### Current hosting limits (Netlify free plan)
- 300 credits/month (deploys cost 15 each, bandwidth 10 credits/GB)
- 100 form submissions/month (not used — form POSTs to Google directly)
- Resets monthly

If you hit the credit cap, the site stays live with the last successful build; new deploys pause until reset. Consider migrating to Cloudflare Pages if it becomes a recurring issue (unlimited bandwidth, no credit system, but CMS login would need to switch from Netlify Identity to GitHub OAuth).

### Contact form flow

1. User submits form at `/contatti/`
2. JS does a `fetch()` POST with `mode: 'no-cors'` to a Google Apps Script Web App URL
3. The Apps Script (`doPost(e)`) reads `e.parameter.email`, `e.parameter.reason`, `e.parameter.message` and appends a row to the Google Sheet
4. Browser can't read the response (no-cors mode), so the JS optimistically shows a success message

The Apps Script URL is stored in `contatti.md` frontmatter as `form_endpoint`. If you redeploy the Apps Script and the URL changes, update it there.

### Form not working?
1. Open Apps Script → **Executions** tab
2. Submit the form on the site
3. Check if an execution appears:
   - **Green** → script ran, check if row was actually added to sheet
   - **Red** → click for error
   - **Nothing** → deployment access issue. Deploy → Manage deployments → set **Who has access** to **Anyone** (not "Anyone with Google account")

---

## Contact

- **Instagram**: [@doppie.project](https://instagram.com/doppie.project/)
- **Email**: info.doppieproject@gmail.com
