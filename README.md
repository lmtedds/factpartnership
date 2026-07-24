# factpartnership.ca

Static site for the Fair and Accountable Canadian Taxation (FACT) Partnership.
Single page, no build step, no dependencies. Edit `index.html` directly.

## Files
- `index.html` — landing page
- `research.html` — the research programme: three themes, methods, and projects
- `announcements.html` — news page; newest entry at the top
- `styles.css` — shared stylesheet for both pages. Colours and type are in the `:root` block at the top.
- `assets/sshrc-signature.png` — official SSHRC signature, English-first bilingual, full colour
- `assets/sshrc-signature-fr.png` — French-first variant (use if/when a French page is added)
- `assets/sshrc-signature-reverse.png` — reverse (white) variant, for dark backgrounds only
- `CNAME` — custom domain for GitHub Pages
- `robots.txt`, `sitemap.xml`

Signature files are the unmodified originals from SSHRC's official download package.

## Deploy (GitHub Pages)
1. Create repo `lmtedds/factpartnership`, push these files to `main`.
2. Settings → Pages → Source: `main` / root.
3. Settings → Pages → Custom domain: `factpartnership.ca`, then tick "Enforce HTTPS".
4. At the domain registrar, add:
   - `A` records for the apex to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` for `www` → `lmtedds.github.io`

## Branding compliance notes
- **SSHRC.** The signature must never be altered, must sit in open space on a clean
  background, and must always be accompanied by one of SSHRC's two prescribed
  acknowledgement messages. Both are done in the "Funding acknowledgement" block.
  The signature is deliberately *not* in the header or hero — SSHRC requires that it
  never imply an output is a SSHRC product.
- **Acknowledgement wording** is verbatim from SSHRC's prescribed option 2
  ("[project name] is supported in part by funding from..."), in English and French,
  and lists all other funders as SSHRC requires when there are multiple sources.
- **SCP / CTO.** Named and linked as organizational partners. No partner logos are used
  yet — request approved logo files and usage guidelines from each before adding them.
  Per the partnership agreement, joint mobilization products are co-branded under FACT
  with recognition of organizational contributions.

## To update later
- **Add an announcement:** in `announcements.html`, copy the whole `<article class="entry">`
  block (it's marked with comments) and paste the copy *above* the existing one — newest first.
  Change the `id` to something like `id="ctj-2026-09-15"`; that id is the shareable link
  (`factpartnership.ca/announcements.html#ctj-2026-09-15`). Update `sitemap.xml`'s `lastmod`.
- **Optional inside an entry:** `<div class="entry-note">` gives a bronze-ruled callout box,
  useful for a quote or a "read the paper" aside.
- **Add a project** to a theme in `research.html`: copy a `<div class="project">` block.
  Status pill is either `status--active` ("Underway") or `status--dev` ("In development").
- Add an output: copy an `<article class="output">` block in the Outputs section of `index.html`.
- Add a person: copy a `<div class="person">` block.
- Colours and type live in the `:root` block at the top of `styles.css`.
