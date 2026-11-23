# Module 9: The Whitespark GBP Rebranding & Name Change Protocol

*Source: Darren Shaw / Whitespark ("What Google Won't Tell You About Rebranding Your Business Profile" & E28 "Disappearing Reviews, New Business Name Policy"). October 2026.*

When renaming or rebranding a local business, including one acquired with its existing management kept in place (e.g., transitioning from a regional umbrella name to a city-focused trading name), the source's reported view is that the route in Google's documentation is costly: per the source, it instructs owners to mark the existing profile as *"Permanently Closed"* and create a brand-new profile, which the source reports loses accumulated reviews, longevity badges, and local ranking momentum.

This module codifies a 5-phase sequence for a genuine rebrand of an existing Google Business Profile. Its goal is to produce corroborating evidence (legal records, website, citations) before each GBP edit so Google can verify the change. It lowers, but does not remove, the risk of suspension, video reverification, or review loss.

**Eligibility gate — ownership continuity (run before any phase):** Proceed only if the §9.3 Legitimate Rebrand test holds: same primary category, same market, same core services, and continuity of operation (the same owner, or a new owner with the existing management still running the business). If the concept has changed, or ownership has changed with no continuing management, stop: this protocol does not apply, and the change follows Google's Identity Change Policy (§9.3).

---

### **9.1 The "Update the Web First" Doctrine & Sitewide Crawl Trigger**

Never touch the Google Business Profile dashboard as the first step of a rebrand. The source reports that a sensitive-field edit prompts Google to check the linked website and third-party data aggregators. If the GBP shows the new name while the website, schema, and directories still show the old identity, the edit lacks corroboration and the source reports it can be rejected or the listing suspended.

```
┌─────────────────────────────────────────────────────────────────────────┐
│                  GBP REBRANDING OPERATING SEQUENCE                      │
├─────────────────────────────────────────────────────────────────────────┤
│ Eligibility gate: §9.3 ownership-continuity test passed (else stop)     │
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
│            * Week 3: Phone Number (only if it changes)                  │
│                                                                         │
│ Phase 5: Media Cleanse & Secondary Citation Sweep                       │
│          - Delete obsolete logos, old signage, and former staff photos  │
│          - Upload 15–20 authentic photos reflecting the new brand       │
└─────────────────────────────────────────────────────────────────────────┘
```

1. **Website & Schema Modernization (Priority #1)**:
   - Update the visible business name, address, and phone number (NAP) across the header, footer, and contact page of the linked website.
   - **Critical Schema Check**: Audit the page source for `LocalBusiness` JSON-LD structured data. Forgetting to update the `name` and `url` properties inside the JSON-LD schema while updating visible HTML text can cause verification rejection (source's reported view).
2. **The Facebook & Tier-1 Directory Cross-Check**:
   - Google heavily weights the **Facebook Business Page**, **Yelp**, **Better Business Bureau (BBB)** / UK equivalents (**Yell.com**, **Scoot**, **Companies House**), and primary data aggregators (**Data Axle**, **Neustar Localeze**, **Foursquare**) as external trust anchors. Update all Tier-1 profiles to match the new brand identity before touching GBP.
3. **The Mandatory 14-Day Indexing Buffer**:
   - After updating the website and Tier-1 directories, **wait a minimum of 14 days**. This allows Googlebot to recrawl the web ecosystem and update its internal entity graph so that when the GBP edit is submitted, Google's check finds the new identity corroborated across the web.

---

### **9.2 The Staggered Sensitive Field Cadence (1 Field Per Week)**

The source reports that changing several sensitive fields at once resembles a profile takeover, which Google's checks exist to stop (e.g., spammers converting an abandoned coffee shop profile into a locksmith listing). One change per week lets each edit be verified against the §9.1 evidence.

1. **The Primary Owner Account Mandate**:
   - Always submit rebranding edits while logged into the Google account designated as the **Primary Owner** of the profile. Edits submitted by accounts with *"Manager"* permissions face higher rejection and suspension rates (source's reported view).
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
     - *Day 15*: Update the **Phone Number** (only if it changes).
   - *Owner confirmation*: Before each sensitive-field edit, show the business owner the exact old and new value and get their explicit confirmation. Do not submit on inferred consent (Owner Confirmation Gate in `00_dispatcher.md`).
   - *Note*: Do not change the Primary Category in a rebrand; a category change fails the eligibility gate (§9.3).
   - *Note*: Never change the physical address and the business name at the same time. For domain-level redirect and migration timing benchmarks, cross-reference [`kirby-seo-deployment`](../../kirby-seo-deployment/SKILL.md) Module 20 §20.4. Use §20.4 for redirect and migration timing only; its GBP cutover sequence no longer changes the Primary Category, and this module's eligibility gate governs any field change.

---

### **9.3 Google's Identity Change Policy & Review Retention Guardrails**

*Source: Whitespark Local Update E28 (Darren Shaw & Claudia Tomina).*

Google’s official **Identity Change Policy** (`support.google.com/business/answer/13762416`) governs whether a business is legally permitted to keep its historical reviews during a name change:

* **When Reviews Are Stripped (Concept/Ownership Reset)**: If a business changes its fundamental industry category, operational concept, or ownership without continuity (e.g., an Italian restaurant rebrands into a Mexican cantina, or a retail computer shop converts into a digital marketing agency), Google classifies it as a new business entity and strips all historical reviews.
* **The Legitimate Rebrand Exemption (Review Retention)**: If the business maintains the same core operational category, serves the same geographic market, and delivers the same core services under continuous management (e.g., *Berkshire IT Services* rebranding to *Ascot IT Services* while keeping `Computer Support and Services` as its primary category), the rebrand fits the policy and is expected to keep its historical reviews.
* **Visual Media Purge**: Immediately after the business name edit is approved, purge the GBP Photos tab of all legacy logos, old vehicle signwriting, and outdated premises signage. Upload 15–20 fresh, authentic operational photos showing the new brand identity. The source reports that photo changes are not sensitive-field edits (reported, single-source, unverified).
