# Module 12: Continuous-Take Video Verification, Address Denial Recovery & Support Governance

*Source: Caleb Ulku ("STOP Creating Google Business Profile Wrong! (2025)" & "Google Business Address Change DENIED? (Quick Fix)") and Whitespark Local Update E41 & E50. October 2026.*

Google’s automated verification algorithms reject over 60% of initial profile verifications and routinely deny address updates, trapping unprepared business owners in suspension loops. Furthermore, Google updated its official terms to penalize aggressive or repetitive support ticket submissions.

This module is the **single canonical source of truth** for the 3-phase continuous-take video verification script, address change pre-checks, SAB centroid defense, and Google Support escalation hygiene.

---

### **12.1 The 3-Phase Continuous-Take Video Verification Blueprint**

*(Note: This module codifies the general execution script for passing Google's live mobile video verification. For DBA name-verification paperwork, see Module 3 §3.3.1; for multi-city technician van scaling, see Module 6 §6.8).*

Even when operating as a Service Area Business (SAB) with a hidden address, Google requires a verifiable physical residential or commercial base—PO Boxes, UPS Stores, and virtual offices (Regus/WeWork) are automatically rejected. To pass video verification on the first attempt, record a **single, continuous, unedited 90-to-120-second video** (with mobile GPS location services enabled) executing three sequential proof phases:

```
┌─────────────────────────────────────────────────────────────────────────┐
│            3-PHASE CONTINUOUS-TAKE VIDEO VERIFICATION SCRIPT            │
├─────────────────────────────────────────────────────────────────────────┤
│ Phase 1: Exterior & Street Sign Anchor (0:00 – 0:30)                    │
│          - Start outside on the public street                           │
│          - Film official municipal street sign & adjacent properties    │
│          - Pan continuously to the building/house number on premises    │
│                                                                         │
│ Phase 2: Operational & Vehicle Control Proof (0:30 – 1:00)              │
│          - Walk to the parked service vehicle on the driveway/lot       │
│          - Show branded vehicle signage / magnetic decals clearly       │
│          - Physically lock and unlock the vehicle using the key fob     │
│            or unlock the front premises door with a physical key        │
│                                                                         │
│ Phase 3: Specialized Tooling & Legal Paperwork (1:00 – 2:00)            │
│          - Open the vehicle/workspace to film trade tools & hardware    │
│          - Film official printed invoices, utility bill, and government │
│            registration matching the EXACT business name on GBP         │
└─────────────────────────────────────────────────────────────────────────┘
```

* **Zero Human Faces or License Plates**: Avoid filming bystanders' faces or third-party vehicle license plates, which can trigger automated privacy rejections during Google's review processing.
* **The Key Fob Control Test**: Google reviewers specifically look for active proof of possession—pressing the key fob to flash the hazard lights and open the service van (or turning a physical deadbolt key in the office door) proves you are not filming a stranger's building or vehicle from the street.

---

### **12.2 Address Change Denial Prevention & Ghost-Listing Pre-Check**

*Source: Caleb Ulku ("Google Business Address Change DENIED? (Quick Fix)").*

Submitting an address change without pre-validating the target address in Google’s spatial database is a primary cause of instant profile suspension:

1. **Step 1: The Google Maps Ghost-Listing Audit**:
   - Before touching your GBP address field, search the exact target street address on Google Maps.
   - Check whether a previous tenant, defunct company, or duplicate business listing still occupies that address pin (especially in the same primary category). If an active or suspended profile shares your category at that coordinate, Google's duplicate-collision filter will deny your update or suspend your profile.
   - Submit a *"Suggest an edit -> Moved / Permanently Closed"* on defunct prior-tenant listings and wait for removal before moving your profile.
2. **Step 2: Pre-Seeding External Proof (14-Day Window)**:
   - Update your website footer, contact page, `LocalBusiness` JSON-LD schema, utility bills, and government registry with the new address at least 14 days prior to editing GBP (following the Module 9 §9.1 cadence and [`kirby-seo-deployment`](../../kirby-seo-deployment/SKILL.md) Module 20 §20.4).

---

### **12.3 SAB Map Pin Centroid Mechanics & Manipulation Defense**

*Source: Whitespark Local Update E41 (Darren Shaw & Amy Toman).*

* **The Hidden SAB Centroid Problem**: Although an SAB hides its physical street address from the public, Google still anchors the profile’s ranking radius to the internal map pin of the verification address. Occasionally, Google’s geocoder misplaces an SAB pin miles away from its true operational base.
* **The URL Parameter Pin Exploit & Sabotage Risk**: By appending specific map data parameters (`data=!10m...`) to a Google Maps search result URL, users can expose a hidden *"Suggest an edit -> Wrong pin location"* interface that permits dragging an SAB’s invisible pin.
* **Defensive Mandate**: Malicious competitors use this vector to drag a rival SAB’s centroid into an ocean, forest, or distant postcode, destroying their local pack rankings overnight. Enforce continuous coordinate drift monitoring via [`kirby-seo-telemetry`](../../kirby-seo-telemetry/SKILL.md) Module 10 and Module 14 to detect and revert unauthorized centroid shifts immediately.

---

### **12.4 Google Policy Alert: "Misuse of Support Channels"**

*Source: Whitespark Local Update E50 (Darren Shaw).*

Google officially updated its Google Business Profile policies to classify **"Misuse of Support Channels"** as a policy violation carrying account-level penalties:

* **Prohibited Conduct**: Submitting multiple simultaneous reinstatement or verification tickets for the same profile, spamming support forums, or using abusive/hostile language toward Google support representatives.
* **Enforcement Penalty**: Google blacklists the submitting Google account from support channels and places the associated Business Profile into permanent unappealable restriction.
* **The Single-Dossier Escalation Rule**: When appealing a suspension, denied edit, or missing review batch, compile a **single, comprehensive Google Drive folder** containing all legal registrations, utility bills, exterior/equipment photos, and transaction proofs. Submit **one ticket**, record the Case ID, and wait for the complete SLA window before escalating to the Google Business Profile Community Product Experts.
