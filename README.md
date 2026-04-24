# DOPPIE Project — Website

The website for **DOPPIE**, a collettivo artistico between Milano and Como.
Live at: [doppie-website.netlify.app](https://doppie-website.netlify.app)

---

## 👋 For the team (no coding required)

Hi! If you're here to add a new mostra, edit your bio, or change text on the site, you **don't need to read any code**. Skip to one of these sections:

- [How to log in](#how-to-log-in)
- [How to add a new mostra](#how-to-add-a-new-mostra)
- [How to edit your team member profile](#how-to-edit-your-team-member-profile)
- [How to edit text on a page](#how-to-edit-text-on-a-page)
- [Things to know before publishing](#things-to-know-before-publishing)
- [If something breaks](#if-something-breaks)

## 💻 For developers

- [Tech stack](#tech-stack)
- [File structure](#file-structure)
- [Making code changes](#making-code-changes)
- [Deployment](#deployment)

---

## How to log in

1. Go to [doppie-website.netlify.app/admin/](https://doppie-website.netlify.app/admin/)
2. Click **Login with Netlify Identity**
3. Use the email you were invited with + your password

If you forgot your password: click **Forgot password?** on the login screen.

If you were never invited: ask whoever runs the site to invite you via Netlify.

---

## How to add a new mostra

Once logged in, you'll see a sidebar with three sections:
- **Pagine del Sito** — editable text on each page
- **Team (Chi Siamo)** — team member profiles
- **Mostre** — all the exhibitions

### Add a mostra, step by step

1. Click **Mostre** in the sidebar → **New Mostra** (top right)
2. Fill out the fields:

| Field | What to write | Example |
|---|---|---|
| **Titolo (prima parte)** | Main title word | `Sentimento` |
| **Titolo (parte in corsivo)** | The second word — will show in grey italic | `carsico` |
| **Anno** | Year of the mostra | `2025` |
| **Ordine di visualizzazione** | 1 = appears first on the page. Newer mostre usually go first | `1` |
| **Status** | Dropdown | `Concluso`, `In corso`, or `Prossimo` |
| **Luogo completo** | Full venue address | `Spazio Milesi, Milano` |
| **Luogo breve** | Just the city — appears as a tag on the image | `Milano` |
| **Curatela** | Curator names, one per line | `Attilio A. Terragni` |
| **Immagine principale** | The big header image. Click Upload and pick a photo | (upload) |
| **Descrizione** | Long-form paragraph about the mostra | (free text) |

3. Then scroll to **Artisti** → click **Add Artista**. For each artist, fill in:
   - **Nome** and **Cognome**
   - **Origine** (e.g. `Milano, 1995`)
   - **Biografia** (short paragraph)
4. Still inside the artist → click **Add Opera** for each work. For each work:
   - **Immagine** → upload the artwork photo
   - **Titolo dell'opera** (e.g. `Eclisse`)
   - **Anno** (e.g. `2020`)
5. Click **Save** as many times as you want while you're working — nothing goes live yet.
6. When it's all ready, click **Publish** (top right).

The mostra will appear on the live site within about 1 minute.

### Image tips
- Hero image works best at a wide ratio (long/horizontal photos look better than square)
- Artwork images work best upright (portrait orientation) — all will be cropped to that shape
- You can upload as many works per artist as you want. The layout adjusts automatically:
  - 1 work = big single image
  - 2 works = side-by-side
  - 3 works = three across
  - 4+ works = 2x2 grid

### Tips for mostre that have more than one artist

Just click **Add Artista** again after filling in the first one. Each artist becomes their own block with their own works. No limit on the number of artists per mostra.

---

## How to edit your team member profile

1. Log in → click **Team (Chi Siamo)** in the sidebar
2. Click on your name in the list
3. Edit:
   - **Nome** — your name (use `\n` if you want a line break between first and last)
   - **Ruolo** — your role (e.g. `Curatore`)
   - **Ordine** — your position in the grid (1 to 4)
   - **Foto** — upload a new photo if you want
   - **Biografia** — a short bio
   - **Email** — public contact email
   - **Link social** — your Instagram URL (or other)
4. Click **Publish**.

You can add a 5th member if needed — just hit **New Membro** at the top right.

---

## How to edit text on a page

All the text on pages like Homepage, Chi Siamo intro, Mostre intro, etc. lives under **Pagine del Sito**.

1. Click **Pagine del Sito** → pick which page you want to edit
2. Edit the fields (each field is labeled in Italian so it's clear what shows up where)
3. **Publish**

### Making parts of a sentence italic
You can put `<em>words</em>` around any words you want to appear in grey italic.

Example:
- Type this: `Un collettivo di <em>arte contemporanea</em>.`
- Shows up as: *Un collettivo di* ***arte contemporanea****.* (with the italic part in grey)

---

## Things to know before publishing

### "Save" vs "Publish"
- **Save** — keeps your draft safe, nothing is live yet. You can save as many times as you want.
- **Save and request review** / **Publish now** — actually makes the change live on the website.

Only **Publish** triggers the site to rebuild. So write freely, save often, publish once.

### It takes about 1 minute to go live
After you click Publish, the site automatically rebuilds. Wait ~60 seconds, then refresh the live site.

### Images are limited in size
If you upload a huge photo (like, 10MB+), it'll still work but might slow down the site. Aim for photos under 2MB. You can resize images before uploading using something like [tinypng.com](https://tinypng.com) or [squoosh.app](https://squoosh.app).

---

## If something breaks

| Problem | What to try |
|---|---|
| Can't log in | Make sure you're at `/admin/` (with the slash). Try "Forgot password?". If still stuck, ask the admin to re-invite you. |
| Published but nothing changed on the site | Wait 60 seconds and refresh. If still nothing, check if the build failed (ask the admin to check Netlify). |
| Uploaded an image but it looks wrong | Check the image orientation. For artwork: portrait (taller than wide). For mostra heroes: landscape (wider than tall). |
| Accidentally deleted a mostra | Ask the admin — the old version is recoverable from GitHub's history. |
| "Editorial workflow" confused me | Your edits go through a review state. Click through until you see a **Publish now** button. That's the one that goes live. |
| Form submissions not appearing in the sheet | This is a connection between the site and Google Sheets — ask the admin to check the Apps Script. |

---

---

# Developer Documentation

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
│   ├── 01-member.md
│   ├── 02-member.md
│   ├── 03-member.md
│   └── 04-member.md
│
├── _mostre/                 # Collection: exhibitions
│   ├── 01-lombra-che-resta.md
│   ├── 02-sentimento-carsico.md
│   └── 03-prossima-mostra.md
│
├── index.md                 # Homepage (hero + manifesto)
├── chi-siamo.md             # Team page (loops _team/)
├── mostre.md                # Archive (loops _mostre/ through mostra.html)
├── calendario.md            # Coming soon
├── contatti.md              # Contact form (POSTs to Google Apps Script)
│
├── admin/
│   ├── config.yml           # Decap CMS field definitions
│   └── index.html           # CMS entry point
│
└── images/
    └── uploads/             # Where CMS-uploaded media lives
```

### Why the structure is the way it is

- **`_mostre/` and `_team/` are Jekyll collections**, defined in `_config.yml`. Each `.md` file in the folder becomes one exhibition/member. The CMS creates/edits these files when users add content.
- **`_includes/mostra.html`** is the single template that renders every exhibition — the magic is that `mostre.md` loops `site.mostre | sort: 'order'` and passes each to this partial. Adding a new mostra = new `.md` file in `_mostre/`, no template changes needed.
- **`_includes/artist.html`** is called from inside `mostra.html` for each artist in the `artists:` list of a mostra's frontmatter. Infinitely nestable.
- The `.single`, `.three`, `.four` classes on `.artist-works` adjust the grid based on how many works an artist has.

## Making code changes

**⚠️ Do not commit directly to `main`.** Every commit to `main` triggers a production Netlify rebuild, which costs credits on the free plan.

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

`admin/config.yml` has `publish_mode: editorial_workflow`, which means CMS saves create PR branches instead of direct commits. Each content edit = one PR. When the editor clicks **Publish**, the PR merges to main → 1 deploy.

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
