# Module 7: Location Page Differentiation — Gate 0 & The 10-Rule Framework

*Source: Nico | AI Ranking — "Google Just Accidentally Created A HUGE OPPORTUNITY For Your Local Business SEO" (Sept 24, 2026 Spam Update + Oct 1, 2026 AI Content & Metadata Guidelines)*

### **7.1 Threat Model: Programmatic Location Sprawl**
The September 24, 2026 Spam Update targets low-effort programmatic location pages — sites generating "one page per town/zip code" by spinning or swapping city names on a shared template. Google now treats template-identical location sets as **doorway pages**, demoting them algorithmically and stranding them in `Crawled - currently not indexed`. Pages sharing **>50% identical substance** are classified as duplicates regardless of how or when they were published.

### **7.2 Algorithmic Realities (What Provides No Protection)**
None of the following defenses work. Do not sell them, buy them, or build around them:
*   **No "safe percentage" of AI content.** Google evaluates usefulness, accuracy, and differentiation — not generation tooling.
*   **No "safe publishing velocity."** Drip-feeding doorway pages over months does not prevent demotion.
*   **AI detector scores, word-count minimums, and "AI-assisted" disclaimer tags provide zero protection.**
*   Metadata is now a first-class enforcement surface: the Oct 1, 2026 AI content documentation sync mandates manual fact-checking of `<title>` tags, meta descriptions, structured data, and image alt text. Execution SOP: `../../kirby-aiseo-skill/SKILL.md` Module 15.

### **7.3 Gate 0 — Doorway Defense (Mandatory Pre-Creation Gate)**
Before creating ANY location page, pass the service-area truth test:
*   **Genuinely serve the area.** If you would not dispatch a vehicle or team there *this week*, do not create the page.
*   **No phantom map pins.** Never claim a virtual office or co-address you do not staff.
*   For non-dispatch professions (lawyers, accountants, consultants, realtors), the same test applies without vehicles: would you genuinely travel to serve a client there this week? The standard is real service capacity, not transportation.
*   **Gate 0 failure = page does not get created.** There is no content-quality workaround for a Gate 0 failure; Rules 1–9 cannot compensate for a fake service area.

### **7.4 The 10-Rule Differentiation Checklist**
Score every location page against Rules 1–9 before publishing; **Rule 10 is post-publish monitoring** and cannot be scored pre-emptively. **Rule 1 is the load-bearing rule** — Rules 2–7 are the structural evidence vectors that prove it, Rules 8–9 the social-proof vectors, Rule 10 the indexation watchdog.

| # | Rule | Pass Criterion |
|---|---|---|
| 1 | 50% Substance Variance | ≥50% of body content is area-specific; passes the Swap Test (§7.5) |
| 2 | Unique Per-Page Schema | Distinct `Service` JSON-LD per page: this page's `serviceType`, `areaServed` = this town, `url` = this page, `provider` → single canonical entity `@id`. Validates clean on validator.schema.org |
| 3 | Unique Geo-Photographs | Genuine on-site job photos per location (e.g. `round-rock-water-heater-install.jpg`); alt text describes the actual image honestly — never label stock/AI photos as "our team" |
| 4 | Area-Specific Polygon Map | Lazy-loaded map embed for the target suburb/town polygon — never the same central-office pin repeated |
| 5 | Real Transit/Travel Commitments | Exact drive times from HQ with operational commitments ("20 minutes from Round Rock via I-35; same-day service if called before 2 PM") |
| 6 | Natural Local Landmarks | 1–3 real reference points woven into contextual sentences ("older homes around Old Town", "off Highway 79 near the Dell Diamond") — no bottom-of-page landmark spam lists |
| 7 | Hyperlocal Neighbor Linking | 2–4 genuine adjacent-suburb pages interlinked with travel notes ("Georgetown, 15 min north"), linking up to the service hub and parent areas directory |
| 8 | Location + Job Customer Proof | Display reviews that quote BOTH the exact suburb AND the specific service performed |
| 9 | Social Video Footprint | 15–30s on-site shorts (TikTok/Reels) with spoken + on-screen local mentions, geotags, local hashtags — embedded or linked on the page |
| 10 | GSC Indexation Hygiene *(post-publish)* | Monitored via Search Console; sustained `Crawled - currently not indexed` = differentiation deficit across Rules 1–7 → §7.7 routing |

### **7.5 The Swap Test (Rule 1 Verification Procedure)**
1.  Swap the town name with an adjacent town you also serve.
2.  If the page still reads coherently, it contains no area-specific substance — **it fails**.
3.  Area-specific substance means content that cannot be transplanted: local housing stock (age, construction type), specific local water/soil/climate issues, municipal regulations and permit regimes, named infrastructure, real job histories in that town.
4.  Quantify: if less than 50% of the substantive body is transplant-resistant, rewrite before publishing. Bulk enforcement of this test is automated pre-deployment: `../../kirby-seo-deployment/SKILL.md` Module 19.
5.  Threshold reconciliation: §7.1's ">50% identical substance" is Google's enforcement classifier (shared template boilerplate counts toward identical substance); this §7.5 variance test is your authoring standard. Because boilerplate inflates the identical-substance ratio above the area-specific ratio, author to a clear majority of area-specific substance and treat 50% as the floor, never the target.

### **7.6 Local Proof Vector SOPs**
*   **Suburb + Job Review Harvesting (Rule 8):** After job completion, ask the review question that elicits both variables: "Would you mind mentioning the neighborhood and what we did?" Surface reviews on the matching location page only where both suburb AND service match. Never transplant a review onto a town where the job did not occur.
*   **On-Site Short Video (Rule 9):** Film 15–30 seconds on site at job start/completion. Requirements: spoken suburb mention + on-screen text mention, platform geotag set to the suburb, 1–2 local hashtags. Embed the short on the corresponding location page or link it from the proof section. One video per page minimum; never re-use a video across towns.
*   Template components implementing Rules 2, 4, 5, and 7 (polygon map embeds; travel-time + neighbor-linking blocks; JSON-LD generator): `../../kirby-scrappy-local-launch/SKILL.md` Module 1.

### **7.7 Indexation Hygiene & Escalation Routing**
*   `Crawled - currently not indexed` on location pages is a **differentiation deficit, not an indexing bug**. Do not respond with indexing services or resubmission spam — remediate Rules 1–7 first.
*   7-phase audit protocol (before/after delta, folder segmentation `/locations/` vs `/services/`, rollout-window alignment, manual-action clearance, 10-rule scoring, metadata fact-check, fix-timing gate): `../../kirby-seo-telemetry/SKILL.md` Module 11.
*   Metadata fact-check pass (`<title>`, meta description, JSON-LD, alt text): `../../kirby-aiseo-skill/SKILL.md` Module 15.
*   The pre-existing indexed-then-pulled router remains `../../kirby-aiseo-skill/SKILL.md` §1.16, with rewrite execution order in Module 3 §3.6.2 C.

### **7.8 Remediation Order**
1.  Eliminate Gate 0 failures first: prune or 301 pages for non-serviced towns into the nearest genuinely-serviced page.
2.  Rewrite Rule 1 failures (substance variance) before touching Rules 2–9 — evidence vectors cannot rescue thin substance.
3.  Layer schema, photos, maps, and proof vectors onto surviving pages.
4.  Execute fixes only after the rollout is marked complete on status.search.google.com; mid-rollout changes cannot be evaluated.
5.  Re-request indexing via GSC URL Inspection only after Rules 1–7 pass on the revised page.

---

### **7.9 Seasonal & Promotional Slug Architecture (Anti-Cannibalization Guardrail)**

*Source: Edward Sturm Ep. 1206 (David Quaid, Harpreet Singh, Gagan Ghotra).*

* **The Multi-Location Slug Hazard:** Service Area Businesses (SABs) and regional multi-location operators frequently deploy temporary holiday landing pages using geo-modified promotional slugs (e.g., `/locations/austin-black-friday-deals` or `/dallas-holiday-specials`). These ephemeral URLs trigger severe keyword cannibalization against established core city pages (`/locations/austin`), fracturing internal link equity and diluting Google Maps 3-pack relevance signals.
* **The Canonical Separation Standard:**
  1. **Permanent Local Hierarchy Invariant:** Core city and service landing pages (`/locations/[city]`) must remain evergreen, stable, and permanent. Never append temporary seasonal modifiers or promotional campaigns to core local URL slugs.
  2. **Dedicated Offer Silo Isolation:** House all promotional discounts and seasonal campaigns under a dedicated `/deals/` or `/offers/` directory structure (e.g., `/deals/black-friday/` or `/offers/winter-furnace-tuneup/`). Never inject calendar years into live promotional slugs (`../../kirby-seo-deployment/SKILL.md` Module 7 §7.18).
  3. **Internal Linking & Canonical Discipline:** Point strict self-referential canonical tags to each specific promotional URL — never canonicalize promo child landers into the parent deals directory or core city pages. Feature contextual promotional banners on core city pages directing local visitors to the centralized deal page, rather than publishing duplicate local promo pages.
  4. **Post-Event Archiving & Redirect Policy:** When seasonal promotions conclude, retire temporary deal URLs cleanly or maintain the directory as an evergreen seasonal hub with the January canonical archival handoff per `../../kirby-seo-deployment/SKILL.md` Module 7 §7.18, preventing dead 404 links while preserving accumulated external link equity.
