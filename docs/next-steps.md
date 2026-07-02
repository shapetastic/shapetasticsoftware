# Shapetastic website — next steps

Reference list of outstanding / optional work. Nothing here is urgent; the site is
live and healthy. Ticked items are already done for context.

## Done
- [x] Added AI content: **AI capabilities** grid, **How we build** strip, responsible-AI pledges in Approach.
- [x] SEO foundation: canonical tag, `ProfessionalService` JSON-LD, `robots.txt`, `sitemap.xml`, absolute OG/Twitter images, `<main>` landmark, logo dimensions + `fetchpriority`.
- [x] Made **shapetasticsoftware.co.uk** the canonical site; **shapetastic.co.uk** 301-redirects to it (verified live). Deploy publishes the site to the canonical host and only the redirect `.htaccess` to the legacy host.

## Off-site (only the owner can do these — highest value)
- [ ] **Google Search Console** — register `shapetasticsoftware.co.uk`, submit `https://shapetasticsoftware.co.uk/sitemap.xml`.
- [ ] If `shapetastic.co.uk` was previously verified in Search Console, use the **Change of Address** tool to signal the domain move (speeds up transfer of ranking signals; the 301 handles it either way).
- [ ] **Google Business Profile** — biggest lever for local/Swansea visibility.
- [ ] Optional: **Bing Webmaster Tools** — verify + submit the same sitemap.
- [ ] Validate structured data via Google's **Rich Results Test** (paste the homepage URL).

## On-page content (nice-to-have, improves SEO depth)
- [ ] **FAQ section** with `FAQPage` structured data — highest-value on-page addition; adds indexable text and can win rich results. Fits the existing card style.
- [ ] **Local keyword tuning** — weave "Swansea", "Wales", "UK" naturally into the title and copy (currently only in the address).

## Polish (optional)
- [ ] Proper **1200×630 social share image** — `og:image`/`twitter:image` currently use the square logo, which social platforms crop.
- [ ] Review the `priceRange: "££"` placeholder in the JSON-LD (`site/index.html`) — adjust or remove.
- [ ] Bump workflow actions to clear the **Node 20 deprecation** warning: `actions/checkout` and `SamKirkland/FTP-Deploy-Action` to their latest versions in `.github/workflows/deploy.yml`.

## Notes
- Site is a single self-contained `site/index.html` (vanilla HTML/CSS/JS, no build step); keep additions dependency-free.
- Deploy triggers only on changes to `site/**`, `redirect/**`, or the workflow file — editing docs like this one does **not** redeploy.
- Email `dean@shapetastic.co.uk` is intentionally kept on the original domain; only web URLs moved to the canonical domain.
