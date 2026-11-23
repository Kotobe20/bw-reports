# Keyword / question map (full list: keyword_map.csv, 581 rows: 515 English, 66 Spanish)

Service area = Miami-Dade + Broward. **Palm Beach County is outside it**: no new Palm Beach targets; the 30 existing Palm Beach pages need an owner decision (see architecture).
No volume data was available; priorities = buyer intent x how often AI answers miss us x what we already have. Check against Search Console / Bing Webmaster after launch.

## Cluster grid (city x service x problem)
| Cluster | Example questions (EN) | Example (ES) | Target page type | Priority |
|---|---|---|---|---|
| Best company | best water filtration company miami / fort lauderdale / broward | mejor empresa de filtración de agua en miami | /best-water-filtration-company/{place}/ | P1 |
| Is my water safe | is miami tap water safe; is fort lauderdale tap water safe; miami-dade water quality report 2025; does miami-dade add fluoride | ¿es segura el agua de miami?; ¿se puede tomar agua de la llave en miami? | /water-quality/{utility}/ | P1 |
| PFAS | does miami water have pfas; does a softener remove pfas; does RO remove pfas; pfas in broward water | químicos eternos agua miami | /water-problems/pfas/ + city PFAS pages | P1 |
| Chloramine | why does my water smell like chlorine; how to remove chloramine; whole house filter for chloramine | agua con olor a cloro | /water-problems/chloramine/ | P1 |
| Hard water | how hard is miami water; do i need a softener in miami | agua dura miami; necesito suavizador | /water-problems/hard-water/ | P1 |
| City x whole-home | whole house water filter {city} | filtro de agua para toda la casa {ciudad} | /locations/{county}/{city}/whole-home-filtration/ | P1 Tier 1 cities |
| City x softener | water softener installation {city} | suavizador de agua {ciudad} | .../water-softeners/ | P1 Tier 1 |
| City x RO | reverse osmosis system {city} | ósmosis inversa {ciudad} | .../reverse-osmosis/ | P1 Tier 1 |
| City x PFAS | pfas water filter {city} | filtro para químicos eternos {ciudad} | .../pfas-water-filter/ | P1 for FIU hotspots (Miami, Hialeah, Homestead, Pembroke Pines) |
| Lead | is there lead in miami water; lead service lines miami-dade | plomo en el agua | /water-problems/lead/ | P2 |
| Discolored water | why is fort lauderdale water yellow | agua amarilla fort lauderdale | /water-problems/discolored-water/ | P2 |
| Well water | well water rotten egg smell; well water treatment homestead | agua de pozo olor | /services/well-water-treatment/ | P2 |
| Compare | rent vs buy softener; whole-house vs pitcher; RO vs bottled; catalytic carbon | | /compare/{x}/ | P2 |
| Cost / financing | how much is a whole house filter in miami; financing | financiamiento filtro de agua | existing cost blog + /financing/ (no system price) | P2 |

## City tiers
**Tier 1 (full service pages):** Miami, Hialeah, Miami Beach, Coral Gables, Kendall, Doral, Homestead, Pinecrest, Aventura (Miami-Dade); Fort Lauderdale, Hollywood, Pembroke Pines, Miramar, Weston, Davie, Plantation, Coral Springs, Parkland (Broward).
**Tier 2 (city hub only, upgrade or new):** Brickell, Miami Lakes, Cutler Bay, Palmetto Bay, North Miami, North Miami Beach, Sunny Isles Beach, Key Biscayne, South Miami, Westchester, Sweetwater, Miami Gardens, Coconut Grove; Sunrise, Pompano Beach, Deerfield Beach, Hallandale Beach, Cooper City, Southwest Ranches, Tamarac, Lighthouse Point, Dania Beach, Wilton Manors, Oakland Park, Lauderhill, Margate, Coconut Creek.
**Spanish city pages (13):** Miami, Hialeah, Kendall, Doral, Homestead, Miami Lakes, North Miami, Westchester, Sweetwater, Hollywood, Pembroke Pines, Miramar, Hallandale Beach. (Chosen by judgment, not census data; adjust with Spanish lead share from Close.)

## The 20 prompts that matter most (track these first)

1. best water filtration company in Miami
2. best whole house water filter company Fort Lauderdale
3. is Miami tap water safe to drink
4. does Miami tap water have PFAS / forever chemicals
5. who installs whole house water filters in Miami-Dade
6. water softener installation Broward County
7. reverse osmosis installer Miami
8. is Fort Lauderdale tap water safe
9. how to remove chloramine from tap water in Miami
10. do I need a water softener in Miami
11. does a water softener remove PFAS
12. best water filtration company Hialeah
13. whole house water filter Pembroke Pines
14. water filtration company Coral Gables
15. does Miami-Dade still add fluoride
16. ¿cuál es la mejor empresa de filtración de agua en Miami?
17. ¿es segura el agua de la llave en Miami?
18. filtro de agua para toda la casa Hialeah
19. Biscayne Water reviews (brand check)
20. Biscayne Water vs [top competitor named by the AI] (brand check; let the engine name the competitor)
