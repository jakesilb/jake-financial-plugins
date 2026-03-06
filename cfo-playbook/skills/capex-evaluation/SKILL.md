---
name: capex-evaluation
description: Apply CFO-level CapEx evaluation frameworks to any company document or financial data. Use when Jake shares a capex schedule, business case, investment proposal, CIM with capex tables, financial model, or any document containing capital expenditure data. Triggers on: "evaluate this capex", "size the capex envelope", "analyze capex", "review this investment case", "maintenance vs growth capex", "is this capex justified", "capex red flags", "what's the capex quality", "rate of return on this investment", "should we approve this project", "post-investment review", or when reviewing any document containing PP&E, depreciation, capex schedules, or investment proposals. Also triggers proactively when a CIM or financial model is shared that shows capex materially diverging from D&A.
---

# CapEx Evaluation

Apply a rigorous, CFO-grade framework to evaluate capital expenditure quality, sizing discipline, and return credibility. Works on individual projects, annual capex programs, or capex history in a company you're evaluating.

---

## Step 1: Identify Industry & Load Context

Industry fundamentally changes what "capex" means and what normal looks like.

**Ask or infer from the document:**
- Asset intensity: heavy (manufacturing, infrastructure) vs light (services, SaaS)?
- Revenue model: what does capex directly enable or protect?
- Growth stage: expanding footprint or maintaining existing base?

Key industry lens for capex:
- **Manufacturing/Industrial**: Capex IS the business. Maintenance/growth split is everything.
- **Retail/Consumer**: Store buildouts = growth capex; refurbs = maintenance. Unit economics per store = capex decision.
- **SaaS/Tech**: Physical capex is minimal. Real "capex" is R&D and CAC — apply envelope thinking there.
- **Infrastructure**: All capex is strategic. Asset condition assessment is critical.
- **Services**: Capex near zero. "Capex thinking" applies to headcount and system investments.

Load full industry detail from [references/industry-contexts.md](../../references/industry-contexts.md#capex-evaluation).

---

## Step 2: Ingest the Document

| Document Type | What to Extract |
|---|---|
| CIM / IM | Capex table (historical + projected), maintenance vs growth split disclosed, D&A schedule |
| Financial model | Capex schedule, D&A, capex assumptions, return metrics per project |
| Management accounts | Actual capex vs budget, YTD spend, project status |
| Investment proposal / business case | Project description, spend profile, return metrics (NPV, IRR, payback), assumptions |
| PP&E note (audited accounts) | Additions, disposals, depreciation charge, asset age profile |

---

## Step 3: Size and Characterize the CapEx Envelope

### 3a. Total Envelope Assessment
Determine whether the total capex budget is appropriately sized. Four inputs:

| Input | Question to Answer |
|---|---|
| Access to capital | What funding sources are available? What's their cost and capacity? |
| Cost of capital | Cheaper capital → larger envelope is justified |
| Quality of pipeline | Are there enough return-generating projects to fill the envelope? |
| Execution ability | Can the organization absorb and deliver this level of spend? |

**Red flag**: Envelope sized by what's available (cash on hand, debt capacity) rather than what the opportunity pipeline justifies. This leads to capital destruction.

### 3b. Maintenance vs Growth Split

**The Coffee Machine Test:**
- Maintenance CapEx = spend required to keep the business operating at its current level. If not spent, revenue declines.
- Growth CapEx = spend that creates new capacity or increases future cash generation.
- Test: "If we stopped this spend, what happens to current revenue?" → Falls = maintenance. Grows = growth. Unclear = dig harder.

```
Total CapEx = Maintenance CapEx + Growth CapEx

Maintenance CapEx Proxy Check:
  Realistic maintenance capex is usually close to D&A (within ±20-30%)
  If reported maintenance capex << D&A → deferred maintenance building
  If reported maintenance capex >> D&A → either assets deteriorating fast, or misclassification
```

**Management's disclosed split vs reality check:**
- Does management claim 80%+ of capex is "growth"? That's a red flag — cherry-picking the label.
- Compare maintenance capex to replacement cost of asset base. Does it make sense on a 10-year replacement cycle?

---

## Step 4: Evaluate Individual Projects or Program

### 4a. Classify Each Project: Hard vs Soft Return

| Type | Characteristics | Outcome Distribution |
|---|---|---|
| **Hard Return** | Proven payback: automation, cost removal, proven rollout programs | Tight — high confidence |
| **Soft Return** | Speculative: new markets, capacity expansion, unproven demand, untested payback | Wide — fat-tailed |

Plot on bubble chart mentally (or produce one):
- X-axis: Payback period
- Y-axis: NPV per $ invested
- Bubble size: $ investment
- Color: hard (green) vs soft (amber/red)

### 4b. Preferred Evaluation Metrics

**Primary — Payback Period:**
- Everyone understands it. Strong for cash-constrained businesses and downside protection.
- Question: "How many months before we get our money back?"
- Normalize for business risk: a 24-month payback on a hard-return automation project ≠ a 24-month payback on an unproven new market entry.

**Secondary — NPV Per $ Invested:**
- NPV ÷ total capex invested = capital efficiency metric
- Captures time value of money AND return per dollar (avoids the problem of $100m NPV on $1bn investment looking equivalent to $100m NPV on $5m investment)
- Use a hurdle rate that reflects risk (hard return = WACC; soft return = WACC + meaningful risk premium)

**Supplementary — CROI (Cash Return on Investment):**
- Mature annual cash generation ÷ total upfront investment
- Simple, easy to communicate. Useful for operational reviews.
- Limitation: ignores time value of money and the J-curve (early years are negative, maturity takes time)

**Avoid as primary metric:**
- Standalone IRR: can be gamed via reinvestment rate assumptions
- Standalone NPV: doesn't capture capital efficiency

### 4c. The Poker-Not-Chess Mental Model

Approving capex is not chess (all cards visible → calculate optimal move). It's poker: there are cards in play you cannot see.

Implications:
- Don't evaluate at point estimates. Build probability-weighted distributions.
- Hard return: tight distribution → single best-estimate is reliable
- Soft return: wide distribution → present base / upside / downside scenarios with explicit probability weights
- Question for soft returns: "What would it take for this to fail?" If the failure case is plausible and the downside is large, that's a no.

### 4d. Stage-Gate for Soft Returns

Never commit the full envelope upfront to speculative projects. Structure as stage-gates:
1. **Gate 1** (exploratory): Small budget to prove concept / test demand
2. **Gate 2** (pilot): Scale if Gate 1 proves out; commit more capital
3. **Gate 3** (rollout): Full commitment only once payback is "hard" — proven, tight distribution
4. **"Burn the Boats"** moment: formal full approval. Make it a real decision with real accountability.

---

## Step 5: Post-Investment Assessment (when reviewing a portfolio company)

If evaluating a company that has already deployed capex, assess delivery quality:

**Success criteria:**
- On Time: commissioned and operational by agreed launch date
- On Budget: total spend within approved amount

**Return delivery:**
- Did the EBITDA improvement promised actually materialize?
- Calculate: EBITDA change in period ÷ cumulative growth capex deployed = realized CROI
- Compare to promised return metrics in the original business case

**The Nathan Problem:**
$100m+ of growth capex deployed over 3 years → EBITDA flat or down → capital destruction. This is a PE value destruction pattern. If you see it in a target, ask hard questions about the pipeline quality and approval discipline.

**Post-Investment Review (PIR) culture:**
- Does the company formally review capex returns post-delivery?
- If no PIR process → no accountability loop → incentive to over-promise persists

---

## Step 6: Structured Output

### What We Like
Cite specific data:
- e.g., "Maintenance capex of $8m vs D&A of $9m — well-matched, suggesting realistic asset maintenance discipline"
- e.g., "Hard/soft return split of 70/30 with stage-gate on the three soft-return projects — good process discipline"
- e.g., "New store CROI of 28% on proven format — tight outcome distribution, reliable payback"

### What We Don't Like
- e.g., "Management classifies 85% of capex as 'growth' with $3m maintenance vs $12m D&A — deferred maintenance is building a cliff"
- e.g., "Business case projects 22% IRR using 3.5% WACC and optimistic terminal value assumptions — strip these out and IRR falls to ~10%"
- e.g., "No PIR process — three prior major capex projects unreviewed; no accountability for delivery"

### Where Is the Opportunity
- e.g., "Stage-gate discipline is absent on soft-return projects — implementing gates could prevent another Nathan-style capital loss"
- e.g., "Maintenance capex has been below D&A for 4 years — asset refresh backlog is creating a buyer opportunity if acquired at the right price"
- e.g., "Strong pipeline of hard-return automation projects sitting unfunded due to conservative envelope sizing"

### Red Flags
- e.g., "$120m deployed over 3 years with EBITDA flat — investigate whether growth capex ever delivered; may be maintenance in disguise"
- e.g., "All 11 submitted projects show positive NPV — in a business with real capital constraints, this means the hurdle rate isn't being applied"

---

## Red Flag Reference

**CapEx quality red flags:**
- [ ] Reported maintenance capex consistently below D&A → deferred maintenance cliff
- [ ] 80%+ of total capex labeled "growth" by management → cherry-picking the classification
- [ ] No stage-gate structure on speculative projects → full exposure to soft-return downside
- [ ] Every business case shows positive NPV or IRR above hurdle → hurdle rate not real
- [ ] Projects regularly 25%+ over budget or timeline → systemic execution risk
- [ ] No PIR culture → no accountability loop, over-promising incentive intact
- [ ] Growth capex deployed without matching EBITDA improvement → Nathan problem
- [ ] Capex envelope sized by available cash, not opportunity quality → capital likely wasted
- [ ] SaaS/tech company with minimal physical capex but no framework applied to R&D or S&M spend → hidden capex-equivalent going unevaluated

**Industry-specific red flags** → see [references/industry-contexts.md](../../references/industry-contexts.md#capex-evaluation)

---

## Cross-References

- For maintenance vs growth split in cashflow context: see [cashflow-quality skill](../cashflow-quality/SKILL.md)
- For total capital allocation decisions (capex vs M&A vs buybacks): see [capital-allocation skill](../capital-allocation/SKILL.md)
- For capex assumptions in deal context: see [deal-diligence skill](../deal-diligence/SKILL.md)
- For capex funding and leverage capacity: see [capital-structure skill](../capital-structure/SKILL.md)
