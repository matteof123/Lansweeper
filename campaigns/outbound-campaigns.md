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
