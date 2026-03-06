---
name: working-capital
description: Apply CFO-level working capital analysis to any company document or financial data. Use when Jake shares AR/AP aging schedules, balance sheets, management accounts, CIMs, or any document containing receivables, payables, or inventory data. Triggers on: "analyze working capital", "run a WC analysis", "what's the NWC situation", "DSO/DPO/DIO analysis", "is working capital a strength or weakness", "working capital peg", "WC peg negotiation", "negative working capital flywheel", "what does WC look like for this deal", "AR aging", "AP aging", "inventory analysis", or any document containing receivables/payables/inventory data. Proactively triggers during deal diligence and portfolio monitoring workflows.
---

# Working Capital Analysis

Analyze working capital structure, quality, and dynamics for any company. Determine whether WC is a structural strength (self-funding growth flywheel) or a drag (cash trap), assess M&A peg implications, and identify improvement opportunities.

---

## Step 1: Identify Industry & Load Context

Industry determines what "normal" WC looks like. Load the appropriate context from [references/industry-contexts.md](../../references/industry-contexts.md#working-capital).

**Critical calibration question**: Should this business have positive or negative NWC?
- Retail / consumer: should be negative (or close to zero)
- SaaS: typically negative (deferred revenue dominates)
- Manufacturing: typically positive (inventory-heavy)
- Professional services: typically positive (receivables-heavy)
- Getting this wrong inverts the entire analysis

---

## Step 2: Ingest the Document

| Document Type | What to Extract |
|---|---|
| AR aging schedule | Buckets (0-30, 31-60, 61-90, 90+), customer concentration, disputed amounts |
| AP aging schedule | Buckets, supplier concentration, any overdue (vendor relationship risk) |
| Balance sheet | AR, inventory, prepayments vs AP, accruals, deferred revenue |
| Management accounts | WC movement vs prior period and prior year |
| CIM / IM | WC commentary, any disclosed WC adjustments, historical WC % of revenue |
| Financial model | WC assumptions, DSO/DPO/DIO built into projections |

---

## Step 3: Calculate NWC

**True NWC** (operating, not statutory):
```
Operating NWC = Trade Receivables
              + Inventory (RM + WIP + Finished Goods)
              + Prepayments (operating only)
              + Cash Float (minimum operating cash, NOT total cash)
              - Trade Payables
              - Accrued Liabilities (operating)
              - Deferred Revenue (current)

Cash Conversion Cycle (CCC) = DIO + DSO - DPO
  DIO = (Inventory ÷ COGS) × 365
  DSO = (Trade Receivables ÷ Revenue) × 365
  DPO = (Trade Payables ÷ COGS or Purchases) × 365

NWC as % of Revenue: NWC ÷ Revenue × 100
```

**Cash Float distinction**: Cash float is the minimum cash a business needs to function operationally (e.g. petty cash, till floats, minimum bank balance). It's part of WC, not available for allocation. It's NOT the total cash balance.

**What to exclude from NWC**: Total cash (only include float), intercompany balances, financial debt, deferred tax, deal-related accruals, non-recurring items.

---

## Step 4: Assess WC Structure

### 4a. Business A vs Business B Test

**Business A (positive NWC — cash trap):**
- Receivables > Payables + Deferred Revenue
- Growth consumes cash → needs funding → slows growth → higher risk
- Normal for: manufacturing, professional services, project-based businesses
- In these sectors: a POSITIVE NWC is normal but watch the trend

**Business B (negative NWC — flywheel):**
- Payables + Deferred Revenue > Receivables + Inventory
- Growth generates cash → self-funding → compounding flywheel
- Examples: Amazon (paid before it pays suppliers), Costco, SaaS companies
- In retail / consumer: this is the gold standard
- Retail example: DPO 75 days, DIO 15 days, DSO 0 → CCC = -60 days → new $10m store returns $5m in WC inflows within 90 days

**Key insight**: Suppliers with stronger balance sheets and cheaper funding may be WILLING to fund a buyer's growth. This is structural leverage, not desperation.

### 4b. WC Efficiency vs Industry
Compare calculated DSO/DPO/DIO to industry norms:

| Metric | Manufacturing | Services | Retail | SaaS |
|---|---|---|---|---|
| DSO (days) | 45–60 | 45–75 | 0–15 | 30–60 (billings to cash) |
| DPO (days) | 30–60 | 30–45 | 60–90 | 30–45 |
| DIO (days) | 30–90 | N/A | 30–60 | N/A |

Deviations from norms warrant explanation.

### 4c. WC Trend Analysis
Calculate WC % of revenue for each available period:
- Improving (declining %): cash being freed up — positive signal
- Deteriorating (increasing %): cash being consumed — warning signal
- Sudden improvement right before a transaction close: flag as potential pre-close manipulation

### 4d. AR Aging Quality (when aging schedule available)
- **0–30 days**: Current — normal
- **31–60 days**: Watch — slow payment
- **61–90 days**: Concern — follow up needed
- **90+ days**: Elevated risk — provide for or write off
- **Concentration**: Top 3 customers as % of AR — concentration increases collection risk
- **Disputed amounts**: Any on hold? This is de facto bad debt

---

## Step 5: M&A WC Peg Analysis

Use this section specifically for deal contexts.

**What the peg is**: The agreed NWC level the seller delivers at closing. Deviation adjusts the purchase price.

**Peg mechanics**:
```
If closing NWC > peg → buyer pays seller the excess (seller benefit)
If closing NWC < peg → seller pays buyer the shortfall (buyer benefit)
Typical range: worth 1–3% of enterprise value
```

**Peg negotiation strategy:**
- Seller wants the peg as LOW as possible (less WC to deliver)
- Buyer wants the peg as HIGH as possible (more WC received)
- Starting point: average of last 12 months — but challenge what's "normal"
- Defer the negotiation late — you'll be better prepared than the other side
- Watch for: seasonal distortion in the average, pre-close WC manipulation, unusual items

**What to scrutinize in the seller's WC peg proposal:**
- [ ] Includes non-operating items (cash, debt-like items) in the NWC definition?
- [ ] 12-month average skewed by unusually favorable quarters?
- [ ] Spicy accounting policies (aggressive revenue recognition, slow accruals)?
- [ ] DPO being artificially extended pre-close to inflate WC?
- [ ] AR being accelerated pre-close to look better than it is?

**Locked-box vs completion accounts:**
- Locked-box: price fixed at historical date, WC risk stays with seller
- Completion accounts: price adjusted at close, WC risk transfers at signing

---

## Step 6: Structured Output

### What We Like
Cite specific data from the document:
- e.g., "Negative NWC of -$4m (CCC of -35 days) — Business B structure; growth is self-funding"
- e.g., "AR aging is clean: 92% current, 5% 31–60 days, 3% 90+ with no disputed amounts"
- e.g., "DPO of 68 days vs industry norm of 45 — strong supplier relationships, a structural advantage"

### What We Don't Like
- e.g., "DSO has crept from 42 days to 61 days over 3 years — collection discipline weakening"
- e.g., "12% of AR is 90+ days overdue; concentration in two customers creates binary risk"
- e.g., "WC % of revenue has risen from 8% to 14% — $6m of incremental cash being consumed by operations"

### Where Is the Opportunity
- e.g., "DPO of 32 days vs sector norm of 55 days — extending to 45 days alone could release $3–4m"
- e.g., "Inventory DIO of 75 days vs industry average of 45 — inventory management initiative could free $2m"
- e.g., "Deferred revenue grew 20% YoY — if this is structural, it's a hidden WC flywheel advantage"

### Red Flags
- e.g., "WC improved sharply in Q4 (last quarter before close) — potential pre-close manipulation; need monthly WC history"
- e.g., "SaaS company with POSITIVE NWC — deferred revenue is shrinking, billings not converting to cash; revenue quality concern"

---

## Red Flag Reference

**Working capital red flags:**
- [ ] Positive NWC in a business that should be negative (SaaS, retail) — structural concern
- [ ] DSO trending up without revenue growth explanation — collection problems or channel stuffing
- [ ] DPO declining — losing supplier leverage, or paying faster under pressure
- [ ] Inventory DIO spiking — demand slowdown or raw material buildup
- [ ] WC improvement in final reporting period before transaction — pre-close manipulation
- [ ] High AR concentration (top 3 customers >40% of AR) — collection binary risk
- [ ] Deferred revenue declining in a subscription business — billings/renewal problem
- [ ] WC "adjustments" consistently additive to EBITDA in management reporting — real cash consumption hidden
- [ ] Volatile WC swings not explained by seasonality — accounting policy or control weakness

**Industry-specific red flags** → see [references/industry-contexts.md](../../references/industry-contexts.md#working-capital)

---

## Cross-References

- For cashflow quality overall: see [cashflow-quality skill](../cashflow-quality/SKILL.md)
- For deal-specific WC peg: see [deal-diligence skill](../deal-diligence/SKILL.md) and [deal-structuring skill](../deal-structuring/SKILL.md)
- For manufacturing/inventory-heavy WC: see [capex-evaluation skill](../capex-evaluation/SKILL.md)
