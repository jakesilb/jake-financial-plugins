---
name: deal-diligence
description: Apply CFO-level financial diligence judgment to any deal document. Use when Jake shares a CIM, QoE report, EBITDA bridge, management accounts, data room financials, or any document for a deal being evaluated. Triggers on: "apply CFO lens to this deal", "what are the financial red flags", "evaluate this QoE", "analyze the EBITDA adjustments", "how many adjustment lines", "is the EBITDA real", "what hidden debt might exist", "review this CIM financially", "assess the earnings quality", "what should we focus on in DD", "rate this deal's financial quality", or any time Jake is evaluating a potential acquisition and shares financial documents. Complements the dd-checklist skill (which tracks DD workstreams and status) — this skill provides the analytical CFO judgment layer on top of that process.
---

# Deal Diligence — CFO Analytical Lens

Apply seasoned CFO judgment to assess the financial quality of a deal. This skill is the analytical framework for *what to look for and why* — the pattern recognition that separates a clean deal from a financial minefield.

**Relationship to other skills:**
- Use the [dd-checklist skill](../../../private-equity/skills/dd-checklist/SKILL.md) to scope workstreams, build request lists, and track DD status
- Use this skill to apply the CFO judgment layer: earnings quality, hidden debt, WC risk, and diligence prioritization
- For WC peg mechanics: see [working-capital skill](../working-capital/SKILL.md)
- For capex quality assessment: see [capex-evaluation skill](../capex-evaluation/SKILL.md)

---

## Step 1: Identify Industry & Load Context

Industry changes which DD areas matter most. Load from [references/industry-contexts.md](../../references/industry-contexts.md#deal-diligence).

Generate a customized DD priority list based on sector:
- **SaaS**: Cohort analysis, NRR, churn, ARR quality, capitalized dev costs, SBC
- **Manufacturing**: Asset condition, environmental liabilities, maintenance capex backlog, supplier dependencies
- **Services**: Key person risk, client concentration, utilization trends, non-compete enforceability
- **Healthcare**: Payer mix, reimbursement risk, regulatory compliance, staffing costs
- **Retail/Consumer**: Same-store sales, inventory aging, channel mix, franchise dynamics

---

## Step 2: Ingest the Document

| Document Type | CFO's Primary Focus |
|---|---|
| CIM / IM | EBITDA quality, capex disclosure, WC commentary, management adjustments |
| QoE report | Adjustment count and quality, revenue sustainability, WC normalization |
| EBITDA bridge | Each adjustment line — recurring vs non-recurring, management discretion |
| Management accounts | Trend analysis, seasonality, month-by-month volatility |
| Audited accounts | Accounting policies, related party transactions, audit qualifications |
| Data room financials | Consistency with CIM, gaps, unexplained variances |

---

## Step 3: Establish Scope — The 4–6 Things That Matter

Before analyzing everything, identify the deal assumptions that drive your valuation. If any are wrong, the thesis breaks. These become your DD priority list.

```
Ask: What assumptions underpin my entry price?
  e.g., "EBITDA of $10m is real and recurring"
       "Maintenance capex is only $1m/year"
       "Top 3 customers (80% of revenue) are not at risk"
       "Working capital is structurally negative"

Each assumption → one DD work stream
Don't investigate what can't move the needle at your price
```

**Two-stage process:**
- **Stage 1** (pre-LOI / initial bid): Light-touch — validate headline assumptions, identify show-stoppers early, low cost
- **Stage 2** (final bid): Full FDD — detailed QoE, WC analysis, debt-like items, normalized EBITDA under stress

**Scope management rule**: Challenge every advisor work stream. Advisors expand scope (= fees). Ask for each item: "Which of our 4–6 key assumptions does this test?" If the answer is weak, cut it.

---

## Step 4: Quality of Earnings Assessment

### 4a. Adjusted EBITDA — The Adjustment Line Count Test

Count the number of EBITDA adjustment lines in the bridge. More lines = more judgment = more risk.

| Adjustment Lines | Signal |
|---|---|
| 1–3 lines | Clean — few exceptional items, high earnings quality |
| 4–7 lines | Normal — scrutinize each carefully |
| 8–12 lines | Elevated concern — management working hard to get to a number |
| 12+ lines | Red flag — EBITDA is a management construct, not a fact |

**For each adjustment line, ask:**
1. Is this genuinely non-recurring? (Or does a "one-off" appear every year?)
2. Would an independent auditor accept this treatment?
3. Is the cash impact the same as the P&L impact? (Non-cash adjustments that are recurring = real cost)
4. Is this a re-classification (legitimate) or a removal (need justification)?

**Normalize vs adjust distinction:**
- *Normalization*: Adjusting for unusual events to reveal run-rate performance (fire damage, COVID, founder salary above market). Least contentious.
- *Adjustment*: Making a judgment call on what's "in" vs "out" of normalized earnings. Most contentious — buyer and seller often disagree.

### 4b. Revenue Sustainability
- Is revenue one-time, recurring, or contracted?
- Customer concentration: top customer as % of revenue, trend
- Are revenues growing because of price, volume, or mix? Which is sustainable?
- Contract duration and renewal rates (especially SaaS/services)
- Any pull-forward of future revenues into the LTM period?

### 4c. Margin Representativeness
- Are LTM margins inflated by cost cuts that won't be sustainable post-acquisition?
- Is SG&A below run-rate due to open headcount? (Common pre-sale tactic)
- Has R&D been cut to inflate near-term margins? (Depletes the product pipeline)
- Owner compensation normalized? (Private company CFOs and CEOs often under- or over-pay themselves)

---

## Step 5: Hidden Debt & Debt-Like Items

Run this checklist against every deal. These items reduce equity value but are often omitted from the headline EV.

**Structural hidden debt:**
- [ ] Deferred revenue not reflected in enterprise value (buyer must deliver the service/product without receiving cash)
- [ ] Operating lease obligations (IFRS 16/ASC 842 — are these in EV or excluded?)
- [ ] Pension deficit (underfunded defined benefit schemes)
- [ ] Earnout liabilities from prior acquisitions still on the balance sheet

**Capex-related hidden debt:**
- [ ] Maintenance capex backlog (assets overdue for replacement — buyer will inherit the spend)
- [ ] Environmental remediation liability (especially manufacturing, industrial)
- [ ] IT systems near end of life (buyer must invest post-close — often missed)

**Legal / tax hidden debt:**
- [ ] Litigation — pending claims, disclosed but under-reserved
- [ ] Tax liabilities in close (deferred tax, disputed positions, transfer pricing exposure)
- [ ] HMRC / IRS exposure on prior years not yet agreed

**Structural transaction items:**
- [ ] Shares vs assets deal: shares deal = buyer assumes ALL liabilities (including the unknowns); assets deal = buyer picks what to assume
- [ ] Change of control provisions in material contracts (customer/supplier agreements that terminate or re-price on change of ownership)

**Working capital hidden items:**
- [ ] Overdue payables that should be treated as debt-like (if AP won't be paid without legal pressure, it's a liability beyond normal trading terms)
- [ ] Customer deposits / advance payments that aren't in the WC peg definition

---

## Step 6: Working Capital Assessment

WC is the "last 1–3%" of deal value most buyers leave on the table. See [working-capital skill](../working-capital/SKILL.md) for full analysis.

In the DD context, the key questions:
- Is the WC peg set fairly? (Average of last 12 months — but is that average "normal"?)
- Are there spicy accounting policies affecting WC? (Aggressive revenue recognition, slow accruals)
- Is WC volatile? (High volatility = higher risk that actual WC at close diverges from peg)
- Has WC been manipulated pre-close? (Spike in collections, extension of payables = window dressing)

---

## Step 7: Structured Output

### What We Like
Cite specific items from the document:
- e.g., "Only 3 EBITDA adjustments, all clearly non-recurring (legal settlement, COVID relief, founder excess compensation) — clean earnings quality"
- e.g., "Top customer is 18% of revenue, 5-year contract with 2 years remaining — concentration manageable and contracted"
- e.g., "Stage 1 FDD confirms our key assumptions; no show-stoppers found at initial bid level"

### What We Don't Like
- e.g., "11 EBITDA adjustment lines totaling $2.1m on a $6.4m EBITDA base — nearly 33% of earnings is management judgment; this is the number to probe"
- e.g., "Maintenance capex disclosed at $400k vs D&A of $1.8m — suspect deferred maintenance; likely $1m+ of additional annual spend not in the model"
- e.g., "No disclosure of change-of-control provisions in customer contracts — a single customer on auto-terminate could remove 25% of revenue"

### Where Is the Opportunity
- e.g., "EBITDA adjustments include $600k 'owner perks' (car, travel, family payroll) — these are real and recoverable; don't give them back in price"
- e.g., "WC peg is set at 12-month average, but Q4 is structurally favorable — negotiate the peg to exclude Q4 data; saves ~$300k"
- e.g., "Hidden capex backlog creates a price negotiation lever: quote the $1.5m deferred maintenance as a price reduction"

### Red Flags
- e.g., "Revenue grew 25% in LTM but management can't explain the driver beyond 'strong demand' — investigate whether pull-forward distorts the run-rate"
- e.g., "Auditor qualified the 2022 accounts on revenue recognition — not disclosed in CIM"

---

## Red Flag Reference

**Financial diligence red flags:**
- [ ] EBITDA adjustment count > 8 lines
- [ ] A "one-off" item appears in multiple periods
- [ ] Management resistant to providing monthly P&L or WC schedule
- [ ] Audited accounts differ materially from management accounts — unexplained gap
- [ ] Revenue recognition policy more aggressive than industry peers
- [ ] SG&A suspiciously low vs revenue in LTM (headcount gap, cut costs pre-sale)
- [ ] Capex materially below D&A for 2+ years — deferred maintenance building
- [ ] Tax returns not provided or redacted significantly
- [ ] Key customer contract not available in data room
- [ ] Change of control provisions not disclosed
- [ ] WC improved sharply in the quarter immediately before signing

**Industry-specific red flags** → see [references/industry-contexts.md](../../references/industry-contexts.md#deal-diligence)
