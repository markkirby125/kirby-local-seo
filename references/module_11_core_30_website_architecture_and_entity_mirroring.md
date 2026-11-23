# Module 11: The Core 30 Website Architecture & Entity Sitemap Blueprint

*Source: Caleb Ulku ("How to Rank #1 on Google Maps (Core 30 Method)", "OWN Your City in a MONTH with This SEO Guide") & Edward Sturm ("The 30-Page Local SEO Hack Google's AI Is Already Rewarding"). October 2026.*

The traditional agency practice of publishing weekly informational blog posts (*"5 Signs Your Boiler Needs Repair"*, *"Why Backup Matters for Small Business"*) is, per the sources above, a poor first investment for a local SMB whose commercial service pages are not yet built: generic informational posts tend to win little local-intent traffic and pass little geographic relevance to the Google Business Profile. Build the commercial pages first (Module 4 §4.2); useful, practitioner-led blog posts can follow ([`kirby-text-first-cro`](../../kirby-text-first-cro/SKILL.md) §21.2).

This module is the **single canonical home** for Caleb Ulku’s **Core 30 Architecture**: a surgical 30-to-38-page commercial sitemap that mirrors every GBP category, sub-service, and regional hub 1:1.

---

### **11.1 Architecture Selection Matrix: Five-Page Lean vs. Core 30**

To prevent architectural conflict across local builds, select the site topology based on business maturity and service breadth:

| Deployment Stage | Target Architecture | Canonical Specification | When to Deploy |
|---|---|---|---|
| **Stage 1: Greenfield / Micro-Budget Launch** | **5-Page Lean Site** | Module 4 §4.2 & [`kirby-scrappy-local-launch`](../../kirby-scrappy-local-launch/SKILL.md) | Brand-new domain, single primary trade, <$100 launch budget, rapid 7-day validation. |
| **Stage 2: Established Multi-Service / City Domination** | **Core 30 Sitemap** | **Module 11 (This Module)** | Established operator, multiple secondary GBP categories, competitive metropolitan/suburban market, scaling into AI Overviews and Ask Maps. |

---

### **11.2 The Core 30 Sitemap Topology**

Google’s local ranking algorithms and LLM crawlers parse websites as hierarchical entity trees. When a website bundles 15 services onto a single generic `/services` page, Google assigns fractional semantic confidence to each capability. Dedicating one structured commercial page to every discrete entity maximizes machine trust.

```
                          ┌────────────────────────────┐
                          │   Homepage (Primary Hub)   │
                          │  Primary GBP Category +    │
                          │      Headquarters City     │
                          └─────────────┬──────────────┘
                                        │
         ┌──────────────────────────────┼──────────────────────────────┐
         ▼                              ▼                              ▼
┌────────────────────┐        ┌────────────────────┐        ┌────────────────────┐
│  Tier 1: Category  │        │ Tier 2: Atomic     │        │ Tier 3: Regional   │
│  Pillar Pages      │        │ Sub-Service Pages  │        │ Geo-Hub Pages      │
│  (GBP Secondaries) │        │ (GBP Service Menu) │        │ (Gate 0 Compliant) │
├────────────────────┤        ├────────────────────┤        ├────────────────────┤
│ 4–8 Pages matching │        │ 10–15 Pages for    │        │ 5–8 Adjacent Town  │
│ exact secondary    │        │ high-margin tasks  │        │ Hubs passing the   │
│ GBP categories     │        │ & industry niches  │        │ Module 7 Swap Test │
└────────────────────┘        └────────────────────┘        └────────────────────┘
```

1. **The Root Hub (1 Page — Homepage)**:
   - Targets the **Primary GBP Category + Primary Headquarters City** (e.g., `Managed IT Support Ascot`).
   - Embeds the live Google Review widget, primary NAP matching GBP digit-for-digit, and links directly to all Tier 1 category pillars.
2. **Tier 1: Secondary Category Pillar Pages (4–8 Pages)**:
   - One dedicated pillar page for every secondary category selected inside the GBP dashboard (e.g., `Computer Security Service`, `Data Recovery Service`, `Computer Consultant`, `Telecommunications Service`).
   - *Rule*: Never add a secondary category to GBP unless its corresponding Tier 1 pillar page is live on the website (Module 8 §8.2).
3. **Tier 2: Atomic Sub-Service & Vertical Pages (12–16 Pages)**:
   - One dedicated page for each core commercial service listed under the GBP Services menu (e.g., `Microsoft 365 Cloud Migration`, `Business VoIP Phone Systems`, `Ransomware Recovery & Firewall Setup`) plus high-margin B2B industry verticals (e.g., `IT Support for Law Firms`, `IT Support for Dental Practices`).
4. **Tier 3: Differentiated Regional Geo-Hubs (5–8 Pages)**:
   - Targets high-value neighboring towns within the 15–25 mile service radius.
   - **Mandatory Compliance Gate**: Every Geo-Hub page MUST pass **Gate 0 and the 10-Rule Differentiation Swap Test** defined in Module 7 §7.3–§7.5 (localized job proof, hyper-local commercial landmarks, zero template spinning).
5. **Tier 4: Commercial Trust & Pricing Anchors (4–6 Pages)**:
   - Dedicated pages for `/pricing` (transparent base pricing and cost drivers), `/case-studies`, `/about` (real leadership/team E-E-A-T), and `/contact` (embedded map CID and SLA commitments).

---

### **11.3 On-Page Structural Blueprint for Every Core 30 Page**

Every service page inside the Core 30 architecture must adhere to a strict 6-block structural template designed for simultaneous human conversion and LLM table extraction:

1. **Title Tag & H1 Parity**:
   - `<title>`: `[Exact GBP Category/Service Name] in [Target City] | [Brand Name]`
   - `<h1>`: Direct commercial match addressing the immediate customer problem.
2. **Above-the-Fold Trust & NAP**:
   - Exact header phone parity, live review rating badge, and clear SLA response commitment.
3. **Problem-to-Deliverable Scope Table**:
   - Use clean HTML `<table>` markup detailing what is included, turnaround times, and technical standards. LLMs disproportionately extract structured HTML tables over dense prose paragraphs.
4. **Transparent Base Pricing & Cost Drivers**:
   - Publish explicit starting rates, per-unit/per-seat tiers, and cost variables (cross-reference [`kirby-text-first-cro`](../../kirby-text-first-cro/SKILL.md) §17 and Module 8 §8.1).
5. **Linear 4-Step Customer Journey**:
   - Detail the exact 4-step operational sequence from initial call to job completion.
6. **Pre-Seeded Conversational FAQ**:
   - Answer 4–5 hyper-specific local pricing, emergency SLA, and technical compatibility questions using `FAQPage` / semantic heading structures.

---

### **11.4 Internal Linking Circuit & Navbar Discipline**

* **The Topical Silo Circuit**: Link Homepage ➔ Tier 1 Category Pillar ➔ Tier 2 Atomic Sub-Services, with bidirectional links back to the parent pillar and lateral links to 2–3 related sub-services.
* **Ban on 100-Link Megamenu Bloat**: Keep global navigation lean (maximum 10–15 top-level links). Dividing internal PageRank across 100+ footer/header links starves primary revenue pages of ranking equity (Module 8 §8.3).
* **Service Page Conversion Parity (Module 7 §7.11 & [`kirby-text-first-cro`](../../kirby-text-first-cro/SKILL.md) §21.1; *(layout, CTA and pricing bullets: directional, single-source heuristic; Credentials & Proof and the PII/coverage rules below are mandatory house rules per §7.11)*):**
  * *Scope & Subpage Split:* Pair every Core 30 Problem-to-Deliverable Scope Table with an explicit **What's Included / What Isn't** exclusion boundary and, only where intents genuinely differ with unique scope content, **Intent-Split subpages** (`repairs` / `servicing` / `new installs`; or link existing Tier 2 pages), banning `3,000`-word informational blog walls on commercial service URLs.
  * *First-Screen Conversion Chrome:* Pair dual **Call + Book Online** first-screen buttons (for Stage 2 Core 30 pages, except [`kirby-text-first-cro`](../../kirby-text-first-cro/SKILL.md) §6.3 premium/high-status CTA withholding; single primary CTA remains valid for Module 4 §4.2 Day-1 5-page Service Page 1 unless Stage 2 conversion parity is applied) with **"From"** price + next live booking slot (never fabricated; omit if no live source) and the Linear 4-Step Customer Journey above (§21.1 item 4's 3-step scope block is an optional compact variant that does not replace the 4-step journey).
  * *Credentials & Proof:* Display real regulator-published trade accreditation numbers (`Gas Safe`, `SRA`, `GDC` where applicable + verified technician names/photos with consent per Module 6 §6.7).
  * *Local Coverage Widget & Tier Scoping:* Pair an interactive **zip/postcode lookup (matching Gate 0-served areas with no unneeded PII retention) + local map** (banning 50-town footers while preserving Rule 7 neighbor links), scoping service+town `<h1>` — distinct from `<title>` — and postcode lookup to pages that target a named town (Tier 3 geo-hubs and town-specific local geo service pages per Module 3 §3.6); Tier 1/Tier 2 pages follow §11.3 item 1 as written.
