# Module 7: Location Page Differentiation — Gate 0 & The 10-Rule Framework

*Source: Nico | AI Ranking — "Google Just Accidentally Created A HUGE OPPORTUNITY For Your Local Business SEO" (September 2026 spam update + Oct 1, 2026 AI Content & Metadata Guidelines)*

### **7.1 Threat Model: Programmatic Location Sprawl**
The September 2026 spam update targets low-effort programmatic location pages — sites generating "one page per town/zip code" by spinning or swapping city names on a shared template. Google now treats template-identical location sets as **doorway pages**, demoting them algorithmically and stranding them in `Crawled - currently not indexed`. Pages sharing **>50% identical substance** are classified as duplicates regardless of how or when they were published. Sources disagree on the exact start and end dates of this update, so this module cites the month only; the rules below do not depend on a date.

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
*   **Existence Litmus Test (Nov 2026 core update):** If a location page couldn't exist without the town name in it, it probably shouldn't exist. A page that only becomes "about" a town because the name was inserted fails Gate 0 regardless of Rules 2–9.

### **7.4 The 10-Rule Differentiation Checklist**
Score every location page against Rules 1–9 before publishing; **Rule 10 is post-publish monitoring** and cannot be scored pre-emptively. **Rule 1 is the load-bearing rule** — Rules 2–7 are the structural evidence vectors that prove it, Rules 8–9 the social-proof vectors, Rule 10 the indexation watchdog.

| # | Rule | Pass Criterion |
|---|---|---|
| 1 | 50% Substance Variance | ≥50% of body content is area-specific; passes the Swap Test (§7.5) |
| 2 | Unique Per-Page Schema | Distinct `Service` JSON-LD per page: this page's `serviceType`, `areaServed` = this town, `url` = this page, `provider` → single canonical entity `@id` (`{site}/#organization`, typed `LocalBusiness` or a subtype such as `Locksmith`); that entity node is identical on every page (same `@id`, site-root `url`, `name`, `telephone`, `hasMap` and `sameAs` per Module 6 §6.10, and, where the business publishes them, `address` (with `geo` only alongside it; omit both for a service-area business that hides its address, Module 6 §6.8) and `openingHoursSpecification`), with no per-locality value on any property: a site-wide `areaServed` is fine, a per-town one is not. No `AggregateRating` or `Review` node for reviews about the business and no `AggregateOffer` or `Offer` node for its prices on service or local pages (Module 6 §6.10; genuine ecommerce product offers are the carve-out, `../../kirby-aiseo-skill/SKILL.md` §2.49). At deploy this clause is a human-review flag, not a structural pass/fail (`../../kirby-seo-deployment/SKILL.md` Module 19 §19.3). Validates clean on validator.schema.org |
| 3 | Unique Geo-Photographs | Genuine on-site job photos per location (e.g. `round-rock-water-heater-install.jpg`); alt text describes the actual image honestly — never label stock/AI photos as "our team" |
| 4 | Area-Specific Polygon Map | Lazy-loaded map embed for the target suburb/town polygon — never the same central-office pin repeated |
| 5 | Real Transit/Travel Commitments | Exact drive times from HQ with operational commitments ("20 minutes from Round Rock via I-35; same-day service if called before 2 PM") |
| 6 | Natural Local Landmarks | 1–3 real reference points woven into contextual sentences ("older homes around Old Town", "off Highway 79 near the Dell Diamond") — no bottom-of-page landmark spam lists |
| 7 | Hyperlocal Neighbor Linking | 2–4 genuine adjacent-suburb pages interlinked with travel notes ("Georgetown, 15 min north"), linking up to the service hub and parent areas directory. Keep the pages under one `/locations/[city]/` subfolder (the skill's existing location-silo path; `[city]` is a placeholder for a slugified town name, not a literal path segment), and create one only for a town that passes Gate 0 (a convention that supports the anti-doorway stance, not a ranking lever) |
| 8 | Location + Job Customer Proof | Display reviews that quote BOTH the exact suburb AND the specific service performed |
| 9 | Social Video Footprint | 15–30s on-site shorts (TikTok/Reels) with spoken + on-screen local mentions, geotags, local hashtags — embedded or linked on the page |
| 10 | GSC Indexation Hygiene *(post-publish)* | Monitored via Search Console; sustained `Crawled - currently not indexed` = differentiation deficit across Rules 1–7 → §7.7 routing |

### **7.5 The Swap Test (Rule 1 Verification Procedure)**
1.  Swap the town name with an adjacent town you also serve.
2.  If the page still reads coherently, it contains no area-specific substance — **it fails**.
3.  Area-specific substance means content that cannot be transplanted: local housing stock (age, construction type), specific local water/soil/climate issues, municipal regulations and permit regimes (including council permit lead-times and utility constraints), named infrastructure, real job histories in that town.
4.  Quantify: if less than 50% of the substantive body is transplant-resistant, rewrite before publishing. Bulk enforcement of this test is automated pre-deployment: `../../kirby-seo-deployment/SKILL.md` Module 19.
5.  Threshold reconciliation: §7.1's ">50% identical substance" is Google's enforcement classifier (shared template boilerplate counts toward identical substance); this §7.5 variance test is your authoring standard. Because boilerplate inflates the identical-substance ratio above the area-specific ratio, author to a clear majority of area-specific substance and treat 50% as the floor, never the target.

### **7.6 Local Proof Vector SOPs**
*   **Suburb + Job Review Harvesting (Rule 8):** After job completion, ask the review question that elicits both variables: "Would you mind mentioning the neighborhood and what we did?" Surface reviews on the matching location page only where both suburb AND service match. Never transplant a review onto a town where the job did not occur.
*   **The 3-Job Localized Mini-Case-Study Slider (Rules 3 & 8 — Steven Fudge case study on Nico | AI Ranking, `ZAQH2Gd1i9E`):** Embed a 3-job before/after slider on each area page documenting specific recent jobs completed in that town, using authentic camera photos with descriptive localized `alt` attributes and paired directly above the matching customer review from that job. *(Per Module 3 §3.20, Google's Vision AI and semantic parser reward the authentic pixel content, localized alt text, and surrounding case-study context — do not waste billable hours on synthetic EXIF coordinate injection).*
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
4.  Execute fixes only after the rollout is marked complete on status.search.google.com **plus at least 7 days** (Nov 2026 core update: Nov 10 – ~Nov 24; freeze through ~Dec 1; canonical freeze rule `../../kirby-seo-telemetry/SKILL.md` Module 16 §16.1–16.2, deploy interlock `../../kirby-seo-deployment/SKILL.md` Module 7 §7.6). Mid-rollout changes cannot be evaluated. This also pauses the item-6 weekly publication cadence.
5.  Re-request indexing via GSC URL Inspection only after Rules 1–7 pass on the revised page.
6.  **Post-Gate Rollout Cadence & Flat URL Taxonomy (Steven Fudge case study on Nico | AI Ranking, `ZAQH2Gd1i9E`):** When restructuring deeply nested location paths (`/location/area/service-area/`) into clean location URLs that pass Gate 0 and Rule 1 (≥50% unique local copy researched via Perplexity), stage publication and indexing at **7 pages per week** to maintain clean Googlebot crawl throughput.

---

### **7.9 Seasonal & Promotional Slug Architecture (Anti-Cannibalization Guardrail)**

*Source: Edward Sturm Ep. 1206 (David Quaid, Harpreet Singh, Gagan Ghotra).*

* **The Multi-Location Slug Hazard:** Service Area Businesses (SABs) and regional multi-location operators frequently deploy temporary holiday landing pages using geo-modified promotional slugs (e.g., `/locations/austin-black-friday-deals` or `/dallas-holiday-specials`). These ephemeral URLs trigger severe keyword cannibalization against established core city pages (`/locations/austin`), fracturing internal link equity and diluting Google Maps 3-pack relevance signals.
* **The Canonical Separation Standard:**
  1. **Permanent Local Hierarchy Invariant:** Core city and service landing pages (`/locations/[city]`) must remain evergreen, stable, and permanent. Never append temporary seasonal modifiers or promotional campaigns to core local URL slugs.
  2. **Dedicated Offer Silo Isolation:** House all promotional discounts and seasonal campaigns under a dedicated `/deals/` or `/offers/` directory structure (e.g., `/deals/black-friday/` or `/offers/winter-furnace-tuneup/`). Never inject calendar years into live promotional slugs (`../../kirby-seo-deployment/SKILL.md` Module 7 §7.18).
  3. **Internal Linking & Canonical Discipline:** Point strict self-referential canonical tags to each specific promotional URL — never canonicalize promo child landers into the parent deals directory or core city pages. Feature contextual promotional banners on core city pages directing local visitors to the centralized deal page, rather than publishing duplicate local promo pages.
  4. **Post-Event Archiving & Redirect Policy:** When seasonal promotions conclude, retire temporary deal URLs cleanly or maintain the directory as an evergreen seasonal hub with the January canonical archival handoff per `../../kirby-seo-deployment/SKILL.md` Module 7 §7.18, preventing dead 404 links while preserving accumulated external link equity.

---

### **7.10 Existing-Estate Zero-Impression Audit (Index-Bloat Pass)**
*Source: Nov 2026 core update audit (example: 140 of 319 location pages with 0 impressions; single-source, directional).*
1. Export GSC per-URL impressions for `/locations/` (and any `{service}-{town}` slugs) over 90 days (snapshot during the freeze; do not prune yet).
2. Flag URLs with 0 impressions. Apply the §7.3 Existence Litmus Test and §7.5 Swap Test to each.
3. After the freeze (`../../kirby-seo-telemetry/SKILL.md` Module 16 §16.2): failures = prune per §7.8 (301 to nearest genuinely-served page, or 410 if no equivalent per `../../kirby-seo-deployment/SKILL.md` Module 7 §7.7); passes = rewrite via Rules 1–9. Zero impressions alone is a trigger for review, not proof of a bad page (new/seasonal pages exempt for 90 days).
4. Rule 10 extension: sitewide drag from zero-impression pages is monitored alongside `Crawled - currently not indexed`.

---

### **7.11 Local-SEO Service-Page Conversion Deltas (`HfRNZZIlZ6w` — Mandatory House Rules + Advisory Conversion Deltas)**
*[`kirby-text-first-cro`](../../kirby-text-first-cro/SKILL.md) §21.1 (`10-Point Service Page Blueprint`) is the advisory layout blueprint (per §21.1, Kasra Dash's conversion heuristics are directional, single-source and unscored); [`kirby-text-first-cro`](../../kirby-text-first-cro/SKILL.md) §1.6 and Module 11 §11.3 item 5 set the 4-step customer journey as the default; the 3-step scope block in §21.1 item 4 (see also [`kirby-aiseo-skill`](../../kirby-aiseo-skill/SKILL.md) Module 2 §2.32E) is an optional compact local-service variant that does not replace the 4-step journey. Strictly honors Module 6 §6.10 & Rule 2 above: **ban `AggregateRating`/`Review` markup for reviews about the business sitewide** (including ecommerce pages; the product-offer carve-out below is unchanged), and ban `AggregateOffer`/`Offer` markup on any page of the site (the sole `Offer` exception applies solely to genuine ecommerce product offers with visible prices, Module 6 §6.10). **Gate rule (§7.11-local; does not relax §7.4 Rules 1–9 or Rule 2's human-review status):** within this §7.11 checklist, only the "Local-Proof & Zip/Postcode Widget Pairing" and "Trade Credentials & Human Entity Proof" bullets carry gating checks, and only their house-rule parts gate publishing (Rules 3/4/7/8, Gate 0, consent and regulator-published identifiers per Module 6 §6.4/§6.7/§6.10); the "Tier-Scoped First-Screen Hero" bullet and all Kasra Dash layout deltas stay advisory and directional; conversion-layout remediation routes to [`kirby-text-first-cro`](../../kirby-text-first-cro/SKILL.md) §21 (applied post-freeze only on existing `/locations/[city]/` URLs; never bypassing §7.8 freezes on active rollout cohorts).*
- [ ] **Tier-Scoped First-Screen Hero & Intent-Split Subpages *(advisory, not part of the gating subset)*:** On pages that target a named town (Tier 3 geo-hubs and town-specific local geo service pages per Module 3 §3.6), put exact primary service + town in `<h1>` per [`kirby-text-first-cro`](../../kirby-text-first-cro/SKILL.md) §21.1 item 1, keeping the `[Service] in [Target City]` pattern in `<title>` per Module 11 §11.3 item 1; Tier 1/Tier 2 pages follow Module 11 §11.3 item 1 as written. Pair with [`kirby-text-first-cro`](../../kirby-text-first-cro/SKILL.md) §21.1 CTAs/pricing and dedicated intent-split subpages (`repairs` vs. `servicing` vs. `new installs` — counted inside the `30–38`-page Core 30 ceiling and created only where intents genuinely differ with unique scope content, or linked to existing Tier 2 pages) instead of `3,000`-word walls *(conversion layout heuristic: directional, single-source; source: Kasra Dash, "This SEO Mistake Is ABSOLUTELY EVERYWHERE", Nov 2026, video `HfRNZZIlZ6w`)*.
- [ ] **Local-Proof & Zip/Postcode Widget Pairing:** On Tier 3 local geo pages, replace bloated 50-town footer SEO link walls with an interactive zip/postcode serviceability checker (matching Gate 0-served areas only, with no persistent PII storage beyond live check) + Rule 4 polygon map embed, while keeping the Rule 7 2–4 adjacent-suburb neighbor links, Rule 3 genuine on-site job photos with honest alt text (no synthetic EXIF geotagging per Module 3 §3.20; native camera geolocation is acceptable per Module 6 §6.4), and Rule 8 reviews quoting both exact suburb AND specific service.
- [ ] **Trade Credentials & Human Entity Proof:** Display relevant trade credentials (`Gas Safe`, `SRA`, `GDC`, where applicable; using only regulator-published identifiers) paired with real team portraits and names (with consent per Module 6 §6.7; authentic-photo rules per Module 6 §6.4).
