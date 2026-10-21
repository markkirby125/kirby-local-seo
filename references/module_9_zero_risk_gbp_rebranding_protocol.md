# Module 9: The Whitespark Zero-Risk GBP Rebranding & Name Change Protocol

*Source: Darren Shaw / Whitespark ("What Google Won't Tell You About Rebranding Your Business Profile" & E28 "Disappearing Reviews, New Business Name Policy"). October 2026.*

When acquiring, renaming, or rebranding a local business (e.g., transitioning from a regional umbrella name to a city-focused trading name), following Google’s official documentation is a catastrophic trap. Google’s documentation instructs owners to mark the existing profile as *"Permanently Closed"* and create a brand-new profile. **Doing so permanently destroys all accumulated review equity, historical longevity badges, and local ranking momentum.**

This module codifies the exact 5-phase operational sequence to rebrand an existing Google Business Profile safely without triggering algorithmic suspensions, forced video reverifications, or review stripping.

---

### **9.1 The "Update the Web First" Doctrine & Sitewide Crawl Trigger**

Never touch the Google Business Profile dashboard as the first step of a rebrand. Whenever a sensitive field is modified on a GBP, Google immediately dispatches automated verification bots to crawl the linked website and cross-reference third-party data aggregators. If the GBP displays the new business name while the linked website, schema, and social directories still display the old identity, Google flags the edit as an unauthorized profile hijacking and suspends the listing.

```
┌─────────────────────────────────────────────────────────────────────────┐
│              ZERO-RISK GBP REBRANDING OPERATING SEQUENCE                │
├─────────────────────────────────────────────────────────────────────────┤
│ Phase 1: Real-World Legal Entity & Document Preparation                 │
│          - Register legal trading name / DBA / Companies House          │
│          - Update utility bills, business insurance, and bank records   │
│                                                                         │
│ Phase 2: Complete Web Footprint Modernization (BEFORE TOUCHING GBP)     │
│          - Deploy new domain/landing page with updated NAP & Schema     │
│          - Update Facebook Business Page, LinkedIn, Yelp, Yell, BBB     │
│          - Synchronize primary data aggregators (Data Axle, Localeze,   │
│            Foursquare)                                                  │
│                                                                         │
│ Phase 3: The Mandatory 14-Day Indexing Buffer                           │
│          - Wait a strict 14-day window for Googlebot to crawl & index   │
│            the updated web citations and website schema                 │
│                                                                         │
│ Phase 4: Staggered Sensitive Field Update on GBP (Primary Owner Only)   │
│          - Log in strictly via PRIMARY OWNER account (Never Manager)    │
│          - Execute strictly one sensitive field change per week:        │
│            * Week 1: Website URL                                        │
│            * Week 2: Business Name                                      │
│            * Week 3: Primary Category / Phone Number                    │
│                                                                         │
│ Phase 5: Media Cleanse & Secondary Citation Sweep                       │
│          - Delete obsolete logos, old signage, and former staff photos  │
│          - Upload 15–20 authentic photos reflecting the new brand       │
└─────────────────────────────────────────────────────────────────────────┘
```

1. **Website & Schema Modernization (Priority #1)**:
   - Update the visible business name, address, and phone number (NAP) across the header, footer, and contact page of the linked website.
   - **Critical Schema Check**: Audit the page source for `LocalBusiness` JSON-LD structured data. Forgetting to update the `name` and `url` properties inside the JSON-LD schema while updating visible HTML text causes instant verification rejection during Google's sitewide crawl.
2. **The Facebook & Tier-1 Directory Cross-Check**:
   - Google heavily weights the **Facebook Business Page**, **Yelp**, **Better Business Bureau (BBB)** / UK equivalents (**Yell.com**, **Scoot**, **Companies House**), and primary data aggregators (**Data Axle**, **Neustar Localeze**, **Foursquare**) as external trust anchors. Update all Tier-1 profiles to match the new brand identity before touching GBP.
3. **The Mandatory 14-Day Indexing Buffer**:
   - After updating the website and Tier-1 directories, **wait a minimum of 14 days**. This allows Googlebot to recrawl the web ecosystem and update its internal entity graph so that when the GBP edit is submitted, Google’s automated check finds 100% corroboration across the web.

---

### **9.2 The Staggered Sensitive Field Cadence (1 Field Per Week)**

Submitting wholesale changes across multiple GBP fields simultaneously triggers Google's anti-hijacking fraud filters (designed to stop spammers from converting abandoned coffee shop profiles into locksmith listings).

1. **The Primary Owner Account Mandate**:
   - Always submit rebranding edits while logged into the Google account designated as the **Primary Owner** of the profile. Edits submitted by accounts with *"Manager"* permissions face significantly higher automated rejection and suspension rates.
2. **The 5 Sensitive Fields**:
   - Business Name
   - Primary Category
   - Physical Address
   - Primary Phone Number
   - Website URL
3. **The 7-Day Stagger Rule**:
   - Modify **only one sensitive field per week** (enforce a strict 7-day interval between edits).
   - **Recommended Cutover Sequence**:
     - *Day 1 (Post 14-Day Buffer)*: Update the **Website URL** field on GBP (linking to the updated domain or redirected landing page). Wait 7 days.
     - *Day 8*: Update the **Business Name** field to the new legal trading name. Wait 7 days.
     - *Day 15*: Update the **Phone Number** or **Primary Category** (only if required).
   - *Note*: Never change the physical address and the business name at the same time. For domain-level redirect and migration timing benchmarks, cross-reference [`kirby-seo-deployment`](../../kirby-seo-deployment/SKILL.md) Module 20 §20.4.

---

### **9.3 Google's Identity Change Policy & Review Retention Guardrails**

*Source: Whitespark Local Update E28 (Darren Shaw & Claudia Tomina).*

Google’s official **Identity Change Policy** (`support.google.com/business/answer/13762416`) governs whether a business is legally permitted to keep its historical reviews during a name change:

* **When Reviews Are Stripped (Concept/Ownership Reset)**: If a business changes its fundamental industry category, operational concept, or ownership without continuity (e.g., an Italian restaurant rebrands into a Mexican cantina, or a retail computer shop converts into a digital marketing agency), Google classifies it as a new business entity and strips all historical reviews.
* **The Legitimate Rebrand Exemption (100% Review Retention)**: If the business maintains the same core operational category, serves the same geographic market, and delivers the same core services under continuous management (e.g., *Berkshire IT Services* rebranding to *Ascot IT Services* while keeping `Computer Support and Services` as its primary category), the rebrand is fully policy-compliant and retains 100% of its historical reviews.
* **Visual Media Purge**: Immediately after the business name edit is approved, purge the GBP Photos tab of all legacy logos, old vehicle signwriting, and outdated premises signage. Upload 15–20 fresh, authentic operational photos showing the new brand identity. Photo additions and deletions do not trigger reverification flags.
