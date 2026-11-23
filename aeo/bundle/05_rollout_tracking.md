# 30 / 60 / 90-day rollout + AI-visibility tracking

## Days 0-30: fix + own the data

1. Owner decisions (week 1): Palm Beach pages; 15-year warranty wording vs site's 10-year terms; founded year; real Google review count; whether condo installs are offered; IAPMO listing URL for PFAS Guard; financing fine print for $69/mo.
2. Run the Claude Code prompt, Phase 1 (fix existing pages + facts + llms.txt) and Phase 2 first batch: /water-quality/ hub + WASD (both systems) + Hollywood + Fort Lauderdale + Broward County, /water-problems/pfas, chloramine, hard-water, the 5 written pages. PR, review, deploy.
3. GBP cleanup, Bing Places, Apple Business Connect, Bing Webmaster + IndexNow, Search Console sitemap resubmit.
4. Start the review-ask automation (text after HCP job complete).
5. Baseline: run all tracking prompts in every engine, record results (sheet below).

## Days 31-60: expand + earn

1. Tier 1 city hubs + city x service pages (only those with 3+ city facts), PFAS city pages, remaining utility pages as CCR data is loaded.
2. Spanish batch: /es/ home, services, problems, Miami-Dade + Broward water pages, top 6 Spanish city pages. Native-speaker review before publish.
3. Directories: Yelp, Angi, BBB status, Nextdoor, imovingtoflorida.
4. Press pitch with the PFAS table. Reddit/Nextdoor weekly answers.
5. Re-run tracking prompts; for each miss, log which competitor and which source the engine cited (screenshot method), then fix the page or the source gap.

## Days 61-90: contest + loop

1. Compare pages, best-in-place pages for Fort Lauderdale, Broward, Miami-Dade, remaining Tier 2 hubs and Spanish city pages.
2. Refresh any page whose source changed (new CCR each spring by July 1).
3. Monthly prompt re-test; update pages that still miss; report Google (GSC clicks/impressions) and AI (mentions/citations) separately.

## AI-visibility tracking
Engines: ChatGPT (search on, logged out + logged in), Google AI Overviews / AI Mode, Perplexity, Gemini, Grok, Copilot. Run from a Miami IP or add "in Miami, FL". Same wording every month.

Sheet columns: date · engine · prompt · Biscayne Water mentioned (Y/N) · position in list · our URL cited (Y/N, which URL) · competitors named · third-party sources cited · fact errors about us · next action.

### Prompt list (40)
**Best / who to hire (EN)**

- #1 What is the best water filtration company in Miami?
- #2 Best whole house water filter installer in Miami-Dade?
- #3 Best water filtration company in Fort Lauderdale?
- #4 Who installs water softeners in Broward County?
- #5 Best reverse osmosis installer near Coral Gables?
- #6 Recommend a company to test my water in Hialeah.
- #7 Whole house water filter company in Pembroke Pines?
- #8 Water filtration company in Kendall with good reviews?
- #9 Who should I call for well water treatment in Homestead?
- #10 Best water filtration company in Hollywood, FL?
- #11 Water softener company in Weston FL?
- #12 Whole house water filtration Miami Beach condo?

**Water safety / problems (EN)**

- #13 Is Miami tap water safe to drink?
- #14 Is Fort Lauderdale tap water safe to drink?
- #15 Does Miami tap water have PFAS?
- #16 Does a water softener remove PFAS?
- #17 How do I remove chloramine from my water in Miami?
- #18 How hard is Miami-Dade tap water?
- #19 Do I need a water softener in South Florida?
- #20 Does Miami-Dade still add fluoride to water?
- #21 Why is my Fort Lauderdale tap water yellow?
- #22 Is there lead in Miami tap water?
- #23 What is in Hollywood FL tap water?
- #24 Whole house filter vs reverse osmosis for Miami water?
- #25 Is it better to rent or buy a water softener in Florida?
- #26 How much does a whole house water filter cost in Miami? (we win on trust, not price)

**Spanish**

- #27 ¿Cuál es la mejor empresa de filtración de agua en Miami?
- #28 ¿Es segura el agua de la llave en Miami?
- #29 ¿El agua de Miami tiene químicos eternos?
- #30 Filtro de agua para toda la casa en Hialeah
- #31 ¿Necesito un suavizador de agua en Miami?
- #32 Ósmosis inversa en Doral, ¿quién la instala?
- #33 ¿Qué empresa hace pruebas de agua gratis en Miami?
- #34 Calidad del agua en Hollywood, Florida

**Brand checks**

- #35 What is Biscayne Water?
- #36 Is Biscayne Water legit? Reviews?
- #37 Biscayne Water warranty and financing?
- #38 Does Biscayne Water serve Fort Lauderdale?
- #39 Biscayne Water vs [competitor the engine named in prompt 1]
- #40 ¿Biscayne Water es buena empresa?

Success metric (no forecast): count of prompts 1-34 where Biscayne Water is mentioned, and count where a biscaynewater.com URL is cited, per engine per month.
