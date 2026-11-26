# 🛠️ Runbook: Booked-Jobs Websites for Home-Service Contractors

> **Mode**: NEXUS-Sprint, then always-on NEXUS-Micro loops | **Duration**: 3 weeks to launch, then continuous | **Agents**: 24

---

## Scenario

You run a productized web agency that sells conversion websites to US home-service contractors: roofing, HVAC, plumbing and electrical. Contractors don't buy "websites". They buy **more booked calls and jobs**. So the product is a booked-jobs system (site + speed-to-lead + reviews + call tracking), and every number you report is a phone call, a booked appointment or a job.

You want the whole machine, from finding prospects to reporting results, run by agents. Humans only approve at a few gates where the law or real money requires it.

The full offer, copy, sequences and agent prompts live in the companion workflow: [`examples/workflow-home-services-contractor-funnel.md`](../../examples/workflow-home-services-contractor-funnel.md).

## The Machine at a Glance

```
 ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
 │ 1. SOURCE    │──▶│ 2. AUDIT +   │──▶│ 3. OUTREACH  │──▶│ 4. CONVERT   │
 │ Maps scrape, │   │ SPEC SITE    │   │ email + video│   │ preview page │
 │ score, dedupe│   │ auto-built   │   │ AI replies   │   │ call OR self-│
 └──────────────┘   └──────────────┘   └──────────────┘   │ serve checkout│
                                                          └──────┬───────┘
 ┌──────────────┐   ┌──────────────┐   ┌──────────────┐          │
 │ 7. EXPAND +  │◀──│ 6. OPERATE + │◀──│ 5. ONBOARD + │◀─────────┘
 │ REFER        │   │ REPORT JOBS  │   │ LAUNCH (≤7d) │
 └──────────────┘   └──────────────┘   └──────────────┘
```

Each box is owned by one agent. The **Agents Orchestrator** moves records between stages through a single CRM pipeline. The **Automation Governance Architect** approves every automation before it touches a real prospect or client.

## Agent Roster

### Command & Governance
| Agent | Role |
|-------|------|
| Agents Orchestrator | Pipeline controller: moves each lead/client between stages, retries failures, escalates to a human |
| Automation Governance Architect | Approves each n8n/Make workflow for value, risk and failure handling before go-live |
| Workflow Architect | Maps every branch: no-reply, bounce, unsubscribe, "already have a guy", payment failure |
| Legal Compliance Checker | CAN-SPAM, TCPA, A2P 10DLC, FTC claims, state contractor-license display rules |

### Offer & Acquisition
| Agent | Role |
|-------|------|
| Offer & Lead Gen Strategist | Owns the offer, guarantee, pricing tiers and lead magnet |
| Pricing Analyst | Unit economics per trade, tier pricing, ad-spend pass-through |
| Outbound Strategist | ICP scoring, signal-based targeting, sequence design |
| Sales Outreach | Writes and personalizes cold email, handles replies and objections |
| PPC Campaign Strategist | Retargeting and contractor-acquisition ads (agency side), plus client Google Ads / LSA |
| Paid Social Strategist | Meta retargeting for people who opened the spec site |

### Build & Fulfillment
| Agent | Role |
|-------|------|
| UX Architect | One conversion template per trade (above-fold phone, offer, trust, service area) |
| UI Designer | Brand tokens auto-derived from the contractor's logo and truck photos |
| Frontend Developer | Template codebase and the spec-site generator |
| SEO Specialist | Service × city pages, schema, Google Business Profile optimization |
| Content Creator | Trade-specific copy, FAQs, monthly posts |
| Tracking & Measurement Specialist | Call tracking, form + booking events, GA4/Ads conversions |
| Email Strategist | Agency nurture, plus client review-request and reactivation flows |

### Retention & Quality
| Agent | Role |
|-------|------|
| Customer Success Manager | Onboarding, health score, churn saves, upsells, referrals |
| Support Responder | Client change requests and questions (email/chat) |
| Analytics Reporter | Monthly "booked jobs" report per client, agency funnel dashboard |
| Evidence Collector | Screenshot QA of every site before launch |
| Reality Checker | Final launch gate; defaults to NEEDS WORK |
| Experiment Tracker | A/B tests on subject lines, preview page, guarantee wording, site hero |
| Executive Summary Generator | Monthly agency P&L, CAC, churn and LTV summary for you |

## Execution Plan

### Week 1: Offer, Compliance & Automation Design

```
Day 1-2: Offer + Economics
├── Offer & Lead Gen Strategist → "Booked-Jobs Website System" offer
│   ├── Dream outcome stated in calls/jobs, not pages
│   ├── Conditional guarantee tied to tracked calls
│   ├── 3 tiers + ad-management add-on
│   └── Lead magnet: free "Missed-Jobs Audit" + spec site
├── Pricing Analyst → Break-even per trade (jobs needed to pay for a year)
└── Outbound Strategist → ICP + scoring model per trade

Day 3-4: Guardrails
├── Legal Compliance Checker → Channel rules
│   ├── Cold email: CAN-SPAM (address, opt-out, honest subject)
│   ├── No cold SMS and no AI-voice cold calls (TCPA)
│   ├── A2P 10DLC registration for every client texting number
│   └── Claims review: no "guaranteed #1 on Google"
├── Workflow Architect → Full branch map for all 7 stages
└── Automation Governance Architect → Approve / reject each workflow

Day 5: Stack decision
└── Automation Governance Architect → Approved tool list (see companion doc)
```

### Week 2: Build the Machine

```
Parallel tracks:
├── UX Architect + UI Designer → 4 trade templates (roof, HVAC, plumb, elec)
├── Frontend Developer → Template repo + spec-site generator
│   └── Input: Maps record → Output: preview URL in < 3 min
├── SEO Specialist → Page architecture + LocalBusiness/Service schema
├── Tracking Specialist → Call tracking + conversion events baked into template
├── Sales Outreach → 4-step cold email sequence per trade
├── Email Strategist → Agency nurture + client review/reactivation flows
└── Frontend Developer → Preview page with "Claim this site" checkout

Gate (Evidence Collector + Reality Checker):
├── 10 spec sites generated end-to-end from real Maps records
├── Mobile Lighthouse ≥ 90, click-to-call above the fold
├── Test call + test form fire conversions in GA4
└── Test checkout → onboarding form → CRM stage change
```

### Week 3: Soft Launch (one metro × one trade)

```
Day 1: Warm-up check
├── Sending domains warmed ≥ 14 days (start this in Week 1)
└── Human approves first 25 emails by hand          ← HUMAN GATE

Day 2-5: 50 → 150 new prospects/day
├── Outbound Strategist → Source + score + dedupe
├── Frontend Developer (generator) → Spec site per A-tier lead
├── Sales Outreach → Send, classify replies, book calls
├── Paid Social Strategist → Retarget spec-site visitors
└── Analytics Reporter → Daily funnel snapshot

End of week:
└── Experiment Tracker → Kill/scale subject lines + preview page variants
```

### Always-On Loops (after launch)

```
Every hour:
└── Agents Orchestrator → Advance stages, retry failed jobs, page a human on errors

Daily:
├── Outbound Strategist → New leads in rotating metros
├── Sales Outreach → Reply handling within 5 min (business hours)
├── Customer Success Manager → Onboarding nudges, health-score alerts
└── Analytics Reporter → Agency funnel dashboard

Weekly:
├── Experiment Tracker → One live test per funnel stage
├── SEO Specialist → GBP posts + one service-city page per client
└── Support Responder → Clear change-request queue (48h SLA)

Monthly:
├── Analytics Reporter → Per-client "Booked Jobs Report" (auto-sent)
├── Customer Success Manager → Upsell ads/LSA to clients with ≥ 4.5★ and capacity
└── Executive Summary Generator → Agency P&L, CAC, churn, LTV
```

## Human Gates (keep these, even when "fully automated")

| Gate | Why it stays human | Owner |
|------|--------------------|-------|
| Approve first 25 sends of any new sequence | Catch tone/claim errors before they scale | You |
| A2P 10DLC brand + campaign registration | Carrier vetting needs a real business identity | You + client |
| Refunds, disputes, guarantee payouts | Real money, real relationships | You |
| Anything the Reality Checker marks NEEDS WORK twice | Prevent retry loops | You |
| Sales calls for Tier 3 / multi-location | Bigger deals close better with a human | You (optional) |

## Funnel Metrics

| Stage | Metric | Starting target | Owner |
|-------|--------|-----------------|-------|
| Source | A-tier leads/day | 100+ | Outbound Strategist |
| Outreach | Positive reply rate | 2-4% | Sales Outreach |
| Spec site | Preview view rate (of delivered) | 25%+ | Experiment Tracker |
| Convert | Booked call or checkout (of viewers) | 5-10% | Offer & Lead Gen Strategist |
| Close | Call-to-close | 25-35% | Sales Outreach |
| Launch | Signed → live | ≤ 7 days | Agents Orchestrator |
| Value | Tracked calls/client/month | Beat guarantee by month 2 | Analytics Reporter |
| Retain | Monthly logo churn | < 4% | Customer Success Manager |

Treat these targets as starting hypotheses. The Experiment Tracker replaces them with your own numbers after 30 days.

## Quality Gates

| Checkpoint | When | Agent |
|-----------|------|-------|
| Claims + compliance review | Every new sequence, ad and template | Legal Compliance Checker |
| Workflow approval | Every new or changed automation | Automation Governance Architect |
| Site QA screenshots (mobile + desktop) | Every launch | Evidence Collector |
| Launch go/no-go | Every launch | Reality Checker |
| Conversion tracking verified | Every launch + monthly | Tracking & Measurement Specialist |
