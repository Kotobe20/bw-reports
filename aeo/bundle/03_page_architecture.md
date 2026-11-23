# Page architecture

Rules for every page: answer-first block (40 to 60 words) under the H1; one H2 per buyer question; a sourced data table where numbers exist; visible FAQ that matches FAQPage JSON-LD word for word; breadcrumb; `dateModified`; 3+ contextual internal links; CTA = free in-home water test. One LocalBusiness node sitewide (`@id` https://biscaynewater.com/#business) referenced by every page. **No AggregateRating** unless it uses the real, current Google total (all reviews, incl. the 2-star) supplied by the owner.

Principle from Doug's screenshots: **fix existing pages before creating new ones.** Phase 1 upgrades what exists; new pages follow.

## A. Fix first (existing pages, ~60)
| Page(s) | Change |
|---|---|
| index.html, /services/ + 3 service pages | Facts to new rules (1000+ customers, 5 stars; extended 15 year warranty; financing line), answer-first block, add PFAS section + link to /water-problems/pfas/ |
| 8 blog posts | Add answer block, data table with CCR citations, dateModified, links to new utility/problem pages; remove unsourced "200-350 ppm", "purer than bottled", "2 cents/gallon" unless a source is added |
| ~40 Miami-Dade + Broward legacy flat city pages (scripts/generate-city-pages.py) | Facts update, answer block, "your water utility" section linking to the right /water-quality/ page; Tier 1 cities get a 301 to the new nested hub **only after owner OK** |
| /locations/ hub, county hubs | Remove Palm Beach from "service area" wording if owner confirms |
| llms.txt, BIZ dict in generate-agent-files.py, data.js, agent skills | New facts; service area; list new hubs |
| 30 Palm Beach pages | **Owner decision.** Options: (1) keep as is, (2) noindex + remove from sitemap, (3) 301 to /locations/. Default in the Claude prompt: list them in the PR, change nothing |

## B. New pages (154)
| Section | URL pattern | Count | Schema | Links to |
|---|---|---|---|---|
| Water-quality hub | /water-quality/ | 1 | CollectionPage, BreadcrumbList | every utility page |
| Utility pages | /water-quality/{utility}/: miami-dade-wasd, miami-dade-wasd-south-dade, miami-beach, north-miami-beach, homestead, north-miami, fort-lauderdale, hollywood, broward-county, pembroke-pines, miramar, sunrise, plantation, pompano-beach, coral-springs | 15 | WebPage + citation, FAQPage, BreadcrumbList | problems, cities served, ES twin |
| Problems hub + pages | /water-problems/ + pfas, chloramine, hard-water, lead, disinfection-byproducts, discolored-water, sulfur-smell-well-water | 8 | WebPage, FAQPage, Service (where we fix it), HowTo (test/fix steps) | services, utilities, compare |
| New services | /services/pfas-water-filtration/, /services/water-testing/, /services/well-water-treatment/ | 3 | Service, FAQPage, HowTo (water-testing) | problems, cities |
| Nested city hubs (new) | /locations/{county}/{city}/ for 16 Tier 1 cities without a nested hub + 8 brand-new Tier 2 cities (Brickell, Miami Gardens, Dania Beach, Wilton Manors, Oakland Park, Lauderhill, Margate, Coconut Creek) | 24 | Service w/ areaServed City, FAQPage, BreadcrumbList | services in city, utility page, county hub |
| City x service | /locations/{county}/{city}/{whole-home-filtration, water-softeners, reverse-osmosis}/ for 18 Tier 1 cities (minus 4 that exist) | 50 | Service, FAQPage, BreadcrumbList | sibling services, utility, problem pages |
| City x PFAS | /locations/{county}/{city}/pfas-water-filter/ for Miami, Hialeah, Homestead, Pembroke Pines | 4 | Service, FAQPage | /water-problems/pfas/ |
| Best-in-place | /best-water-filtration-company/{miami, miami-dade, fort-lauderdale, broward}/ | 4 | Article, HowTo, FAQPage | services, reviews, utility |
| Compare hub + pages | /compare/ + rent-vs-buy-water-softener, catalytic-carbon-vs-standard-carbon, reverse-osmosis-vs-bottled-water, whole-house-vs-pitcher-filter, diy-vs-professional-install, water-softener-vs-pfas-filter | 7 | Article, FAQPage | services |
| Guides | /guides/how-to-read-your-water-quality-report/, /guides/boil-water-notice-and-hurricanes/ | 2 | HowTo, FAQPage | water-quality |
| Trust | /faq/ (all FAQs, grouped), /about/ (owner-supplied facts only), /reviews/ (real Google reviews from scripts/google-reviews.json, link to GBP), /sources/ (every source + date checked) | 4 | FAQPage; AboutPage + Organization; WebPage | everywhere |
| Spanish | /es/ (home), /es/contacto/, /es/financiamiento/, /es/servicios/ + 4 services, /es/problemas/ + 4 (pfas, cloro-y-cloramina, agua-dura, plomo), /es/calidad-del-agua/ + 3 (miami-dade, fort-lauderdale, hollywood), /es/ciudades/{13 cities}/, /es/preguntas-frecuentes/, /es/mejor-empresa-filtracion-agua-miami/ | 32 | same as EN twins, inLanguage es-US, hreflang pairs | EN twins + ES siblings |

**Total new: 154 pages** (plus ~60 upgraded). Utility pages without verified CCR data ship as `draft` (noindex, not in sitemap) until the numbers are loaded from the PDF.

**Thin-page guard:** a city x service page must carry at least 3 city-specific facts (its utility and that utility's sourced numbers, neighborhoods, nearby cities) or it stays draft. 50 near-identical pages would hurt more than help.

## C. Machine-readable layer

- sitemap.xml: add every non-draft page with real lastmod; `xhtml:link` hreflang alternates for EN/ES pairs.
- robots.txt: already right; keep. Add `Sitemap:` for any new sitemap file only.
- llms.txt: add sections "Water quality by utility", "Water problems", "Spanish / Español", "Compare"; update facts; remove Palm Beach if owner confirms.
- llms-full.txt + Markdown twins: regenerate with scripts/generate-agent-files.py.
- JSON-LD @graph per page; Organization/LocalBusiness only once with @id; `sameAs` GBP, Facebook, Instagram, Nextdoor, Yelp/BBB/Angi once created.

## D. Internal linking
Hub-and-spoke: home → services, /water-quality/, /water-problems/, /locations/, /es/. Every city page → its utility page + 2 problem pages. Every problem page → services that fix it + 3 most affected utilities. Every utility page → the cities it serves. Every EN page ↔ ES twin. Breadcrumbs everywhere. No orphan pages (build fails on orphans).
