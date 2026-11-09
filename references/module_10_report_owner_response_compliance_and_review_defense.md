# Module 10: The "Report Owner Response" Button & Review Disappearance Defense

*Source: Caleb Ulku ("Google Reviews Just Added A New Button" & "Google Is Deleting Your Reviews (Even If They're Legit)") and Whitespark Local Update E44 & E28. October 2026.*

Google has introduced two aggressive enforcement mechanisms across the Google Business Profile review ecosystem: a public **"Report owner response"** button beneath every business reply, and an AI-driven review spam filter that routinely deletes legitimate 5-star customer reviews.

This module establishes the mandatory compliance guardrails for owner responses and the technical solicitation protocol that prevents legitimate reviews from being quarantined.

---

### **10.1 The "Report Owner Response" Trap & PII Prohibition**

Google placed a direct **Report owner response** action link beneath every public business reply on Google Maps and Search. Any user, disgruntled former employee, or competitor can flag an owner's response with two clicks across five violation categories:
1. Off-topic commentary
2. Profanity or vulgar language
3. Bullying or harassment
4. Discrimination or hate speech
5. **Personal Information (PII)**

```
┌─────────────────────────────────────────────────────────────────────────┐
│             OWNER RESPONSE COMPLIANCE & PII GUARDRAILS                  │
├─────────────────────────────────────────────────────────────────────────┤
│ ❌ STRICTLY PROHIBITED IN REPLIES (Triggers Deletion / Revocation)      │
│    - Customer surnames or full names (use the handle's first name only)  │
│    - Invoice numbers, billing amounts, or payment dispute details       │
│    - Specific project addresses, IP addresses, or network hardware info │
│    - Medical, dental, legal, or financial engagement specifics          │
│    - Hostile counter-accusations ("You refused to pay our £95 fee")     │
│                                                                         │
│ ✅ MANDATORY APOLOGETIC CONVERSION SCRIPT (Negative Reviews)            │
│    "We take client service standards seriously. Due to client privacy   │
│     policies, we do not discuss specific account details publicly.      │
│     Please contact our Managing Director at [Listed Phone Number]       │
│     so we can investigate and resolve this immediately."                │
└─────────────────────────────────────────────────────────────────────────┘
```

* **Structure, Not Verbatim Wording:** The script above is the minimum compliant structure (acknowledge, decline to discuss account details publicly, route offline). The wording is an example: vary phrasing between replies (Module 6 §6.6 bans repetitive corporate slop) and draft through [`kirby-gbp-review-replies`](../../kirby-gbp-review-replies/SKILL.md).
* **Phone Number Rule:** Insert `[Listed Phone Number]` only when the owner has opted in and the number matches the phone listed on the profile. Otherwise route with "contact us using the details on this profile". Never put an unlisted direct line in a public reply.
* **Reviewer Name Rule:** Use the reviewer's first name only, taken from their display handle. Use no name if the handle is not a first name or looks like a surname.
* **The Five-Figure Compliance Mistake**: When confronted with an unfair 1-star review, business owners frequently attempt to "prove the reviewer wrong" by citing internal records (*"John Smith, our logs show our engineer visited your Ascot office on Tuesday and you refused to pay Invoice #1042 for your firewall upgrade"*). Under Google's moderation policy—as well as UK GDPR and US HIPAA/OCR enforcement—confirming a customer's real identity, location, or transaction specifics in a public forum is classified as a severe **Personal Information (PII) breach**.
* **Enforcement Consequences**: Google’s automated moderation filter (Whitespark E28) scans owner responses before and after publication. Flagged responses are deleted, and repeated violations result in permanent revocation of owner reply privileges or full profile restriction.
* **The Public Audience Rule**: Never write a negative review response for the aggrieved reviewer. Write it exclusively for the next 100 prospective buyers evaluating your professionalism and accountability.

---

### **10.2 Why Legitimate Reviews Disappear & The 4G/5G Solicitation Protocol**

*Source: Caleb Ulku ("Google Is Deleting Your Reviews") & Whitespark E28.*

Google’s automated spam algorithms evaluate the metadata, network origin, and velocity of every incoming review. Legitimate 5-star reviews are systematically deleted when businesses violate five algorithmic triggers:

1. **The On-Premise Wi-Fi / IP Collision Trigger**:
   - Never ask a customer to leave a Google review while connected to your business Wi-Fi network, or while your field technician is connected to the customer's corporate Wi-Fi managing the GBP dashboard from the same IP address.
   - Matching IP subnets or identical GPS device clusters between the GBP administrator and the reviewer triggers an instant *"Self-Review / Fake Engagement"* quarantine.
   - **Operational Mandate**: Instruct customers to submit reviews from their mobile device over cellular data (**4G/5G**) or via a follow-up SMS/email 24–48 hours after the technician has left the premises.
2. **The Velocity Burst Filter**:
   - Exporting a CSV of 200 past clients and blasting them simultaneously produces 15–20 reviews in 48 hours followed by months of zero activity. Google’s anomaly detector flags sudden spikes above historical baseline velocity and purges the entire batch.
   - **Operational Mandate**: Use the rolling 30-day drip cadence (1–3 requests per day/week) established in Module 6 §6.6.
3. **Formatting & Link Quarantine Triggers**:
   - Reviews containing URLs, email addresses, phone numbers, currency symbols (`£`, `$`), or all-caps exclamation strings are automatically held in pending moderation.
4. **Zero-History Google Accounts**:
   - Reviews submitted from newly created Google accounts with zero prior Maps contributions carry a high rejection probability. Prioritize soliciting reviews from active Google Workspace users or established consumer accounts.
5. **ChatGPT-Scripted & AI-Templated Review Text (Eric Velch, `7q6eVp8TAmE`)**:
   - Providing customers with pre-written review templates or prompting review text through ChatGPT triggers Google's NLP synthetic-text classifiers, causing reviews to fail to stick or disappear during automated sweeps. Strictly ban pre-scripted AI review copy; use the natural two-variable prompt in Module 3 §3.1.1 D (*"mention the problem we fixed and your town in your own words"*).

---

### **10.3 Off-Platform Proof Ledger for Review Restoration**

When Google’s filter erroneously deletes legitimate customer reviews, submitting a generic support ticket fails unless backed by verifiable transaction proof:

* Maintain an internal **Review Evidence Ledger** tracking: (a) Screenshot of the published review (captured via automated weekly monitoring per [`kirby-seo-telemetry`](../../kirby-seo-telemetry/SKILL.md) Module 14), (b) Reviewer display name and date, and (c) Redacted work order or paid invoice number proving a genuine commercial transaction.
* Present this unified evidence package in a single support escalation (observing the Module 12 §12.4 single-ticket rule).
