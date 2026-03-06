---
name: cashflow-quality
description: Apply CFO-level cashflow quality analysis to any company document or financial data. Use when Jake shares a CIM, management accounts, financial model, P&L, cashflow statement, or any financial document and wants to understand cashflow quality. Triggers on: "evaluate cashflow quality", "analyze free cashflow", "how good is the cash conversion", "what's the MFCF", "EBITDA to FCF conversion", "is the cash real", "analyze this company's cashflow", "cashflow red flags", "how much cash does this business generate", or when reviewing any financial document for PE diligence or portfolio monitoring. Also triggers proactively when a financial document is shared that contains EBITDA, capex, or cashflow data.
---

# Cashflow Quality Analysis

Apply the Maintainable Free Cashflow (MFCF) framework to any company document or financial data to determine whether reported earnings translate into real, durable cash — and how much of it is genuinely available for capital allocation.

---

## Step 1: Identify Industry & Load Context

Before any analysis, identify the company's industry. This changes thresholds, what counts as maintenance vs growth capex, and what "good" looks like.

**Ask or infer from the document:**
- What sector? (SaaS, manufacturing, services, healthcare, retail, infrastructure, financial services)
- What's the revenue model? (recurring, project, transactional, contract)
- What growth stage? (early-growth, scaling, mature, declining)

Then load the relevant industry context from [references/industry-contexts.md](../../references/industry-contexts.md#cashflow-quality).

---

## Step 2: Ingest the Document

Accept whatever Jake provides and identify what's available:

| Document Type | Key Data to Extract |
|---|---|
| CIM / IM | Historical P&L, EBITDA bridge, capex table, working capital commentary |
| Management accounts | Monthly P&L, cashflow statement, BS movements |
| Financial model | FCF build, capex schedule, WC assumptions |
| Audited accounts | Cash from operations, capex, D&A, WC movements |
| AR/AP aging | DSO/DPO calculation, concentration, overdue buckets |

If data is partial, note what's missing and what assumptions are being made.

---

## Step 3: Build the MFCF Stack

Reconstruct MFCF from available data. Work top-down from EBITDA:

```
Reported EBITDA
- SBC (estimated cash cost — see note below)
- Maintenance CapEx (not total capex — separate maintenance from growth)
- Maintenance R&D (existing products only; growth R&D is below the line)
± Working Capital movements (operating WC only, not acquisition-related)
- Interest (cash interest, not notional)
- Tax (cash taxes, not accounting tax expense)
= MFCF (Maintainable Free Cashflow)

Below the line (capital allocation — excluded from MFCF):
- Growth CapEx
- Growth R&D
- Acquisitions
- Dividends / buybacks
```

**SBC Note**: Estimate annual SBC cost as (total grants outstanding × grant price) ÷ average vesting period. Do NOT add back. Treat as real cash cost that dilutes shareholders even if it doesn't hit the bank.

**The Coffee Machine Test** — separating maintenance from growth capex:
- Maintenance: spend required to keep the business operating at current level. If you don't spend it, revenue declines. Example: replacing worn equipment on its natural cycle.
- Growth: spend that creates new capacity or revenue. Example: opening a new site.
- When in doubt: ask "if we stopped this spend, what happens to current revenue?" If it falls, it's maintenance.

---

## Step 4: Assess Cashflow Quality

Run each quality check and flag issues:

### 4a. EBITDA-to-MFCF Conversion
Calculate: MFCF ÷ EBITDA

| Conversion Rate | Signal |
|---|---|
| >70% | High quality — most EBITDA converts to real cash |
| 50–70% | Normal — watch for trend direction |
| 30–50% | Elevated concern — investigate what's consuming cash |
| <30% | Red flag — EBITDA is materially overstating real cash generation |

Conversion varies by industry (see industry-contexts.md). SaaS should be high; manufacturing with heavy capex will naturally be lower.

### 4b. Working Capital Trend
- Is WC consuming or generating cash? Sustained WC outflow in a mature business is a red flag.
- Are WC adjustments consistently positive in EBITDA bridges? This means cash quality is eroding.
- Is WC seasonally explained, or structurally deteriorating?

### 4c. Capex Classification
- Total reported capex vs what the business describes as maintenance
- Has maintenance capex been understated to inflate apparent FCF? Signs: aging assets, deferred replacement cycles, growing maintenance costs in OpEx
- Is growth capex generating the promised returns? Compare EBITDA growth to cumulative growth capex deployed

### 4d. SBC Adjustment
- Is SBC large relative to EBITDA? Tech/SaaS companies commonly add back SBC to get to "adjusted EBITDA" — strip it back out
- Has diluted share count been growing? If yes, SBC is a real and recurring cost

### 4e. MFCF Return on Net Assets
Calculate: MFCF ÷ Net Assets (PP&E + NWC + Intangibles)

This is the efficiency metric. A business generating 15% MFCF/NA is more capital-efficient than one generating 8%. Trend matters as much as level — is it improving or eroding as the asset base grows?

---

## Step 5: Structured Output

Produce analysis in this format:

### What We Like
List specific positive observations with data citations:
- e.g., "MFCF conversion of 74% over the last 3 years — sustainably high, suggesting EBITDA is real cash"
- e.g., "WC has been a consistent cash generator (-$2m annually) driven by 60-day payables vs 30-day receivables"

### What We Don't Like
List concerns with data citations:
- e.g., "Maintenance capex disclosed at $3m vs D&A of $8m — suspicious gap suggests deferred investment"
- e.g., "SBC addback of $4m annually inflates 'adjusted EBITDA' — real cash EBITDA is ~15% lower"

### Where Is the Opportunity
Identify where cashflow improvement levers exist:
- e.g., "WC cycle is 45 days vs industry norm of 25 — AR management improvement could release $3-5m"
- e.g., "Maintenance capex is understated; a buyer who normalizes this should expect $2m higher recurring capex"

### Red Flags
Specific items requiring follow-up in diligence:
- e.g., "EBITDA has grown 40% over 3 years but FCF is flat — investigate capex classification and WC movements"

---

## Red Flag Reference

**Cashflow quality red flags:**
- [ ] EBITDA growing but MFCF flat or declining
- [ ] Sustained positive WC adjustments in EBITDA bridge (cash being consumed by WC growth)
- [ ] Total capex close to D&A — suggests little maintenance/growth split discipline
- [ ] Management discloses "growth capex" of 80%+ of total — cherry-picking the label
- [ ] SBC is material and consistently added back in "adjusted" metrics
- [ ] MFCF/Net Assets ratio declining over time despite EBITDA growth
- [ ] 13-week cash forecast or covenant compliance being managed tightly — liquidity stress signal
- [ ] FCF only positive in H2 (seasonal) but described as structural
- [ ] Significant gap between accounting D&A and actual capex — either deferred maintenance or bloated intangibles

**Industry-specific red flags** → see [references/industry-contexts.md](../../references/industry-contexts.md#cashflow-quality)

---

## Cross-References

- For working capital detail: see [working-capital skill](../working-capital/SKILL.md)
- For capex sizing: see [capex-evaluation skill](../capex-evaluation/SKILL.md)
- For capital allocation decisions below the MFCF line: see [capital-allocation skill](../capital-allocation/SKILL.md)
- For deal-specific cashflow analysis: see [deal-diligence skill](../deal-diligence/SKILL.md)
