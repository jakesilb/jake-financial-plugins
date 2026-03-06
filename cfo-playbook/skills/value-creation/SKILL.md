---
name: value-creation
description: Apply the 7 Pillars CFO framework to evaluate, score, or prioritize value creation for any PE-backed company. Use when Jake shares a value creation plan, portfolio company financials, board pack, or any document where post-acquisition performance or exit preparation is relevant. Triggers on: "score against the 7 pillars", "evaluate this value creation plan", "what pillars apply here", "assess portfolio company performance", "where is value being created or destroyed", "which levers should we pull", "exit prep CFO review", "is this company exit-ready", "review the operating plan CFO lens", "what's the CFO doing wrong here", or when reviewing any portco documents. Complements the value-creation-plan skill (which builds the output deliverable) and returns-analysis skill (which models the returns) — this skill provides the judgment layer: which pillars to prioritize and why.
---

# Value Creation — 7 Pillars CFO Framework

Evaluate a PE-backed company's value creation strategy, execution quality, and exit readiness against the 7 Pillars framework. The goal is not to build the plan (use [value-creation-plan](../../../private-equity/skills/value-creation-plan/SKILL.md) for that) — it's to apply CFO judgment on what's working, what's missing, and what to prioritize.

**Relationship to other skills:**
- Use [value-creation-plan skill](../../../private-equity/skills/value-creation-plan/SKILL.md) to structure and output the value creation plan document
- Use [returns-analysis skill](../../../private-equity/skills/returns-analysis/SKILL.md) to model IRR/MOIC and attribute returns to value creation levers
- Use this skill to score, prioritize, and stress-test the plan using the 7 Pillars lens
- For MFCF and cashflow quality: see [cashflow-quality skill](../cashflow-quality/SKILL.md)
- For capex deployment quality: see [capex-evaluation skill](../capex-evaluation/SKILL.md)

---

## Step 1: Identify Industry & Load Pillar Priority Matrix

Industry determines which pillars matter most and in what order. Load from [references/industry-contexts.md](../../references/industry-contexts.md#value-creation).

**Industry priority matrix:**

| Sector | Primary Pillars | Secondary Pillars |
|---|---|---|
| Software / SaaS | Open the Throttle, Polish the Trophy | Traveling Light |
| Industrial / Manufacturing | Squeezing the Lemon, Traveling Light | Stop the Bleed, Playing Lego |
| Business Services (roll-up) | Playing Lego, Squeezing the Lemon | Open the Throttle |
| Retail / Consumer | Open the Throttle, Squeezing the Lemon | Polish the Trophy |
| Healthcare | Open the Throttle, Polish the Trophy | Squeezing the Lemon |
| Distressed / Turnaround | Stop the Bleed, Fillet the Fish | Traveling Light |
| Infrastructure | Traveling Light, Polish the Trophy | Squeezing the Lemon |

---

## Step 2: Ingest the Document

| Document Type | What to Extract |
|---|---|
| Value creation plan | Levers identified, $ targets, timelines, owners |
| Board pack / portco update | KPI trends, EBITDA bridge actual vs plan, initiative status |
| Management accounts | Margin trends, revenue growth, WC, capex |
| Exit preparation materials | EBITDA normalization, narrative, banker materials |
| 100-day plan | Priority initiatives, quick wins, reporting structure |

---

## Step 3: Score Against the 7 Pillars

Evaluate each pillar: Is it in the plan? Is it being executed? Is there evidence it's delivering?

---

### Pillar 1 — Traveling Light (Capital Efficiency)

**What it is**: Every dollar on the balance sheet has a purpose. No fat, no latent capital, no dead assets.

**What the CFO owns**:
- Balance sheet rationalization: sell non-core assets, release WC
- MFCF/Net Assets improving over the hold period
- Treasury efficiency: pooling, cash repatriation, debt optimization
- Working capital improvement programs (DSO, DPO, DIO)

**What good looks like**: MFCF/Net Assets improving each year; WC as % revenue declining; asset turns increasing; cash balance actively managed not just accumulated.

**Assess**: Is there a WC improvement plan? Has the asset base been rationalized? Is cash generating a return?

---

### Pillar 2 — Playing Lego (Buy-and-Build / Inorganic Growth)

**What it is**: Use the platform to acquire bolt-ons, accelerate scale, and expand multiple through aggregation.

**What the CFO owns**:
- M&A deal evaluation (IRR vs organic alternative)
- Integration financial management (100-day plan per acquisition)
- Combined chart of accounts, reporting, controls
- Synergy tracking — $ delivered vs $ promised, month by month

**What good looks like**: Bolt-ons acquired at lower multiples than platform's expected exit multiple; integration complete within 100 days; synergies tracked by initiative with clear ownership.

**Assess**: Is there a bolt-on pipeline? Are integrations on track? Are synergies being tracked — or just assumed?

**Red flag**: Buy-and-build strategy with no integration playbook = value destruction risk. Every acquisition adds complexity without a system.

---

### Pillar 3 — Fillet the Fish (Perimeter Shifting / Disposal)

**What it is**: Separate what's profitable from what's dragging the business. Dispose of non-core, unlock the sum-of-parts premium.

**What the CFO owns**:
- Divisional P&L by segment (with allocated vs unallocated cost clarity)
- Sum-of-parts analysis: what is each segment worth independently?
- Carve-out financial preparation for disposals
- Ensuring disposal proceeds are allocated correctly (debt paydown vs reinvestment)

**What good looks like**: Loss-making or low-multiple divisions identified early; disposal timetable agreed with sponsor; remaining core is cleaner, higher-margin, higher-multiple.

**Assess**: Is there a divisional P&L with true contribution? Has anyone run a sum-of-parts? Are there units dragging the multiple that could be sold for value?

**Case study signal**: One site generating $15m EBITDA, two sites bleeding. The answer is obvious — but only if the divisional P&L exists to reveal it.

---

### Pillar 4 — Squeezing the Lemon (Efficiency / Margin Expansion)

**What it is**: Systematic cost reduction and margin improvement without gutting the business.

**What the CFO owns**:
- Cost reduction program design and tracking
- Procurement savings (consolidated supplier base, volume renegotiation)
- Overhead rationalization (shared services, spans and layers)
- OpEx ZBB — challenge every line from zero
- Gross margin improvement (COGS reduction, pricing, mix)

**What good looks like**: Identified $X of cost savings → tracked by initiative → delivered to P&L on schedule. EBITDA margin improving year-on-year without corresponding revenue growth as the primary driver.

**Assess**: Is there a cost reduction program with specific initiative owners and $ targets? Or is cost saving just a hope embedded in the model?

**Red flag**: Lemon squeezed too hard — SG&A cut below sustainable run-rate, R&D gutted, headcount reduced below what's needed to deliver growth. Short-term EBITDA inflation, long-term capability destruction.

---

### Pillar 5 — Open the Throttle (Growth Enablement)

**What it is**: Fund and execute growth — new markets, new products, new channels, pricing power.

**What the CFO owns**:
- Growth investment evaluation (capex envelope for growth)
- Unit economics: does growth pay back? (see [capex-evaluation skill](../capex-evaluation/SKILL.md))
- Revenue quality and sustainability: recurring vs transactional, retention rates
- Financial infrastructure to support scale (systems, controls, reporting)

**What good looks like**: Growth investment generating returns above hurdle rate; unit economics improving as scale grows; financial reporting can keep up with the growing business.

**Assess**: Is growth being funded, or just projected? Is there a stage-gate on speculative growth spend? Are unit economics tracked?

**Red flag**: Growth capex or growth opex deployed without unit economics or return metrics → Nathan problem emerging.

---

### Pillar 6 — Stop the Bleed (Turnaround / Restructuring)

**What it is**: In distressed or underperforming situations — identify and fix the hemorrhage first, before investing in growth.

**What the CFO owns**:
- 13-week cashflow forecast (liquidity management)
- Covenant compliance monitoring
- Lender relationship management
- Cost-right-sizing: what does a sustainable cost base look like?
- Decision: fix, sell, or close each underperforming unit

**What good looks like**: Bleeding stopped within 60–90 days; runway secured; lenders aligned; restructuring complete before growth investment begins.

**Assess**: Is the business losing money? If yes, is there a credible turnaround plan? Does the CFO have 13-week visibility?

**Red flag**: Distressed business trying to "invest through the problem" without first stopping the bleed. Cash runs out before the investment pays off.

---

### Pillar 7 — Polish the Trophy (Exit Preparation)

**What it is**: Prepare the business for exit — reporting quality, narrative, EBITDA normalization, timing.

**What the CFO owns**:
- Exit-grade reporting: clean, auditable, buyer-ready accounts
- EBITDA normalization stress test: will buyers apply the same adjustments?
- Skeleton IM built 12–18 months before exit — rehearse the story, find the weak spots, fix them
- Timing: exit into a favorable market, not when you need to
- Multiple expansion: what's the story that gets us to the higher multiple?

**What good looks like**: Hilton/Blackstone model — years of balance sheet cleanup and EBITDA normalization before a well-timed, well-prepared exit. Dr Martens/Permira — £300m in, £3.7bn out through brand development + DTC + geographic expansion.

**Assess**: Is there a skeleton IM? Is the EBITDA normalization defensible to a buyer's DD team? Is exit timing being managed?

**Red flag**: Polish the Trophy being attempted without the underlying EBITDA substance. A great story around mediocre numbers doesn't hold up in buyer DD.

---

## Step 4: 100-Day Integration Plan Assessment (for new acquisitions)

When evaluating a recently acquired company, assess whether the first 100 days have been structured correctly:

**Days 1–30: Stabilize**
- [ ] Management aligned and retained (compensation agreed, employment confirmed)
- [ ] Financial reporting visibility established (monthly accounts, cashflow)
- [ ] Chart of accounts standardized for consolidated reporting
- [ ] Minimum financial controls in place
- [ ] Quick wins identified (pricing, obvious costs, WC opportunities)

**Days 31–60: Plan**
- [ ] Value creation plan drafted and communicated
- [ ] Top 3–5 initiatives launched with owners and milestones
- [ ] 18-month cashflow forecast built
- [ ] Reporting cadence set (weekly flash, monthly review, quarterly board pack)

**Days 61–100: Execute**
- [ ] First quick wins delivered and quantified
- [ ] First board pack with operating metrics presented
- [ ] Plan adjusted based on early learnings

---

## Step 5: Exit Readiness Assessment

Run this checklist when a portco is 12–24 months from a potential exit:

- [ ] Skeleton IM drafted — does the story hold together?
- [ ] EBITDA normalization: how many adjustment lines? Will buyers accept them?
- [ ] Audit quality: are the last 3 years of accounts clean and audited?
- [ ] Management team: exit-ready? (Buyers pay more for a team that stays)
- [ ] Working capital: peg set correctly, no manipulation risk
- [ ] Capex: no deferred maintenance cliff that emerges in buyer DD
- [ ] Customer contracts: not expiring or at risk at exit timing
- [ ] Multiple expansion story: what's the narrative that justifies a higher multiple?

---

## Step 6: Structured Output

### What We Like
Cite specific evidence from the document:
- e.g., "Squeezing the Lemon is well underway: $2.3m of identified savings, $1.8m delivered in year 1, initiative-level tracking in place"
- e.g., "Skeleton IM drafted 14 months before target exit — story is coherent, EBITDA normalization is defensible (3 lines, all clean)"
- e.g., "Playing Lego pipeline has 3 bolt-ons identified at 5–6x EBITDA vs platform expected exit at 9x — instant multiple arbitrage"

### What We Don't Like
- e.g., "Open the Throttle is the stated priority but there's no stage-gate or return metric on growth spend — $4m deployed with no unit economics tracking"
- e.g., "Value creation plan has no owner for Traveling Light — WC % of revenue has risen 200bps since close, bleeding $1.5m of cash"
- e.g., "Exit is 18 months away but no skeleton IM exists — the normalization story will take 6 months to build, leaving no time to fix weaknesses"

### Where Is the Opportunity
- e.g., "Fillet the Fish is completely absent from the plan — two divisions with negative EBITDA contribution are dragging the multiple; disposing would re-rate the core business from 7x to 9x"
- e.g., "Traveling Light opportunity: DSO of 62 days vs industry average of 38 — a WC program could release $3–4m and fund the next bolt-on"
- e.g., "Synergy tracking from the 2023 acquisition is informal — formalizing this with initiative owners would likely surface an additional $500k of undelivered savings"

### Red Flags
- e.g., "$12m of growth capex deployed over 2 years, EBITDA down 8% — Nathan problem emerging; Open the Throttle is consuming capital without returns"
- e.g., "EBITDA normalization has 14 adjustment lines for a $7m EBITDA business — Polish the Trophy will fail DD when buyers see this"
