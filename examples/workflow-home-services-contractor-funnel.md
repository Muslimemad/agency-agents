# Multi-Agent Workflow: Booked-Jobs Websites for Home-Service Contractors

> An agent-run agency that sells conversion websites to US roofers, HVAC techs, plumbers and electricians, from lead sourcing to monthly results reporting. Team roster and phase plan: [`strategy/runbooks/scenario-home-services-websites.md`](../strategy/runbooks/scenario-home-services-websites.md).

## The Scenario

Contractors get pitched "a new website" every week and ignore it. What they actually want is the phone ringing with jobs they can close. So this agency sells **booked calls and jobs**, and the website is the delivery vehicle.

The funnel has one unfair advantage: **we build the prospect's new site before we ever contact them.** The first email links to it. Seeing their own business name, reviews and phone number on a fast, good-looking mobile site does most of the selling.

Everything below was produced by activating agents from this repo. The prompts are at the end so you can regenerate or adapt any piece.

---

## Part 1 — The Offer

*Owner: Offer & Lead Gen Strategist · Economics: Pricing Analyst*

### The value equation applied

| Lever | How this offer moves it |
|-------|-------------------------|
| **Dream outcome** | "More of the calls you already get turn into booked jobs, and you stop losing jobs to the guy who answered first." |
| **Perceived likelihood** | They see *their* finished site before paying. Conditional guarantee on tracked calls. Monthly report counts calls, not "impressions". |
| **Time delay** | Live in 7 days. Missed-call text-back works the first day. |
| **Effort & sacrifice** | No meetings needed. One 10-minute onboarding form. We write every word and handle domain, Google profile and tracking. |

### Name and promise

> **The Booked-Jobs Website System**
> A new site that's built to turn visitors into phone calls, live in 7 days, with every call and lead tracked. If it doesn't hit your call target in 60 days, we keep working for free until it does.

### What's in it (the stack)

| # | Component | What the contractor gets | Why it books jobs |
|---|-----------|--------------------------|-------------------|
| 1 | **Conversion website** | Trade-specific template: tap-to-call header, "Get a quote in 60 seconds" form, service-area pages, reviews, license #, financing badge | Homeowners with a leak or a dead AC call the first site that loads fast and looks legit |
| 2 | **Missed-call text-back** | Missed calls get an instant text: "Sorry we missed you. This is {{company}}. What can we help with?" | Saves the job when they're on a roof or under a sink |
| 3 | **60-second speed-to-lead** | Form fills trigger an SMS + email to the owner and an auto-call that connects them ("Press 1 to call the customer back now") | Calling back in under 5 minutes wins far more jobs than calling an hour later |
| 4 | **Review engine** | Post-job review request by text/email to every customer (no gating) | More reviews means more calls from Google Maps |
| 5 | **Google Business Profile tune-up** | Categories, services, photos, weekly posts, link to the new site | Maps is where most local calls come from |
| 6 | **Call tracking + Booked-Jobs Report** | Tracking number, recorded calls (where legal), monthly 1-page report | Proof. This is what stops churn. |
| 7 | **Unlimited small edits** | Text or email a change, done within 48h | Removes the "my web guy never answers" pain |

**Bonuses (time-boxed, honest):**
- Setup fee waived if they claim their preview site within 7 days. The preview really does come down after 14 days.
- Seasonal campaign pack per trade: HVAC spring/fall tune-up, roofing storm response, plumbing frozen-pipe/water-heater, electrical panel-upgrade/EV-charger.
- Free domain and site migration from their old host.

### Guarantee (conditional, outcome-based)

> **The 60-Day Call Guarantee.** During onboarding we set a call-and-lead target for your trade and market based on your current numbers. If your new site and profile don't produce that many tracked calls and form leads in the first 60 days after launch, we keep working for free until they do. If we still haven't hit it by day 90, we refund your setup fee too.
>
> *Your side: answer or return leads during business hours, and keep the tracking number and site link on your Google profile.*

Why calls and not jobs? We control whether the phone rings. The contractor controls whether they close. A jobs guarantee invites disputes. A calls guarantee is measurable by both sides and still speaks directly to the outcome.

### Pricing

| | **Core** | **Growth** ⭐ most picked | **Dominate** |
|---|---|---|---|
| Monthly | $297 | $497 | $997 + ad spend |
| Setup | $497 (waived within 7 days) | $497 (waived within 7 days) | $997 |
| Website + speed-to-lead + missed-call text-back | ✅ | ✅ | ✅ |
| Call tracking + Booked-Jobs Report | ✅ | ✅ | ✅ |
| Review engine | — | ✅ | ✅ |
| GBP management + weekly posts | — | ✅ | ✅ |
| New service × city page | — | 2 / month | 4 / month |
| Google Local Services Ads + Search management | — | — | ✅ |
| Term | 3-month minimum, then monthly | 3-month minimum, then monthly | 6-month minimum |

**The math the contractor sees** (Pricing Analyst; rough US averages, replace with the contractor's own job value during onboarding):

| Trade | Typical ticket | Extra jobs/year that pay for Growth ($5,964 + setup) |
|-------|----------------|------------------------------------------------------|
| Roofing (replacement) | $10k-$15k | **1** |
| HVAC (system replacement) | $7k-$12k | **1** |
| Plumbing (service call / water heater) | $300-$2,500 | ~1 per month |
| Electrical (service / panel upgrade) | $300-$3,000 | ~1 per month |

> "One extra roof a year pays for this. Everything after that is profit."

### Lead magnet

**Free Missed-Jobs Audit + Your New Site, Already Built.** It's a one-page scorecard: mobile speed, tap-to-call, form, reviews vs. the top 3 competitors in the Map Pack, GBP completeness. It sits next to the preview link, so the prospect gets real value even if they never buy.

---

## Part 2 — The Funnel Map

*Owner: Workflow Architect · Approved by: Automation Governance Architect*

```
SOURCE ──▶ SCORE ──▶ SPEC SITE ──▶ EMAIL SEQ ──▶ PREVIEW PAGE ──┬──▶ SELF-SERVE CHECKOUT ──┐
  │          │           │             │              │         │                         │
  │       C-tier      build fail    reply ─▶ AI router │         └──▶ 15-min call ──▶ close ┤
  │       → drop      → retry x2       │  ├ interested ─────────────┘                     │
  │                   → human          │  ├ question → KB answer → re-offer               │
  │                                    │  ├ objection → library → re-offer                │
  │                                    │  ├ not now → 90-day nurture                      │
  │                                    │  ├ unsubscribe → global suppression              │
  │                                    │  └ unsure (<0.8 conf) → human                    │
  │                               viewed preview, no action                               │
  │                                    └──▶ Meta/Google retargeting + bump email          │
  ▼                                                                                       ▼
 CRM ◀───────────────────── Agents Orchestrator owns every stage change ──────────── ONBOARD
                                                                                         │
             REFER/UPSELL ◀── MONTHLY REPORT ◀── OPERATE ◀── LAUNCH ◀── QA GATE ◀────────┘
```

### Stage 1 — Source & score (Outbound Strategist)

**Sources:** Google Maps business data from a licensed provider (e.g. Outscraper, Apify actors, or a Places API integration; respect each source's terms), state contractor-license databases, PageSpeed Insights API, a tech-detection lookup, and email finding + verification.

**ICP scoring (0-100):**

| Signal | Points | Why |
|--------|--------|-----|
| Rating ≥ 4.3 and ≥ 25 reviews | +25 | They do good work. Marketing them is easy and ethical. |
| No website, or Facebook-only | +25 | Biggest gap, easiest sell |
| Mobile PageSpeed < 50 | +15 | Visible, provable problem |
| No tap-to-call or no form above the fold | +15 | Directly leaks calls |
| Running Google Ads / LSA (ad transparency or LSA badge) | +10 | Already paying for clicks that the site wastes |
| Hiring posts, or 3-25 employees | +10 | Has capacity and is growing |
| Franchise / national brand / corporate site | −100 | Can't buy locally |
| Rating < 3.8 | −40 | Reviews will sink any site; refer them out |

A-tier (≥ 60) gets a spec site. B-tier (40-59) gets the audit-only email. C-tier is dropped.

**Launch order (by trade):** start with **HVAC and plumbing**, where urgency makes the "missed call = lost job" story hit hardest and demand runs year-round. Add **roofing** next (biggest tickets; sell storm pages and financing). Add **electrical** last. Start with 1 trade × 3 metros, rotating metros weekly so you never re-hit the same market too fast.

### Stage 2 — Spec site generator (Frontend Developer, UI Designer, Content Creator)

**Input:** one scored lead record. **Output:** `preview.youragency.com/{slug}` in under 3 minutes.

1. Pull name, phone, city, service area, services, hours, rating, review count, 3 recent 5★ review snippets (attributed "via Google"), and their logo/photos from their site or GBP.
2. UI Designer agent derives brand tokens from the logo: primary color, contrast-safe accent. If no logo, use a clean trade-default palette.
3. Content Creator agent writes the hero, services and FAQs from the trade template. It only states facts from the record: no invented years in business, certifications or warranties.
4. Build static pages with the trade template. Add `noindex` and a top banner: *"Preview built for {{company}}. Not live. Expires {{date}}."*
5. Run a Lighthouse mobile check. It must score ≥ 90 or the build is retried.
6. Screenshot the mobile + desktop hero for the email/video.
7. Auto-delete after 14 days unless claimed.

### Stage 3 — Outreach (Sales Outreach, Legal Compliance Checker)

**Channel rules (non-negotiable):**
- **Cold email only** for first touch. Use separate sending domains, warmed ≥ 14 days, ≤ 30-40 sends per inbox per day, plain text, a real sender name, the business's physical address and a one-reply opt-out.
- **No cold SMS. No AI-voice or prerecorded cold calls.** Under the TCPA, an AI-generated voice counts as "artificial", and texts and calls to cell phones without prior consent carry per-message statutory damages. Several states (e.g. FL, OK) add stricter rules on top. Texts and calls are fine *after* a prospect books or replies and asks to be called.
- **Optional human dialer:** a human (you or a hired setter) can call A-tier leads who opened the preview twice. Scrub against the National DNC list first.

**4-step sequence (plumbing version; the agent swaps trade variables):**

**Email 1 — Day 0** · Subject: `built a new site for {{company}}`
```
Hi {{first_name}},

I was looking for a plumber in {{city}} and found {{company}}.
{{review_count}} reviews at {{rating}}★ is better than most of the
companies showing above you on Google.

The catch: on a phone, your site {{top_issue}}. When someone has
water on the floor, they call the first company they can tap.

So I built you a new one. It's already done:
{{preview_url}}

If you like it, it can be live this week. If not, no problem.
It comes down on its own in 14 days.

{{sender_first_name}}
{{agency_name}} · {{agency_address}}
(Reply "no" and I won't email again.)
```

**Email 2 — Day 3** · Subject: `re: {{company}}`
```
{{first_name}}, quick side-by-side of your current site vs. the new
one on a phone:

{{comparison_gif_url}}

The new one loads in {{new_load_time}}s (yours: {{old_load_time}}s)
and has a call button on every screen.

Preview's still up: {{preview_url}}
```

**Email 3 — Day 7** · Subject: `one water heater`
```
{{first_name}}, the honest math:

The site + missed-call text-back is ${{price}}/mo. One water heater
install covers about {{months_covered}} months of it.

And if it doesn't hit the call target we set together in 60 days,
we work free until it does.

Want it live? Claim it here (takes 2 minutes): {{claim_url}}
Or grab 15 min with me: {{booking_url}}
```

**Email 4 — Day 12** · Subject: `taking it down`
```
{{first_name}}, I'll take the {{company}} preview down on {{expiry_date}}
so it doesn't sit out there with your name on it.

If now's not the time, no worries. Reply "later" and I'll check
back in a few months.
```

**Trade swaps:**

| Variable | Roofing | HVAC | Plumbing | Electrical |
|----------|---------|------|----------|------------|
| Urgent moment | "a leak after a storm" | "the AC dies in July" | "water on the floor" | "half the house loses power" |
| Email 3 subject | `one roof` | `one system swap` | `one water heater` | `one panel upgrade` |

**AI reply router** (Claude API classification step in n8n; confidence threshold 0.8):

| Class | Automated action |
|-------|------------------|
| Interested | Reply with claim link + booking link, mark HOT, notify you |
| Question (price, contract, "is this a scam") | Answer from the FAQ knowledge base, re-offer both links |
| Objection | Pick from the objection library (below), one reply, re-offer |
| Not now / later | Stop the sequence, enroll in a 90-day nurture |
| Unsubscribe / angry | Suppress across every tool within 1 minute, no reply |
| Wrong person | Ask for the owner's email once |
| Out of office | Pause until the return date |
| Low confidence / legal threat | Route to a human, never auto-reply |

### Stage 4 — Convert (Offer & Lead Gen Strategist, Frontend Developer)

The **preview page** is the real sales page. It wraps their spec site:

```
┌─────────────────────────────────────────────────────────────┐
│ Banner: "Your new site, {{company}} — ready to go live"     │
├───────────────────────────┬─────────────────────────────────┤
│   [ their site in a        │  ✅ Live in 7 days              │
│     phone frame,           │  ✅ Missed-call text-back       │
│     scrollable ]           │  ✅ Every call tracked          │
│                            │  ✅ 60-Day Call Guarantee       │
│                            │                                 │
│                            │  Your Missed-Jobs Audit: 41/100 │
│                            │  [ see what's leaking ▸ ]       │
│                            │                                 │
│                            │  $497/mo · setup $0 until {{d}} │
│                            │  [ CLAIM MY SITE ]  ← Stripe    │
│                            │  [ talk to a human first ] ← Cal│
└───────────────────────────┴─────────────────────────────────┘
```

**Two paths, both automated:**
- **Self-serve:** Stripe Checkout → webhook → CRM `WON` → onboarding form opens immediately on the thank-you page.
- **Call:** Cal.com 15-min slot → confirmation + reminder texts (they consented by booking) → AI note-taker → follow-up email with the claim link within 2 minutes of the call ending.

**Retargeting:** preview viewers who don't act join a Meta + Google audience for 14 days. Creative is a 6-second clip of *their* site scrolling (Paid Social Strategist). Each one also gets a "saw you checked it out" bump email.

**15-minute call script** (for you or a setter, Sales Outreach):
1. *(1 min)* "You saw the site. What did you think?" Let them talk.
2. *(4 min)* "Where do most of your jobs come from right now? What happens when you miss a call on a job?" Get the pain in their words.
3. *(3 min)* Walk the preview on their phone: tap-to-call, quote form, missed-call text (trigger a live demo to their own phone).
4. *(3 min)* The math: "What's an average job worth to you? So one extra job a month is ${{x}}."
5. *(2 min)* Offer + guarantee + setup-waiver deadline.
6. *(2 min)* "Want me to text you the link to lock it in?" Send the claim link while you're still on the call.

**Objection library:**

| They say | We say |
|----------|--------|
| "I get all my work from referrals." | "Great. Referrals Google you before they call. This makes sure they find a site that matches the guy they were told about, and catches the ones who call while you're busy." |
| "I already have a web guy." | "Keep him if he's tracking your calls. If he can't tell you how many calls the site made last month, that's the gap we fill." |
| "I got burned by marketing before." | "That's why there's no 12-month contract and you get a calls report every month. If the numbers aren't there, you're not stuck." |
| "I'm too busy for this." | "That's the point. It's a 10-minute form, we do everything else, and it answers your missed calls while you're on a job." |
| "We use Angi / HomeAdvisor." | "Those leads go to 3-4 contractors at once. Calls from your own site are yours alone and don't cost per lead." |
| "Too expensive." | "What's one {{trade_job}} worth? If this brings in one a year (roofing/HVAC) or one a month (plumbing/electrical), it's paid for. And the guarantee covers you if it doesn't." |

### Stage 5 — Onboard & launch in ≤ 7 days (Agents Orchestrator)

```
Day 0  Stripe webhook → CRM WON → onboarding form (10 min):
       logo/photos, license #, services, service area, hours,
       financing partner, avg job value, GBP manager access,
       domain registrar access, how they want lead alerts
       └─ Orchestrator fans out tasks in parallel:
          ├─ UI Designer → final brand tokens
          ├─ Content Creator → final copy (trade + their specifics)
          ├─ SEO Specialist → service×city pages, LocalBusiness schema, GBP fixes
          ├─ Tracking Specialist → tracking number, GA4 + Ads conversions
          ├─ Frontend Developer → production build on their domain
          └─ A2P 10DLC registration for their texting number   ← HUMAN GATE
Day 3  Client approval link (approve or request changes in one form)
Day 5  Evidence Collector → mobile/desktop screenshots, test call, test form,
       test missed-call text, accessibility pass
Day 6  Reality Checker → GO / NEEDS WORK (max 2 loops, then a human)
Day 7  DNS cutover, GBP website link → new site, welcome email + "what to expect"
Day 14 CSM check-in text: "Getting the lead alerts OK?"
Day 30 First Booked-Jobs Report
```

### Stage 6 — Operate & prove it (Analytics Reporter, SEO Specialist, Email Strategist)

**Monthly Booked-Jobs Report** (auto-generated, emailed and texted as a link; sample numbers):

```
{{company}} — October results
──────────────────────────────────────────
📞 64 calls from your site & Google profile   (▲ 38% vs. before launch)
   └─ 9 missed calls saved by text-back
📝 17 quote requests
⭐ 11 new Google reviews  (now 4.8★ / 142)
💵 Est. value at your $650 avg job and 40% close: ~$21,000

Top pages: Water Heater Repair – Mesa · Emergency Plumber – Gilbert
Next month: 2 new city pages (Chandler, Queen Creek) + fall water-heater campaign
Guarantee target: 45 calls+leads in 60 days → ✅ hit on day 31
```

If the client connects their field-service software (ServiceTitan, Jobber or Housecall Pro), the report shows **booked jobs and revenue** pulled from it instead of estimates.

**Ongoing automations:** weekly GBP posts, review requests after every completed job, seasonal campaigns sent to the client's past customers (only people who did business with them, with opt-out), and a monthly rank and speed check.

### Stage 7 — Retain, expand, refer (Customer Success Manager)

**Health score:** calls trend (40%), report opens (15%), edit requests answered on time (15%), review growth (15%), payment status (15%). Below 60 triggers a save play: a free extra city page plus an honest "here's what we're changing" email, and you get a heads-up.

**Expansion:** Growth clients with ≥ 4.5★, a rising call trend and spare capacity get the Dominate (LSA + ads) offer in month 3.

**Referral:** "Know a contractor in a different trade? One month free for you, setup waived for them." Roofers know HVAC guys, HVAC guys know electricians.

**Agency-side inbound (layer on after outbound works):** Meta lead ads to contractors in target metros offering the free Missed-Jobs Audit. Partnerships with supply houses and distributors (lunch-and-learn decks generated by the Document Generator). Monthly case-study posts built from Booked-Jobs Reports, with client permission.

---

## Part 3 — The Automation Stack

*Owner: Automation Governance Architect*

| Job | Default pick | Alternatives |
|-----|--------------|--------------|
| Orchestration | n8n (self-hosted) | Make, Zapier |
| Lead + client database | Supabase (Postgres) | Airtable |
| Maps / business data | Outscraper | Apify, Places API |
| Email find + verify | Apollo or Hunter + ZeroBounce | Prospeo, NeverBounce |
| Cold email + warm-up | Instantly | Smartlead |
| AI steps (personalize, classify, write) | Claude API | — |
| Spec + client sites | Astro/Next.js template on Vercel | Webflow, WordPress |
| Booking | Cal.com | Calendly |
| Payments | Stripe Checkout + Billing | — |
| Call tracking, missed-call text-back, speed-to-lead | Twilio (+ A2P 10DLC) | CallRail, GoHighLevel |
| Reviews + client CRM | GoHighLevel sub-account per client | Podium, NiceJob |
| Retargeting | Meta + Google Ads | — |
| Reporting | Generated HTML/PDF from Supabase | Looker Studio |

> **Shortcut:** if you'd rather not build fulfillment plumbing, run each client's missed-call text-back, reviews and CRM in a GoHighLevel sub-account and keep n8n only for the agency acquisition pipeline.

### Workflow inventory

| ID | Trigger | What it does | Agent owner |
|----|---------|--------------|-------------|
| WF-01 | Cron, daily 6am | Pull new Maps records for today's metro × trade | Outbound Strategist |
| WF-02 | New record | Enrich, PageSpeed, score, dedupe vs. CRM + suppression list | Outbound Strategist |
| WF-03 | A-tier scored | Generate spec site + audit + screenshots | Frontend Developer |
| WF-04 | Spec site ready | Personalize + enroll in sequence | Sales Outreach |
| WF-05 | Email reply webhook | Classify → route (table above) | Sales Outreach |
| WF-06 | Preview page view | Mark warm, add to retargeting, send bump email | Paid Social Strategist |
| WF-07 | Stripe `checkout.session.completed` | CRM WON, onboarding form, kickoff tasks | Agents Orchestrator |
| WF-08 | Onboarding form submitted | Fan out build tasks, chase missing assets | Agents Orchestrator |
| WF-09 | Build complete | QA screenshots + test events → Reality Checker | Evidence Collector |
| WF-10 | Cron, 1st of month | Build + send Booked-Jobs Reports | Analytics Reporter |
| WF-11 | Cron, weekly | Health scores, churn alerts, upsell flags | Customer Success Manager |
| WF-12 | Any unsubscribe / bounce / complaint | Global suppression across every tool | Legal Compliance Checker |
| WF-13 | Any workflow error | Retry ×2 → alert you with the record + error | Agents Orchestrator |

### Core lead record

```sql
create table leads (
  id uuid primary key default gen_random_uuid(),
  place_id text unique,
  company text not null,
  trade text check (trade in ('roofing','hvac','plumbing','electrical')),
  city text, state text, phone text, website text,
  owner_first_name text, email text, email_verified boolean default false,
  rating numeric, review_count int,
  mobile_speed int, has_tap_to_call boolean, has_form boolean,
  runs_ads boolean, score int, tier text,
  preview_url text, preview_expires_at timestamptz,
  stage text default 'sourced',  -- sourced|scored|spec_built|in_sequence|replied|hot|booked|won|lost|suppressed
  last_reply_class text,
  suppressed boolean default false,
  created_at timestamptz default now()
);
```

---

## Part 4 — Compliance Guardrails

*Owner: Legal Compliance Checker. This is a checklist, not legal advice; have a US attorney review before you scale.*

- **CAN-SPAM:** truthful headers and subject lines, physical address, working opt-out honored within 10 business days (we do it in 1 minute).
- **TCPA + state mini-TCPAs:** no cold texts and no AI/prerecorded cold calls. Human dials only, DNC-scrubbed. Texts only after consent.
- **A2P 10DLC:** register the brand and campaign for every texting number (agency and each client) before sending.
- **Reviews:** ask *every* customer. No gating, no incentives, no fake reviews. That's both the FTC's 2024 rule on fake reviews and review suppression and Google policy.
- **Ad and guarantee claims:** no "#1 on Google guaranteed". Guarantee terms in writing on the checkout page.
- **Contractor license display:** many states require the license number on ads and websites (e.g. California CSLB). The template always shows it.
- **Accessibility:** templates pass an automated WCAG 2.1 AA check before launch.
- **Call recording:** some states require all-party consent. Play a "this call may be recorded" message or turn recording off by state.
- **Spec sites:** `noindex`, clearly labeled as previews, auto-expire, and removed on request.

---

## Part 5 — Illustrative Unit Economics

*Owner: Pricing Analyst. These are starting assumptions; the Experiment Tracker replaces them with real data after 30 days.*

| Step | Monthly volume | Assumption |
|------|----------------|------------|
| A-tier leads emailed | 3,000 | ~140/day × 22 sending days |
| Opened the preview | 600 | 20% of delivered |
| Booked a call or checked out | 36 | 6% of viewers |
| New clients | 10 | ~30% close on calls, self-serve counted directly |
| New MRR | ~$4,500 | blended ~$450/mo |
| Tool + infra cost | ~$800-1,200/mo | inboxes, data, Twilio, hosting, AI calls |

At 4% monthly churn, ~10 new clients/month levels off around 250 clients (~$110k MRR). Retention is the business. That's why the Booked-Jobs Report and the guarantee exist.

---

## Part 6 — Agent Activation Prompts

Run these in order the first time. After that, the Agents Orchestrator runs them on the schedules above.

**Step 1 — Offer & Lead Gen Strategist**
```
Activate Offer & Lead Gen Strategist.

Design a grand-slam offer for a productized web agency selling to US
home-service contractors (roofing, HVAC, plumbing, electrical).
They buy booked calls and jobs, not websites.

Deliver: offer name + one-line promise, value stack with the
job-booking reason for each component, a conditional guarantee
measured on tracked calls + form leads, 3 pricing tiers (monthly +
setup), an honest urgency mechanism, and a lead magnet that works
even if they never buy. Score the final offer on the value equation.
```

**Step 2 — Pricing Analyst**
```
Activate Pricing Analyst.

For tiers at $297 / $497 / $997+spend monthly, compute the break-even
in jobs per year for each trade using typical US ticket sizes. Flag
which trade has the easiest ROI story and recommend whether setup
should be waived, discounted, or held. Show assumptions explicitly.
```

**Step 3 — Outbound Strategist**
```
Activate Outbound Strategist.

Build an ICP scoring model (0-100) for contractors pulled from Google
Maps data. Inputs available: rating, review count, website URL,
mobile PageSpeed, tap-to-call present, form present, ads/LSA
presence, employee estimate, franchise flag. Output tiers A/B/C with
the action for each, plus a metro rotation plan for 1 trade × 3 metros.
```

**Step 4 — Workflow Architect, then Automation Governance Architect**
```
Activate Workflow Architect.

Map the full workflow tree for this funnel: source → score → spec site
→ 4-step cold email → AI reply router → preview page → (Stripe
self-serve | 15-min call) → onboarding → QA → launch → monthly report
→ health score. Include every branch: bounce, unsubscribe, angry
reply, build failure, payment failure, missing onboarding assets,
client unresponsive for 5 days. Mark the human gates.
```
```
Activate Automation Governance Architect.

Review the workflow tree and WF-01..WF-13 inventory. For each
workflow: approve / approve-with-changes / reject, with failure
handling, idempotency, rate limits, secrets handling, and an owner.
Use n8n as the default platform.
```

**Step 5 — Legal Compliance Checker**
```
Activate Legal Compliance Checker.

Review this US B2B outreach + fulfillment system for CAN-SPAM, TCPA
(including AI-voice rules), state mini-TCPA laws, A2P 10DLC, FTC
review rules, contractor license display rules, call-recording
consent, and guarantee wording. Output a pass/fix list for every
email, page, and automation. Flag anything that needs a lawyer.
```

**Step 6 — UX Architect + Frontend Developer (spec-site generator)**
```
Activate UX Architect.

Design one conversion template per trade (roofing, HVAC, plumbing,
electrical). Mobile first. Required above the fold: tap-to-call, the
trade's urgent promise, rating + review count, "quote in 60 seconds"
form. Also: services, service-area pages, license #, financing badge,
FAQ, sticky call bar. Lighthouse mobile ≥ 90.
```
```
Activate Frontend Developer.

Build a spec-site generator: input a lead JSON record, output a static
noindex preview at preview.<agency>/<slug> in under 3 minutes, using
the trade template, brand tokens from the logo, and only facts present
in the record. Add the preview banner, 14-day expiry, Lighthouse check,
and mobile/desktop screenshots. Then build the preview page wrapper
with Stripe Checkout and Cal.com buttons.
```

**Step 7 — Sales Outreach**
```
Activate Sales Outreach.

Write the 4-step cold email sequence per trade (plain text, < 90
words each, honest subject lines, opt-out line, links to the
prospect's prebuilt preview site). Then write the reply-router system
prompt: 8 classes, confidence threshold 0.8, the action per class, and
an objection library for referrals-only, has-a-web-guy, burned-before,
too-busy, uses-Angi, and too-expensive.
```

**Step 8 — Analytics Reporter + Customer Success Manager**
```
Activate Analytics Reporter.

Design the monthly one-page Booked-Jobs Report for a contractor:
calls, missed calls saved, form leads, reviews, estimated value from
their avg job + close rate, top pages, next month's plan, and guarantee
progress. Plain language, readable on a phone in 20 seconds. Also
design the agency funnel dashboard for the stages in the runbook.
```
```
Activate Customer Success Manager.

Build the client lifecycle: Day 0-7 onboarding nudges, Day 14 check-in,
Day 30 first report, a weighted health score, save plays below 60,
month-3 upsell criteria for ads/LSA, and a cross-trade referral offer.
```

**Step 9 — Evidence Collector + Reality Checker (every launch)**
```
Activate Evidence Collector.

For {{client_domain}}: capture mobile + desktop screenshots of every
page, place a test call, submit a test form, trigger a missed-call
text, verify GA4/Ads conversions fired, and run an accessibility scan.
Return evidence, not opinions.
```
```
Activate Reality Checker.

Given the Evidence Collector's report for {{client_domain}}, decide GO
or NEEDS WORK for launch. Default to NEEDS WORK unless every check has
evidence.
```

---

## Key Takeaways

1. **Sell the outcome you can measure.** Calls and leads are tracked, guaranteed and reported. Jobs are shown wherever the client's software allows it.
2. **The spec site is the funnel.** Building first flips the pitch from "trust me" to "here it is".
3. **Automate everything except the legally and financially sensitive gates.** First sends, A2P registration, refunds and stuck loops stay human.
4. **Retention is the business.** The monthly Booked-Jobs Report is the most important thing the agency ships.
