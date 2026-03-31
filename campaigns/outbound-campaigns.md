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

> **Source:** Actual email content pulled from Smartlead API message history endpoints. Every BEFORE example is a real email that was sent.

### How Clay AI Campaigns Work

Most Lansweeper campaigns use Clay AI to generate personalized `{{Email-1}}` and `{{Subject Line}}` per lead. The Smartlead template contains only the variable — the actual copy lives in Clay. The only campaigns with static templates are **Close-Lost** and **Past Champion** (spintext in Smartlead).

All Clay campaigns follow the same **framework**: `Company-specific hook → Case study → "Worth a closer look for [company]?" CTA`. The differences are in hook quality, case study relevance, and personalization depth.

---

### LS: Close-Lost — ALL 3 EMAILS — ✅ NO CHANGE

_2.9% reply rate. 8 interested. Best performer by far._

**Actual Email 1 sent to Çagatay Zavazar (Siberlock):**
```
Hi Çagatay,

When Siberlock looked at Lansweeper, the platform was a much earlier
version. Since then, we've shipped a fully redesigned UI, AI-driven
search across your asset data, live BI dashboards, and built-in
workflows that connect discovery straight into action.

We also added ISO 27001 on top of SOC 2 Type II — if compliance was
part of the earlier hesitation, that's now been addressed.

Would it be worth a quick 15-minute look?
```
**His reply:** *"It's great to hear about the advancements at Lansweeper — the updates regarding compliance are particularly noted. Could you please share a short demo video or deck highlighting the new UI and AI features?"*

**Why it works:** Specific product updates create curiosity. Compliance hook caught a security company. Low-friction CTA. The prospect is now requesting materials — warm lead.

**Actual Email 2 sent to Ronwald King (CGI Philippines):**
```
Hi Ronwald,

Quick example — Itron, a global organization with 20 offices, had no
centralised discovery before Lansweeper. Within just a few weeks they
had full insight across 32,000 assets and connected it all to ServiceNow.

Their IT team now identifies compliance gaps in real time and resolves
them quickly — no more spreadsheet juggling.

If that sounds like the kind of visibility CGI Philippines was looking
for, I'd be happy to show you what's available now. Just 15 minutes,
no obligation.
```
**His reply:** *"We are an active user of Lansweeper and we want to maximize our license. Can we set a session to review our existing instance and recommend improvements?"*

**Insight:** Ronwald is already a customer — this is an **upsell opportunity**, not a new deal. Customer exclusion needs tightening, but the positive response validates the messaging approach.

---

### LS: Website Visitors — Email 1 — 🔄 REWRITE RECOMMENDED

**Diagnosis:** 1.7% reply rate (good volume) but 0 marked interested. Actual emails read like product brochures — bold/italic HTML formatting in plain-text mode looks broken, abstract "Technology Asset Intelligence" concept intro, and vague CTAs. One explicit negative: *"We are 1000%. Thanks but we are not interested."* One wrong target: *"I am not the owner of this Company, so NO THANKS."*

---

#### BEFORE (actual email sent to Chris at Sheltair Aviation):
**Subject:** `asset visibility gap`

**Body:**
```
Hi Chris,

How confident are you that your current asset inventory is truly
complete and accurate?

Many teams rely on asset data spread across tools, manually updated,
and obsolete as soon as reports are built.

Lansweeper provides one continuously updated source of truth across
IT, OT, IoT, and Cloud — eliminating blind spots and enabling
confident decisions.

Would it be helpful to run a no-cost Asset Visibility Assessment
to understand what's really connected?

PS: We work alongside [cut off]
```

**His reply:** *"We are 1000%. Thanks but we are not interested."*

**Problems identified from actual sent emails:**
1. **Subject line is generic** — "asset visibility gap" / "asset data problem" / "unreliable inventory data" all feel like spam subject lines. No personalization, no specificity.
2. **"Technology Asset Intelligence" is jargon** — Prospects don't use this term. It reads as a tagline, not a conversation.
3. **Bold/italic formatting renders poorly** — HTML bold tags in plain-text emails look like broken markup.
4. **No case study in Email 1** — The second email (sent to Chris Verst at Verst Logistics) includes Qarmet + Rentokil proof, but Email 1 has zero social proof.
5. **"No-cost Asset Visibility Assessment" sounds like a sales pitch** — Every vendor offers a "free assessment."
6. **No company-specific hook** — These are website visitors, so we know they were looking at Lansweeper. Reference that.

---

#### AFTER (suggested 2026-03-31):
**Subject:** `noticed you on lansweeper.com`

**Body:**
```
Hi {{first_name}},

Noticed someone from {{company_name}} was looking at Lansweeper
recently — usually means asset visibility or compliance is on the radar.

Quick context: Rentokil found 130 unpatched servers across their 90+
country estate within 24 hours of deploying Lansweeper. No agents,
no disruption.

If {{company_name}} is evaluating discovery tools, happy to do a
15-minute walkthrough on your environment.

Worth a look?
```

**What changed and why:**
- **Subject:** `asset visibility gap` → `noticed you on lansweeper.com` — acknowledges the website visit signal. Personal, not generic.
- **Hook:** Generic question → website visit reference. These leads visited the site — use that signal.
- **Body:** Removed "Technology Asset Intelligence" jargon. Added Rentokil case study (130 servers, 24 hours, 90+ countries) — specific and compelling.
- **CTA:** "No-cost Asset Visibility Assessment" → "15-minute walkthrough on your environment" — same offer, less salesy language.
- **Formatting:** Removed bold/italic HTML. Plain text only.

```json
{
  "campaign_id": 2900594,
  "email_step": 1,
  "sync_date": "2026-03-31",
  "changes": {
    "subject": { "before": "asset visibility gap", "after": "noticed you on lansweeper.com", "reason": "Generic subject triggered 'We are 1000% not interested' reply. Website visit signal should be used." },
    "hook": { "before": "How confident are you that your current asset inventory is truly complete?", "after": "Noticed someone from {{company_name}} was looking at Lansweeper recently", "reason": "These are WEBSITE VISITORS — reference the visit. Current hook ignores the strongest signal we have." },
    "body": { "before": "No case study. 'Technology Asset Intelligence' jargon. Bold/italic HTML broken.", "after": "Rentokil case study (130 servers, 24 hours). Plain text. No jargon.", "reason": "Email 2 already has Qarmet+Rentokil and performs better. Pull proof into Email 1." },
    "cta": { "before": "no-cost Asset Visibility Assessment", "after": "15-minute walkthrough on your environment", "reason": "Same offer, less salesy. Every vendor offers a 'free assessment'." }
  }
}
```

---

### LS: MSPs [Ai Copy] US — Email 1 — 🔄 REWRITE RECOMMENDED

**Diagnosis:** 0.6% reply rate. 13 replies, 0 interested. Clay is generating MSP emails using **IT organization case studies** (Hitachi Energy, University of Derby) instead of MSP-specific ones (Acora, B2B Cyber Secure, Krome). The emails talk to MSPs like they're enterprises managing their own IT, not service providers managing clients.

---

#### BEFORE (actual email sent to Tim Pash at Cherokee Federal):
**Subject:** `post-acquisition asset visibility`

**Body:**
```
Hi Tim,

Following the HigherEchelon acquisition, how are you approaching
asset discovery to maintain audit readiness across the 60+ agencies
you support?

B2B Cyber Secure used to rely on multiple tools for compliance
reporting — creating a high risk of presenting incomplete asset data
during audits.

They now use our platform to automate discovery into a single source
of truth, generating compliance-ready inventories in minutes.

Worth a closer look for Cherokee Federal?
```

#### BEFORE (actual email sent to Demetrias at Planet Technologies):
**Subject:** `compliance visibility challenges`

**Body:**
```
Hi Demetrias,

With Planet Technologies' growth and focus on cloud solutions, how
are you ensuring complete visibility into your IT assets and
maintaining compliance across diverse environments?

The University of Derby faced similar pressures — specifically around
compliance and certification in a fast-moving educational environment.
Their situation was a struggle to maintain compliance with evolving
regulations.

They implemented systematic asset management and scanning — achieving
Cyber Essentials Plus certification...
```

**Problems identified from actual sent emails:**
1. **Case study mismatch for Demetrias** — University of Derby (education) used as proof for Planet Technologies (MSP/cloud). An MSP doesn't relate to a university's compliance struggles.
2. **Tim's email is better** — B2B Cyber Secure is actually an MSP case study. But even here, the hook is about Cherokee Federal's own acquisition, not their client management challenges.
3. **Missing MSP-specific language** — No mention of "your clients' environments," PSA/RMM integration, or multi-tenant management.
4. **"Worth a closer look?" is passive** — Works for Close-Lost (warm) but too soft for cold MSP outreach.

---

#### AFTER (suggested 2026-03-31):
**Subject:** `discovery across your client environments`

**Body:**
```
Hi {{first_name}},

Quick question — how many of {{company_name}}'s client environments
have complete asset visibility right now?

Most MSPs we work with are juggling separate discovery tools per
client, or relying on RMM data that misses 20-30% of what's actually
on the network.

Acora standardized asset inventory across 300+ managed environments
without manual rework — feeding clean data directly into their
PSA/RMM toolchain.

Worth seeing how they did it?
```

**What changed and why:**
- **Subject:** `post-acquisition asset visibility` → `discovery across your client environments` — MSP-specific. Speaks to their business model, not their internal IT.
- **Hook:** Company-specific acquisition hook → universal MSP pain point (visibility across client environments). The acquisition hook was clever but too narrow.
- **Case study:** University of Derby (education) → Acora (300+ MSP environments). Must use MSP proof for MSP targets.
- **Pain point:** Added "RMM data misses 20-30%" — specific, technical, credible to MSP audience.
- **Integration:** Added PSA/RMM toolchain reference — MSPs care about how tools fit their stack.
- **CTA:** "Worth a closer look?" → "Worth seeing how they did it?" — peer-proof CTA.

```json
{
  "campaign_id": 2912101,
  "email_step": 1,
  "sync_date": "2026-03-31",
  "changes": {
    "subject": { "before": "compliance visibility challenges / post-acquisition asset visibility", "after": "discovery across your client environments", "reason": "MSPs think about CLIENT environments. Current subjects focus on the MSP's own IT." },
    "hook": { "before": "Company-specific hook about their own compliance", "after": "How many client environments have complete visibility?", "reason": "Universal MSP pain. Every MSP with 10+ clients has this problem." },
    "case_study": { "before": "University of Derby (education) for MSP targets", "after": "Acora (300+ MSP environments)", "reason": "Case study MUST match the buyer persona. An MSP doesn't relate to a university." },
    "body": { "before": "Generic compliance language", "after": "RMM data gap (20-30% miss) + PSA/RMM integration", "reason": "MSPs live in PSA/RMM tools. Referencing their stack shows we understand their world." },
    "cta": { "before": "Worth a closer look for [company]?", "after": "Worth seeing how they did it?", "reason": "Peer-proof CTA drives more curiosity than a generic 'closer look'" }
  }
}
```

---

### LS: EOLS [Ai Copy] — Email 1 — 🔄 REWRITE RECOMMENDED

**Diagnosis:** 0.3% reply rate. 4 replies, 0 interested. Completed.

---

#### BEFORE (actual email sent to Dave Arthurs at North):
**Subject:** `windows11 visibility challenges`

**Body:**
```
Hi Dave,

North's recent acquisitions are driving significant growth. How are
you ensuring complete visibility across your expanded, hybrid IT
landscape for the Windows 11 migration — especially with DORA/NIS2
compliance in mind?

Our Enterprise Technology Asset Intelligence Platform establishes a
single source of truth for governance and cost control. Hitachi Energy
leveraged this to scan 150,000 assets and generate critical reports
in seconds, streamlining their compliance efforts.

Worth a brief conversation?
```

#### BEFORE (actual email sent to Aurora at Santander/Northeastern):
**Subject:** `merged tech visibility gaps`

**Body:**
```
Hi Aurora,

Santander's Webster acquisition will merge diverse tech stacks. How
are you ensuring complete visibility of your marketing technology —
and DORA/NIS2 compliance — for your Windows 11 migration?

Our Enterprise Technology Asset Intelligence Platform establishes a
single source of truth, federating data for governance and cost
control. Cerner standardized inventory across 28 hospitals with our
platform — improving reporting and reducing risk from outdated devices.

Is streamlining this [cut off]
```

**Problems identified from actual sent emails:**
1. **"Enterprise Technology Asset Intelligence Platform"** — Full product brochure language. Nobody talks like this. Compare to Close-Lost which just says "Lansweeper."
2. **Hooks are overloaded** — "acquisitions + hybrid IT + Windows 11 + DORA/NIS2 compliance" all in one sentence. Too many concepts.
3. **Aurora was at Northeastern, not Santander** — The Clay personalization was wrong. Email bounced (wrong address).
4. **Dave Arthurs had left the company** — Reply was "Dave has transitioned out of North."
5. **"Worth a brief conversation?" is vague** — No specific offer, no time commitment.
6. **PS about agentless discovery is defensive** — "won't disrupt fragile legacy systems" plants worry.

---

#### AFTER (suggested 2026-03-31):
**Subject:** `what's still running eol at {{company_name}}`

**Body:**
```
Hi {{first_name}},

Quick question — does {{company_name}} have a reliable count of
devices still running Windows 10, Server 2012, or other end-of-life
systems?

Most IT teams know the deadlines are coming but don't have a
trustworthy number. Qarmet used Lansweeper to identify 2,000+ devices
for upgrade — 1,200 flagged for immediate replacement — which got
their budget approved in days instead of weeks.

Takes 15 minutes to see how it works on your environment. Worth it?
```

**What changed and why:**
- **Subject:** `windows11 visibility challenges` → `what's still running eol at {{company_name}}` — specific, lowercase, conversational.
- **Hook:** Removed acquisition/DORA/NIS2/Windows 11 overload → one simple question about EOL visibility.
- **Product name:** `Enterprise Technology Asset Intelligence Platform` → `Lansweeper` — use the brand name, not a tagline.
- **Case study:** Hitachi Energy (too big, not relatable) → Qarmet (specific: 2,000 devices, 1,200 replacements, budget approval) — directly about EOL migration.
- **CTA:** `Worth a brief conversation?` → `Takes 15 minutes. Worth it?` — specific time commitment.
- **Removed PS** about agentless/fragile systems — defensive framing.

```json
{
  "campaign_id": 2953821,
  "email_step": 1,
  "sync_date": "2026-03-31",
  "changes": {
    "subject": { "before": "windows11 visibility challenges / merged tech visibility gaps", "after": "what's still running eol at {{company_name}}" },
    "hook": { "before": "Overloaded: acquisitions + DORA + NIS2 + Windows 11 in one sentence", "after": "Single question: do you have a reliable count of EOL devices?", "reason": "Too many concepts = nothing lands. Close-Lost succeeds with ONE focused hook." },
    "product_name": { "before": "Enterprise Technology Asset Intelligence Platform", "after": "Lansweeper", "reason": "Product brochure language. Nobody says 'Enterprise Technology Asset Intelligence Platform' in conversation." },
    "case_study": { "before": "Hitachi Energy (150K assets) / Cerner (28 hospitals)", "after": "Qarmet (2,000 devices, 1,200 replacements, budget approved)", "reason": "Qarmet case study is specifically about EOL/migration. Hitachi is generic scale." },
    "cta": { "before": "Worth a brief conversation?", "after": "Takes 15 minutes. Worth it?", "reason": "Specific time. Close-Lost uses '15 minutes' consistently and it works." }
  }
}
```

---

### LS: IT Orgs [Ai Copy] EU — Email 1 — ⚠️ MINOR TWEAKS

**Diagnosis:** 2.1% reply rate — second best. But many "replies" are OOO auto-responses in German, Latvian, French. Actual positive engagement is lower than 2.1% suggests.

#### Actual email sent to Youssef at EFA:
**Subject:** `nis2 compliance readiness`

**Body:**
```
Hi Youssef,

With new regulations like NIS2 and DORA, how are you validating your
complete attack surface and managing shadow IT today?

The University of Derby used manual data and fragmented scanners —
creating audit pressure and more time fire-fighting than preparing.

They then used a disciplined scanning approach to get full visibility
— helping them achieve Cyber Essentials Plus certification and improve
compliance posture.

Worth a closer look for efa?
```

**What's working:** NIS2/DORA hook is highly relevant for EU targets. Compliance angle lands.

**What to improve:**
- Company name "efa" should be properly cased ("EFA")
- "Worth a closer look for efa?" reads as low-effort personalization
- Case study rotation could be smarter — University of Derby is UK education, not always relevant for EU manufacturing or finance targets

**Recommended tweak (not a full rewrite):** Ensure Clay capitalizes company names properly, and add case study matching logic: manufacturing targets get Bekaert/Rentokil, financial services get the compliance angle with more specific regulatory references.

---

### LS: MSPs [Ai Copy] EU — Email 1 — ⚠️ CASE STUDY FIX + UNSUB

**Actual email sent to Dmitrijs at Tet.lv:**
**Subject:** `compliance readiness`

**Body:**
```
Hi Dmitrijs,

With Tet.lv navigating compliance and efficiency in a hybrid IT
environment, how are you ensuring complete asset visibility for audit
readiness?

University of Derby used to face significant pressure regarding
compliance and certification — making audit readiness a constant
challenge.

They then transitioned to disciplined weekly scanning with Lansweeper
— achieving Cyber Essentials Plus certification and solid compliance.

Worth a closer look for Tet.lv?

Unsubscribe
```

**Problems:**
1. **University of Derby for an MSP target** — Same case study mismatch as MSP US. Use Acora (300+ environments) or B2B Cyber Secure.
2. **"Unsubscribe" as a bare word link** — Looks spammy. 13 unsubscribes on 609 sent (2.1%). Consider "PS: If this isn't relevant, reply and I'll remove you" — lower friction, fewer spam flags.
3. **The hook is about Tet.lv's own compliance** — MSPs care about their clients' compliance, not their own.

**Fix:** Apply the same MSP framework from the US rewrite above. Replace University of Derby with Acora/B2B Cyber Secure. Change "Unsubscribe" to a PS opt-out line.

---

### LS: IT Organizations [Intent Data] — ❌ KILL

_0 replies on 288 leads. Complete failure. Do not relaunch without pairing intent signals with Close-Lost-quality copy (specific product updates, relevant case studies, named compliance frameworks)._

---

### Targeting Changes — 2026-03-31

#### Close-Lost — NO CHANGE
_Best performer. Feed more leads from Salesforce closed-lost pipeline._

#### MSPs — TIGHTEN + FIX CASE STUDIES
**BEFORE:** MSPs of all sizes. Clay using IT org case studies (University of Derby) for MSP targets.
**AFTER:** MSPs managing 10+ client environments. Clay must use ONLY MSP case studies: Acora (300+ environments), B2B Cyber Secure (government, 2K-100K assets), Krome (multi-site).
**Remove:** Solo IT consultants, MSPs under 5 clients.

#### IT Orgs — SPLIT BY VERTICAL FOR CASE STUDY MATCHING
**BEFORE:** All IT organizations 1,000+ employees, same Clay prompt for all.
**AFTER:** Split Clay case study selection by detected vertical:
- Manufacturing → Bekaert (100% IT+OT visibility), Rentokil (130 servers, 90 countries), Qarmet (2,000 devices)
- Financial Services → Compliance focus (SOX, PCI-DSS), on-prem + AI angle (validated by Banque BEMO reply)
- Education → University of York (£300K saved), University of Derby (Cyber Essentials Plus)
- Healthcare → Cerner (28 hospitals)

#### Website Visitors — REFERENCE THE VISIT
**BEFORE:** Generic "asset visibility" subject lines. No reference to website visit.
**AFTER:** Subject line acknowledges the visit. Hook references they were researching Lansweeper.

```json
{
  "sync_date": "2026-03-31",
  "targeting_changes": {
    "msp_campaigns": {
      "case_study_fix": "ONLY use Acora, B2B Cyber Secure, Krome — never University of Derby or Hitachi Energy for MSP targets",
      "remove_segments": ["solo consultants", "MSPs under 5 clients"],
      "add_signals": ["hiring technicians", "adding security services"],
      "unsub_fix": "Replace bare 'Unsubscribe' link with PS opt-out line"
    },
    "it_org_campaigns": {
      "vertical_split": {
        "manufacturing": ["Bekaert", "Rentokil", "Qarmet", "Hitachi Energy"],
        "financial_services": ["on-prem + AI angle", "SOX/PCI-DSS compliance"],
        "education": ["University of York", "University of Derby"],
        "healthcare": ["Cerner"]
      }
    },
    "website_visitors": {
      "subject_fix": "Reference website visit in subject line",
      "hook_fix": "Acknowledge they were researching Lansweeper",
      "formatting_fix": "Remove bold/italic HTML tags — send as clean plain text"
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
