# Jero Selvin Josis Justin — Résumé Site

A static, single-page résumé site. No build step, no dependencies — just `index.html` plus an `assets/` folder.

## Files
- `index.html` — the site
- `assets/photo.jpg` — profile photo
- `Jero_Selvin_Josis_Justin_Resume.pdf` — the original PDF, linked from the "Download PDF résumé" button

## Deploy on GitHub Pages
1. Create a new GitHub repo (e.g. `jero-resume`) and upload these three items to the repo root, keeping the folder structure as-is.
2. In the repo, go to **Settings → Pages**.
3. Under **Source**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
4. Your site will be live at `https://<your-username>.github.io/jero-resume/` within a minute or two.

## Deploy on Vercel
1. Push the same repo to GitHub (steps above, minus the Pages setup).
2. Go to vercel.com → **Add New Project** → import the repo.
3. Framework preset: choose **Other** (it's plain static HTML — no build command needed).
4. Deploy. Vercel gives you a `https://<project>.vercel.app` URL, and you can attach a custom domain later.

## Editing content later
Everything is in `index.html` — job history is in the `<section id="experience">` block, skills in `<section id="skills">`, etc. No templating engine, just edit the text directly and re-deploy (Vercel/GitHub Pages redeploy automatically on every push).

## A note on "ATS bypass"
I didn't add hidden white-text keyword stuffing — most modern ATS platforms (Workday, Greenhouse, iCIMS, etc.) flag or strip that, and it can actually hurt you if a recruiter views page source. Instead this site is ATS-*friendly* the legitimate way:
- Real semantic HTML (`<h1>`–`<h2>`, `<dl>`, proper heading hierarchy) instead of images-of-text, so any parser can read it.
- A `schema.org` Person JSON-LD block and Open Graph tags, so job boards / LinkedIn-style crawlers and search engines index you correctly.
- A concise plain-text summary (visually hidden, but present in the HTML and read by screen readers/parsers) that repeats your core keywords — RCA, CAPA, Six Sigma, SPC, NPI, Python, PyTest, etc. — in plain prose.
- A same-content downloadable PDF for the systems that only accept file uploads.

For actual job applications, most companies still want a PDF or DOCX upload into their ATS — this site is best used as the link in your email signature, LinkedIn, or application "portfolio URL" field to make a strong first visual impression, alongside the PDF for the formal upload.
