---
name: capital-structure
description: Apply CFO-level capital structure analysis to any company document or financial data. Use when Jake shares a CIM, lender presentation, cap table, debt schedule, LBO model, or any document where leverage, funding mix, or debt capacity is relevant. Triggers on: "evaluate the capital structure", "what's the debt capacity", "analyze the leverage", "review the debt terms", "is the capital structure appropriate", "covenant analysis", "refinancing risk", "capital structure for this deal", "how much debt can this business carry", "CFADS analysis", "should we use debt or equity", or when reviewing any document with a debt schedule, leverage ratio, or funding structure. Complements the lbo-model skill (which builds the model) and returns-analysis skill (which models returns) — this skill provides the CFO judgment on whether the structure is right for the business.
---

# Capital Structure Analysis

Apply rigorous CFO judgment to assess whether a company's capital structure is appropriate, sustainable, and aligned with its business strategy. Capital structure isn't downstream from strategy — it IS strategy.

**Relationship to other skills:**
- Use [lbo-model skill](../../../financial-analysis/skills/lbo-model/SKILL.md) to build the LBO model mechanics
- Use [returns-analysis skill](../../../private-equity/skills/returns-analysis/SKILL.md) to model IRR/MOIC across leverage scenarios
- Use this skill to assess whether the structure is right, sustainable, and appropriately flexible
- For cashflow generation that services the debt: see [cashflow-quality skill](../cashflow-quality/SKILL.md)
- For capital allocation decisions funded by the structure: see [capital-allocation skill](../capital-allocation/SKILL.md)

---

## Step 1: Identify Industry & Load Context

Business type determines appropriate leverage and structure. Load from [references/industry-contexts.md](../../references/industry-contexts.md#capital-structure).

| Business Profile | Typical Leverage | Structure Notes |
|---|---|---|
| Asset-heavy, predictable cashflows (infrastructure, real estate) | 4–8x EBITDA | High leverage supported by asset collateral and contracted revenues |
| Recurring revenue (SaaS, subscription) | 3–6x EBITDA | Revenue-based facilities; ARR-backed lending increasingly common |
| Cyclical industrial/manufacturing | 1.5–3x EBITDA | Needs flexibility; tight covenants dangerous through the cycle |
| Project-based services | 1–2x EBITDA | Lumpy cashflows limit leverage capacity |
| Distressed / turnaround | Minimize debt | Debt kills turnarounds; flexibility > leverage |

---

## Step 2: Ingest the Document

| Document Type | What to Extract |
|---|---|
| CIM / IM | Sources and uses, debt structure at close, EBITDA and leverage multiples |
| LBO model | Debt schedule, amortization, PIK vs cash pay, covenant tests |
| Lender presentation / CIM | Debt capacity argument, CFADS, leverage ratios, covenant package |
| Cap table | Equity layers, co-invest, management rollover, preferred vs common |
| Debt agreement / term sheet | Covenants (financial and maintenance), pricing, amortization, maturity |

---

## Step 3: Calculate CFADS and Debt Capacity

**CFADS** (Cashflow Available for Debt Service) is the foundational metric. It's what the business can actually use to service debt — not EBITDA.

```
CFADS = EBITDA
      - Cash Tax
      - Cash Interest (on existing debt)
      - Maintenance CapEx
      - Working Capital movements
      - Mandatory debt amortization
      = Cash available to service additional debt

Debt Capacity = CFADS ÷ Debt Service Coverage Ratio (DSCR)
  A DSCR of 1.2x means $1.20 of CFADS for every $1.00 of debt service
  Typical minimum DSCR covenant: 1.1x–1.3x
  Conservative: 1.5x+
```

**Key distinction: EBITDA vs CFADS**
- EBITDA doesn't pay debt — cash does
- Businesses often lever to EBITDA multiples, but the real question is: what's the DSCR?
- A high-EBITDA business with heavy maintenance capex and significant WC consumption may have much less CFADS than the EBITDA multiple suggests

---

## Step 4: Funding Options Taxonomy

### Debt Instruments

**Senior Secured Debt:**
- *Term Loan A/B*: Amortizing; TLA typically bank-held, TLB typically institutional; TLB has minimal amortization (1% p.a.) with bullet at maturity
- *Revolving Credit Facility (RCF)*: Drawn/undrawn as needed; provides liquidity buffer; typically secured; key covenant is headroom
- *Asset-Based Lending (ABL)*: Borrowing base tied to AR/inventory; good for asset-heavy or WC-intensive businesses

**Junior/Subordinated Debt:**
- *Mezzanine*: Subordinated to senior; higher cost; often includes equity kicker (warrants/PIK)
- *PIK (Payment in Kind)*: Interest accrues to principal rather than paid in cash; preserves CFADS but compounds rapidly; use only when cashflow is genuinely constrained in early years
- *Second Lien*: Secured but junior to first lien; higher yield; common in leveraged buyouts
- *High Yield Bonds*: Public market; covenant-lite; large minimums; suited to large-cap

**Private Credit / Unitranche:**
- Single lender provides all debt (combines senior + mezz in one instrument)
- Higher cost but simpler structure; faster to close; increasing market share
- Common in PE mid-market where bank syndication is slow or uncertain

**Specialist / Growth:**
- *Venture Debt*: For growth-stage companies; doesn't dilute equity; tied to milestones
- *Revenue-Based Financing*: Repayment as % of monthly revenue; suits SaaS/recurring models
- *Sale-Leaseback*: Release capital from owned assets; off-balance sheet; quasi-debt

### Equity Instruments
- Sponsor equity (LP capital from fund)
- Management equity / rollover
- Co-invest (LP or third party alongside sponsor)
- Preferred equity (liquidation preference; can distort returns)

### Hybrid
- Convertible notes
- Preferred with equity conversion
- Warrants attached to debt

---

## Step 5: Assess Capital Structure Quality

### 5a. Is Leverage Appropriate?

**Not a multiple question — a CFADS question.** Calculate:
- Leverage ratio: Net Debt ÷ EBITDA (the shorthand)
- DSCR: CFADS ÷ Total Debt Service (the reality)
- Interest coverage: EBITDA ÷ Cash Interest (the stress test)

**The cycle matters**: A 3x leveraged industrial business at cycle peak may be 6x at cycle trough. Capital structure must be sized for the trough, not the peak.

### 5b. Covenant Analysis

Read every financial covenant. Assess headroom under stress:

| Covenant Type | What to Check |
|---|---|
| Leverage (Net Debt / EBITDA) | Current ratio vs covenant; headroom under 20% EBITDA decline |
| DSCR / Interest Cover | How much does EBITDA need to fall before breach? |
| Minimum Liquidity | Is the floor realistic? (Peloton had weekly-tested $250m minimum) |
| Capex limits | Does the covenant allow the maintenance capex the business needs? |
| Restricted payments | Can the company pay management fees, dividends? |

**Covenant stress test**: Model EBITDA declining 20%/30%/40% and identify at what level each covenant breaches.

### 5c. Capital Structure Flexibility

The capital desperation trap: a business that underperforms its plan may not have enough CFADS to refinance on market terms. This inflexibility leaves the company unable to attract reasonable lenders — pushed into the arms of distressed/vulture lenders at punishing rates.

**Flexibility checklist:**
- [ ] Maturity wall: when does debt mature? Is there a refinancing wall within 18 months?
- [ ] Prepayment penalties: can you refinance cheaply if performance improves?
- [ ] RCF undrawn: is there liquidity cushion for operational needs?
- [ ] Covenant headroom: can the business miss plan by 20% without breaching?
- [ ] PIK toggle: if cashflow deteriorates, can interest be deferred?

### 5d. Capital Structure vs Strategy Alignment

**The right structure matches the business's needs:**
- Growth business: needs flexibility, not maximum leverage. Covenant headroom > return optimization.
- Stable cashflow (infrastructure): can lever heavily; use leverage for return enhancement.
- Cyclical business: conservative structure is disciplined, not timid. Heavy leverage at peak = disaster at trough.
- Turnaround: debt kills turnarounds. Minimize financial obligations; maximize management bandwidth.

**WACC note**: Academic WACC optimization (find the mix that minimizes WACC) is mostly irrelevant for mid-market PE CFOs. The real question is: what structure keeps us solvent, flexible, and able to execute the value creation plan? The marginal cost of debt matters more than the theoretical optimum.

---

## Step 6: Structured Output

### What We Like
- e.g., "DSCR of 1.6x at base case — meaningful headroom; business can underperform plan by 25% before debt service is at risk"
- e.g., "Unitranche structure eliminates inter-creditor complexity; faster close and one relationship to manage post-close"
- e.g., "RCF of $20m undrawn provides real liquidity buffer; critical for WC-intensive business with seasonal swings"

### What We Don't Like
- e.g., "Leverage at 5.8x on a cyclical industrial business — at trough EBITDA (historical -35%), this implies 9x leverage and likely covenant breach"
- e.g., "Minimum liquidity covenant tested weekly at $250m — operationally burdensome; management distraction; no buffer for a bad week"
- e.g., "Capex covenant of $8m/year when maintenance capex realistically requires $11m — sets up a covenant breach or deferred maintenance spiral"

### Where Is the Opportunity
- e.g., "PIK toggle available on $30m of mezz — if cashflow is constrained in Year 1 integration, toggle to PIK to preserve CFADS for operations"
- e.g., "Sale-leaseback on owned property could release $15m at close — can de-lever by 0.8x and provide headroom without affecting operations"
- e.g., "RCF is currently undrawn and sized at $15m — increase to $25m at close to provide WC buffer for the seasonal business cycle"

### Red Flags
- e.g., "Net debt / EBITDA of 6.2x on a services business with no hard assets and lumpy project revenue — structure is fragile; single contract loss triggers distress"
- e.g., "Debt matures in 14 months; current EBITDA trending 15% below underwrite — refinancing risk is real and immediate"
- e.g., "No RCF in the structure — zero liquidity buffer for a business with 90-day WC cycle; operational fragility"

---

## Red Flag Reference

**Capital structure red flags:**
- [ ] DSCR below 1.2x at base case
- [ ] Leverage above industry-appropriate range at current EBITDA
- [ ] Debt maturity wall within 18 months with underperforming EBITDA
- [ ] Covenants with <15% headroom under base case
- [ ] Capex covenant limiting maintenance spend below sustainable level
- [ ] No RCF or liquidity facility — no buffer
- [ ] PIK interest accruing on significant portion of debt — compounding rapidly
- [ ] Capital structure designed at peak-cycle EBITDA — trough will breach covenants
- [ ] Lender is a distressed/special situations fund — implies prior distress or desperation capital

**Industry-specific red flags** → see [references/industry-contexts.md](../../references/industry-contexts.md#capital-structure)
