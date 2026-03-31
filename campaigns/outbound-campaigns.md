# Lansweeper — Outbound Campaigns

> Last updated: 2026-03-31
> Platform: SmartLead + Clay (EmailBison migration pending)
> LinkedIn: Heyreach

---

## Sync Update — 2026-03-31

**Smartlead API connected. 27 campaigns discovered. 2 NEW campaigns launched since init. Full copy extracted for active campaigns.**

### Metrics as of 2026-03-31

| ID | Campaign | Status | Leads | Sent | Replies | Interested | Bounced | Unsub |
|----|----------|--------|-------|------|---------|------------|---------|-------|
| 3105785 | LS: Past Champion | 🆕 Active | 107 | 0 | 0 | 0 | 0 | 0 |
| 3094531 | LS: MSPs [Ai Copy] EU | 🆕 Active | 2,335 | 609 | 3 | 0 | 2 | 13 |
| 2993068 | LS: Close-Lost | 🟢 Active | 1,010 | 2,350 | 29 | 8 | 56 | 0 |
| 2900594 | LS: Website Visitors | 🟢 Active | 1,325 | 4,566 | 39 | 0 | 89 | 0 |
| 3028566 | LS: IT Orgs EU | ✅ Done | 4,402 | 8,665 | 93 | 2 | 110 | 0 |
| 2911913 | LS: IT Orgs US | ✅ Done | 5,211 | 10,223 | 65 | 1 | 237 | 0 |
| 2912101 | LS: MSPs US | ✅ Done | 2,190 | 4,348 | 13 | 0 | 55 | 0 |
| 3028996 | LS: Intent Data | ✅ Done | 288 | 576 | 0 | 0 | 0 | 0 |
| 2953821 | LS: EOLS | ✅ Done | 1,226 | 2,434 | 4 | 0 | 33 | 0 |

**Change vs 2026-03-30 (init):** Smartlead API now connected — first time seeing actual metrics. 2 new campaigns launched. Close-Lost confirmed as #1 performer at 2.9% reply rate. Intent Data confirmed as failure (0 replies).

---

### NEW — LS: Past Champion (Campaign 3105785)

_Just launched 2026-03-30. 107 leads, 0 sent yet. 2-step sequence._

#### Email 1 — Past Champion Reconnect

**Subject:** `Congrats on {{New Company}}, {{First Name}}`

**Body (spintext):**
```
{Hi|Hey|Hello} {{first_name}},

{Saw you moved to|Noticed you joined|Saw you recently joined} {{new company}} - {congrats on the new role|congratulations on the move|congrats on the transition}.

I {spoke with|was chatting with|connected with} {{Account Manager}} and {{Gender}} {told me|mentioned|shared} how quickly your team at {{company_name}} {got value out of|saw results with|started benefiting from} Lansweeper.

{Curious how|I'd love to hear how} {IT asset visibility|asset discovery and compliance|infrastructure visibility} {looks at|is shaping up at|is being handled at} {{new company}}. {Might be worth|Could be worth|Would it be worth} a quick {chat|conversation|call} to see if there's a fit?
```

#### Email 2 — Follow-up

**Subject:** (same thread)

**Body (spintext):**
```
{Hi|Hey|Hello} {{first_name}},

I know {onboarding at a new company keeps you busy|starting a new role can be hectic|the first few weeks at a new company are always packed}.

If {IT asset visibility, compliance tracking, or infrastructure discovery|asset visibility, compliance management, or infrastructure discovery|IT asset tracking, compliance monitoring, or network discovery} ever {becomes a priority|comes up as a focus|lands on your radar} at {{new company}}, {I'd be happy to|would love to|I'd welcome the chance to} {reconnect|catch up|have a quick call}.

{A lot has changed|Lansweeper has evolved significantly|We've shipped a lot} since your time at {{company_name}}.
```

---

### NEW — LS: MSPs [Ai Copy] EU (Campaign 3094531)

_Launched 2026-03-27. 2,335 leads, 609 sent, 3 replies, 13 unsubscribes._

#### Email 1 — AI-generated (Clay variable)

**Subject:** `{{Subject Line}}` (personalized per lead via Clay)
**Body:** `{{Email-1}}` (AI-generated per lead)

_Note: This campaign uses Clay AI to generate personalized copy per lead. No static template — each email is unique. Monitor reply quality to assess AI copy effectiveness._

**Early concern:** 2.1% unsubscribe rate (13 unsubs on 609 sent). EU compliance requires clear opt-out — review unsubscribe language positioning.

---

### LS: Close-Lost (Campaign 2993068) — NO COPY CHANGE

_Best performer. 2.9% reply rate, 8 interested. 3-step sequence. Continue as-is._

**Copy summary:**
- Email 1: "Lansweeper has changed since {{company_name}} last looked" — platform evolution hook, rebuilt UI, AI search, BI dashboards
- Email 2: "How Itron got visibility across 20 offices in weeks" — case study with 32,000 assets / ServiceNow integration
- Email 3: Soft breakup — "timing is everything" + leave door open

---

### LS: Website Visitors (Campaign 2900594) — CLASSIFICATION FIX NEEDED

_1.7% reply rate but 0 interested. Slack shows positive replies (Greg Emmerson pricing inquiry). Smartlead interested classification may not be configured or replies not being tagged._

---

---

## Copy Optimization — 2026-03-31

### Architecture Note

Most Lansweeper campaigns use **Clay AI-generated copy** — each lead gets a unique `{{Email-1}}` and `{{Subject Line}}` dynamically. The only campaigns with static Smartlead templates are **Close-Lost** and **Past Champion**. For Clay campaigns, the "copy to optimize" is the **framework/prompt** that Clay uses, not a static template.

---

### Campaign: LS: Close-Lost — Email 1 — NO CHANGE RECOMMENDED

_2.9% reply rate. 8 interested. Best performer by far. Do not touch._

**Why it works:**
- "Lansweeper has changed" hook creates curiosity/FOMO without re-pitching from scratch
- Specific product updates (rebuilt UI, AI search, BI dashboards, ISO 27001) signal momentum
- Compliance angle as secondary hook catches regulated industries (Banque BEMO asked about on-prem + AI)
- Soft "15-minute look" CTA — low friction
- Itron case study in Email 2 (32,000 assets, 20 offices, ServiceNow) adds concrete proof

---

### Campaign: LS: Close-Lost — Email 2 — NO CHANGE RECOMMENDED

_Itron case study is landing. Keep as-is._

---

### Campaign: LS: Close-Lost — Email 3 — NO CHANGE RECOMMENDED

_Soft breakup. Effective as a door-open. No data suggesting it needs change._

---

### Campaign: LS: EOLS [Ai Copy] — Email 1 — REWRITE RECOMMENDED

**Diagnosis:** 0.3% reply rate on 1,226 leads. Completed with only 4 replies, 0 interested. The end-of-life systems angle (Windows 10/11/Server) is failing. The PS line ("our discovery is agentless and won't disrupt fragile legacy systems") leads with a defensive reassurance — it signals worry, not value. The Clay AI prompt framework likely focuses too narrowly on EOLS urgency without connecting to broader pain points.

**Campaign is completed — apply learnings to next EOLS variant if relaunched.**

---

#### BEFORE (ran as of March 2026):
**Subject:** `{{Subject Line}}` (Clay AI — likely EOLS-focused)

**Body:**
```
{{Email-1}} [Clay AI-generated — end-of-life systems focus]

PS Our discovery is fully agentless and won't disrupt fragile legacy
systems. If this isn't relevant on your end, feel free to let me know.
```

**Problems:**
1. EOLS urgency alone doesn't trigger action — IT teams already know their EOL dates
2. PS leads with fear ("won't disrupt fragile systems") — plants doubt instead of removing it
3. No case study or proof point
4. No connection to what happens *after* discovery (compliance, reporting, action)

---

#### AFTER (suggested 2026-03-31):
**Subject:** `{your eol exposure | what's still running Windows 10 at {{company_name}}}`

**Body:**
```
Hi {{first_name}},

Quick question — does {{company_name}} have full visibility into which
devices are still running Windows 10, Server 2012, or other end-of-life
systems?

Most IT teams we talk to know the deadline is coming but don't have a
reliable count. Qarmet used Lansweeper to identify 2,000+ devices for
upgrade in days — 1,200 flagged for immediate replacement — which got
their budget approved faster than expected.

Takes about 15 minutes to see how it works on your environment.
Worth a look?

PS: Fully agentless — nothing to install, nothing to disrupt.
```

**What changed and why:**
- **Hook:** Changed from generic EOLS urgency to a specific question ("do you have full visibility?") — mirrors the "what's on your network" angle that works in Close-Lost
- **Body:** Added Qarmet case study (2,000+ devices, 1,200 replacements, budget approval) — concrete proof from the case studies doc
- **CTA:** "See how it works on your environment" — actionable, not vague
- **PS:** Kept agentless reassurance but made it a brief aside, not the lead

**Machine-readable diff:**
```json
{
  "campaign_id": 2953821,
  "email_step": 1,
  "sync_date": "2026-03-31",
  "changes": {
    "subject": { "before": "{{Subject Line}} (Clay AI)", "after": "your eol exposure | what's still running Windows 10 at {{company_name}}" },
    "hook": { "before": "Clay AI EOLS urgency", "after": "Specific question about visibility into EOL devices", "reason": "EOLS urgency alone didn't work (0.3%). Visibility question mirrors Close-Lost's successful 'has changed' curiosity hook" },
    "body": { "before": "Clay AI + defensive PS", "after": "Visibility question → Qarmet case study → 15-min CTA", "reason": "Added concrete proof (Qarmet: 2,000 devices, budget approval) and shifted from fear to value" },
    "cta": { "before": "Unknown (Clay)", "after": "See how it works on your environment", "reason": "Specific and actionable vs generic" }
  }
}
```

---

### Campaign: LS: MSPs [Ai Copy] US — FRAMEWORK REWRITE

**Diagnosis:** 0.6% reply rate on 2,190 leads. 13 replies, 0 interested. MSP segment consistently underperforms IT orgs (0.6% vs 1.2-2.1%). The Clay AI framework for MSPs is likely using generic "managed service" language. MSPs respond better to peer proof (other MSPs) and scalability angles.

**Campaign is completed — apply to MSPs EU (active) and future MSP campaigns.**

---

#### BEFORE — Clay AI Framework (inferred from campaign structure):
```
Clay generates {{Subject Line}} and {{Email-1}} per lead.
Framework likely focuses on: MSP visibility challenges, tool
consolidation, multi-client management.
No static PS or case study anchor.
```

**Problems:**
1. No MSP-specific case study in the prompt (Acora: 300+ environments, B2B Cyber Secure: government ministries)
2. Likely using IT org language, not MSP language ("your environment" vs "your clients' environments")
3. No mention of PSA/RMM integration — MSPs care about tool chain, not standalone discovery
4. No scalability proof — MSPs need to see "works across 300+ environments" not "works for 1 company"

---

#### AFTER — Recommended Clay AI Framework for MSP campaigns:

**Prompt framework for Clay:**
```
Write a cold email to an MSP owner/technical director.

HOOK (choose one based on signals):
- If growing client count: "As you scale past [X] clients, do you have
  standardized discovery across all environments?"
- If security-focused: "How quickly can you generate a compliance-ready
  asset inventory for any client?"
- Default: "How many of your client environments have complete asset
  visibility right now?"

BODY REQUIREMENTS:
- Reference MSP-specific case study: "Acora standardized asset inventory
  across 300+ managed environments without manual rework"
- OR: "B2B Cyber Secure delivers compliance-ready inventories in minutes,
  even for estates of 100,000 assets"
- Mention PSA/RMM integration: "feeds clean data into your existing
  PSA/RMM toolchain"
- Use MSP language: "your clients' environments", not "your environment"

CTA: "Worth a quick look at how [similar MSP] did it?"

TONE: Peer-to-peer. Short sentences. No product brochure language.
```

**Machine-readable diff:**
```json
{
  "campaign_id": "MSP_framework",
  "email_step": 1,
  "sync_date": "2026-03-31",
  "changes": {
    "hook": { "before": "Generic MSP visibility", "after": "Scalability question tied to client count", "reason": "MSPs think in terms of client environments, not their own. 0.6% reply rate shows generic hook isn't landing." },
    "body": { "before": "No MSP case study", "after": "Acora (300+ environments) or B2B Cyber Secure (100K assets)", "reason": "MSP case studies from Drive doc not being used. These are the strongest MSP proof points." },
    "cta": { "before": "Generic demo ask", "after": "Peer reference CTA", "reason": "MSPs respond to peer proof more than feature demos" }
  }
}
```

---

### Campaign: LS: Website Visitors — NO COPY CHANGE

_1.7% reply rate — copy is working. The issue is 0 leads marked "interested" in Smartlead despite clearly positive replies in Slack (Greg Emmerson pricing inquiry, etc.). This is a **classification/workflow issue**, not a copy issue. Fix the Smartlead interested-tagging workflow._

---

### Campaign: LS: IT Organizations [Intent Data] — KILL AND DON'T REPEAT

_0% reply rate on 288 leads. Intent data signals (likely Bombora or similar) without strong personalized copy produced zero engagement. If intent data is revisited, it must be paired with the Close-Lost style copy (specific product updates, case studies, compliance hooks) — not generic AI copy._

---

### Campaign: LS: MSPs [Ai Copy] EU — MONITOR + UNSUB FIX

_Only 609 sent, too early for copy judgment. But 13 unsubscribes (2.1%) is high. Immediate action: review unsubscribe text placement and EU opt-out compliance language. Consider adding a clear "PS: If this isn't relevant, just reply and I'll remove you" instead of a formal unsubscribe link — reduces spam flags._

---

### Targeting Changes — 2026-03-31

#### Close-Lost — NO CHANGE
_Keep targeting. Feed more leads from Salesforce closed-lost pipeline._

#### MSPs — TIGHTEN
**BEFORE:** MSPs of all sizes and types
**AFTER:** MSPs managing 10+ client environments, security-focused, hiring technicians, US + UK + EU
**Remove:** Solo IT consultants, MSPs under 5 clients
**Evidence:** 0.6% US / 0.5% EU early — broad targeting dilutes signal. Case studies (Acora, Krome) are mid-market MSPs.

#### IT Orgs — SPLIT BY VERTICAL
**BEFORE:** All IT organizations 1,000+ employees
**AFTER:** Split into vertical-specific campaigns:
- Manufacturing (strongest: Rentokil, Hitachi Energy, Bekaert, Qarmet case studies)
- Financial Services (Banque BEMO reply confirms demand for on-prem + AI)
- Education (University of York £300K saved, University of Derby Cyber Essentials)
**Evidence:** EU outperforms US 2:1. Vertical-specific hooks and case studies should increase relevance.

```json
{
  "sync_date": "2026-03-31",
  "targeting_changes": {
    "msp_campaigns": {
      "remove_segments": ["solo IT consultants", "MSPs under 5 clients"],
      "add_signals": ["hiring technicians", "adding security services", "growing client count"],
      "evidence": "0.6% reply rate on broad MSP targeting. Case studies are mid-market MSPs."
    },
    "it_org_campaigns": {
      "split_into": ["Manufacturing", "Financial Services", "Education"],
      "add_signals": ["vertical-specific compliance triggers", "M&A activity for manufacturing"],
      "evidence": "EU 2.1% vs US 1.2%. Vertical-specific case studies available for all 3."
    }
  }
}
```

---

### Interested Replies — 2026-03-31

_No new replies since 2026-03-30 Slack data. Same reply set as init. See init section below._

> Added: 2026-03-31
> Sender persona: "Lana"

---

## Sync Update — 2026-03-30

**Note: This is the initial brain file creation, not a sync update. Campaigns are running on SmartLead — email copy not available in EmailBison. Reply data sourced from Slack #lansweeper-outbound-replies-it.**

### Campaign Overview as of 2026-03-30

| ID | Campaign | Channel | Status | Notes |
|----|----------|---------|--------|-------|
| — | LS: IT Organizations [Ai Copy] | Email | Active | US targeting, enterprise IT orgs 1000+ employees, AI-generated copy |
| — | LS: IT Organizations [Ai Copy] EU | Email | Active | European targeting, same segment |
| — | LS: Close-Lost | Email | Active | Reactivating Salesforce closed-lost deals from last 6 months |
| — | LS: Website Visitors | Email | Active | Triggered by website visitor deanonymization via Clay |
| — | IT - Indirect | LinkedIn | Active | Via Heyreach, targeting IT decision-makers |
| — | Website Visitor (A) | LinkedIn | Active | Via Heyreach |
| — | Website Visitor (B) | LinkedIn | Active | Via Heyreach |

**Overall positive reply rate:** ~0.7% (per 2026-03-20 sales alignment call)

**Email copy status:** Not available — campaigns on SmartLead, not yet migrated to EmailBison. Sales team (Henry, Brad) have requested shorter, more impactful messaging.

---

### Copy Notes from Calls

From 2026-03-20 Sales Team Alignment call:
- Current copy uses AI-generated messaging
- Sales team wants **shorter, more impactful** messaging
- Primary lead source: Apollo database, companies 1000+ employees
- Decision-maker criteria kept consistent across campaigns for testing simplicity
- European campaigns include unsubscribe links; US campaigns use opt-out language
- Privacy policy links in European email signatures only
- Website visitor campaign uses **14-day PoC + personalized demo** as lead magnet

From 2026-01-28 Sync:
- Slow ramp-up: 5 additional emails every 2 days
- Two main streams: general IT/MSP segment + end-of-life technology campaign
- LinkedIn outreach targets highly active decision-makers, adapting messaging based on email insights

---

### Interested Replies — 2026-03-30

Summary: Strongest engagement from Close-Lost campaign. IT Directors, CIOs, and IT Systems Managers responding positively. Industrial security and financial services showing OT/on-prem interest.

| # | Person | Title | Company | Industry | Campaign | Channel | Reply Summary |
|---|--------|-------|---------|----------|----------|---------|---------------|
| 1 | Enrique Martín García | — | Titanium Industrial Security | Industrial Cybersecurity | LS: Close-Lost | Email | Interested in Lansweeper OT updates, asked for product info |
| 2 | Vassilis Fotinias | IT Director | Danaos Shipping Co | Maritime/Shipping | LS: Close-Lost | Email | Forwarded to security expert Renat Mazaev for arrangement |
| 3 | Tony Lucarelli | — | IPPL | IT Services | LS: Close-Lost | Email | Still interested, budgeted, busy with server migration. Follow up later. |
| 4 | Deepak Chand | IT/IS Manager | FASTSIGNS | Retail/Franchising | LS: Close-Lost | Email | Wants to set up a meeting |
| 5 | Darren Marsden | CIO | West Brom Building Society | Financial Services | LS: IT Orgs EU | Email | Already evaluating Lansweeper through a vendor's proposal |
| 6 | Serge Ghawitian | IT Systems & Network Manager | Banque BEMO | Banking | LS: Close-Lost | Email | Interested if on-prem including AI. Key signal for financial services. |
| 7 | Rafa Hens | — | Aguas de Córdoba | Utilities | LS: Close-Lost | Email | Already purchased! Deciding between cloud vs on-prem. (Spanish) |
| 8 | Ronwald King | IT Director | CGI (APAC Philippines) | IT Consulting | LS: Close-Lost | Email | Active Lansweeper user, wants to maximize license — upsell opportunity |
| 9 | Greg Emmerson | — | Applegreen | Retail/Fuel | LS: Website Visitors | Email | Asked about cloud pricing for 12K assets. **FLAGGED: already a customer** |
| 10 | Nick C. | — | — | — | IT - Indirect | LinkedIn | Will stop by booth at RSA Conference |
| 11 | Art Thompson | — | — | — | Website Visitor (A) | LinkedIn | Positive — will register on website |
| 12 | Cagatay Zavazar | — | Siberlock | Cybersecurity | LS: Close-Lost | Email | Interested but very busy. Timing issue, not target issue. |
| 13 | Renee Hough | Director CTE | Putnam County School District | Education (K-12) | LS: IT Orgs | Email | Redirected to IT Director Lenon Harvey — referral lead |

**Neutral / Not Now:**
- Rigo Lopez (CCUSD) — budget constraints, reconnect July
- Stephanie Williams (Greenville K-12) — polite decline, keeping info
- Josh Galland (Miro) — auto-forward
- Mauricio Correa (Itaú) — shared new contact info only

> Added: 2026-03-30
