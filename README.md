# Windsor Pondscape

A static site for a native-pond and bog-filtration installer serving Windsor-Essex, Ontario. Pure HTML/CSS, no build step, no forms, no JavaScript framework — ready to publish on GitHub Pages at **windsorpondscape.ca**.

## What's in here

```
index.html          Home
services.html        Pond design & install, native planting, bog filtration, maintenance, opening/closing
about.html           About / Ambassador Property Contractors backlink
service-area.html    Windsor-Essex town-by-town coverage (local SEO)
contact.html         Phone + email only, no forms
404.html             Custom not-found page
css/style.css         Design tokens, layout, typography
favicon.svg          Site icon
robots.txt           Crawler rules + sitemap pointer
sitemap.xml          XML sitemap for search engines
CNAME                 GitHub Pages custom domain file (windsorpondscape.ca)
```

## Publish it on GitHub Pages

1. Create a new **public** GitHub repository (e.g. `windsor-pondscape`).
2. Upload every file in this folder to the repository root, keeping the `css/` folder structure intact.
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
5. Under **Custom domain**, enter `windsorpondscape.ca` and save (this matches the included `CNAME` file — GitHub will keep it in sync automatically once set).
6. Check **Enforce HTTPS** once it becomes available (GitHub needs to issue a certificate first — can take up to 24 hours).

## Point the domain at GitHub Pages

Once you own **windsorpondscape.ca**, add these DNS records at your registrar:

**Apex domain (windsorpondscape.ca) — four A records:**
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**www subdomain (optional, recommended) — one CNAME record:**
```
www   CNAME   <your-github-username>.github.io.
```

DNS propagation can take anywhere from a few minutes to 24+ hours. GitHub's own docs (Settings → Pages, after adding the custom domain) will show a green checkmark once it verifies correctly — worth double-checking there if anything looks off.

## SEO already built in

- Unique, keyword-targeted `<title>` and meta description on every page
- Canonical URLs on every page
- Open Graph + Twitter Card tags for link previews
- `HomeAndConstructionBusiness`, `Service`, `BreadcrumbList`, and `FAQPage` JSON-LD structured data
- Semantic HTML (proper heading hierarchy, `<nav>`, `<main>`, `<footer>`)
- Descriptive, keyword-rich `alt` text on every image
- `robots.txt` + `sitemap.xml`
- Fast by default — no JS frameworks, no render-blocking scripts, minimal external requests (Google Fonts + Wikimedia-hosted photos only)
- Local SEO: dedicated service-area page naming every town served, city entities in structured data

## About the native plant photos

The three plant photos (cardinal flower, great blue lobelia, blue flag iris) are hotlinked directly from Wikimedia Commons under CC0 / public domain licenses — see the credit line in the site footer. Hotlinking keeps the repo lightweight, but for the best performance and to fully control uptime, consider downloading them and serving them from an `images/` folder in this repo instead — swap the `<img src="...">` URLs in `index.html` accordingly.

## Editing content later

Everything is plain HTML — search for the text you want to change directly in the relevant `.html` file. The five services each have their own `id` anchor (`#design-install`, `#native-planting`, `#bog-filtration`, `#maintenance`, `#opening-closing`) on `services.html` if you want to link to a specific one.
