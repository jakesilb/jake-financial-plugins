---
name: capital-allocation
description: Apply CFO-level capital allocation analysis to any company document or financial data. Use when Jake shares a CIM, management accounts, board deck, financial model, long-range plan, or any document where investment decisions, cash deployment, or return of capital is at play. Triggers on: "evaluate capital allocation", "how is management deploying capital", "build vs buy analysis", "should they return capital or invest", "capital allocation framework", "what's the return on invested capital", "assess management's capital discipline", "is this a good use of cash", "dividend vs buyback vs reinvestment", "MFCF per share analysis", or when reviewing any document where EBITDA-to-FCF conversion and use of that FCF is relevant. Proactively applies when running LBO, returns analysis, or value creation workflows.
---

# Capital Allocation Analysis

The first duty of any CFO is capital allocation: maximizing long-term MFCF per share. This skill evaluates how well a company deploys the cash it generates, whether management's decisions create or destroy shareholder value, and where the highest-return opportunities lie.

---

## Step 1: Identify Industry & Lifecycle Stage

Capital allocation priorities vary sharply by industry and growth stage. Load context from [references/industry-contexts.md](../../references/industry-contexts.md#capital-allocation).

**Critical calibration:**
- Early-growth tech: almost all MFCF should flow into growth (return metrics are years out)
- Mature industrial: disciplined split between maintenance, growth, and shareholder returns
- Cyclical business: capital structure matters; over-investing at peak cycle is a classic trap
- PE-backed company: capital allocation IS the value creation plan — evaluate against the 7 pillars

---

## Step 2: Ingest the Document

| Document Type | What to Extract |
|---|---|
| CIM / IM | Historical capex, M&A history, dividend policy, debt repayment, share buybacks |
| Financial model | FCF waterfall, uses of cash, projected capex vs growth investment |
| Board deck / LRP | Capital allocation policy stated, investment priorities, return targets |
| Management accounts | Actual vs budget on capex, opex growth, cash position movement |
| PE information memo | Value creation plan, capital deployed by pillar, return timeline |

---

## Step 3: Establish the MFCF Baseline

Capital allocation starts after MFCF. You can't allocate what you haven't generated.

```
MFCF (see cashflow-quality skill for build)
  ↓
Capital Allocation Decisions:
  1. Fix balance sheet weakness (if applicable)
  2. Growth CapEx (return > cost of capital)
  3. Growth OpEx (discretionary — ZBB justified)
  4. M&A (build vs buy)
  5. Return capital (dividends, buybacks, debt repayment)
```

**The broken leg principle**: If the balance sheet is impaired (covenant breach risk, refinancing wall, high leverage in a cyclical), fix it first. You can't run before you can walk. Paying dividends while covenant headroom is shrinking = wrong hierarchy.

---

## Step 4: Evaluate Each Allocation Decision

### 4a. The Core Principle
Return capital to shareholders **unless** there are investments available that generate better returns per dollar than shareholders can achieve elsewhere.

Apple case study as the reference frame:
- Phase 1: R&D investment in iPod/iPhone/iPad = capital allocation into compounding returns
- Phase 2: By 2012, MFCF exceeded reinvestment opportunities → launched history's largest buyback
- Lesson: the right answer changes as the business matures. Know which phase you're in.

### 4b. Decision Hierarchy (evaluate in this order)

**1. Balance Sheet Repair (if needed)**
- Is leverage elevated? Is there a refinancing wall in 12–24 months?
- Are covenants close to being breached?
- If yes: all discretionary capital goes here first. No dividends. No buybacks. No vanity M&A.

**2. Maintenance Operations**
- Is maintenance capex fully funded? (See capex-evaluation skill)
- Is working capital adequately funded for growth? (See working-capital skill)
- If no: fix before any growth allocation.

**3. Growth Investment** (only after 1 and 2 are satisfied)
Evaluate three forms on the same basis — cashflow return per dollar invested:

| Type | Framework | When to prefer |
|---|---|---|
| **Growth CapEx** | Payback + NPV/$ | Organic growth, proven returns, asset-heavy expansion |
| **Growth OpEx** | ZBB + stage-gate | R&D, S&M, headcount growth (treat as capex — build the case) |
| **M&A** | Build vs buy comparison | Market too fragmented / slow / expensive to build organically |

**Build vs Buy decision:**
- Build: lower cost, full control, slower, execution risk
- Buy: faster, proven revenue, integration risk, often expensive
- The right question: "What's the NPV per dollar of each path?" not "Which feels better?"
- M&A at >8x EBITDA vs organic growth at 15x return → organic almost always wins. Do the math.

**ZBB for discretionary opex growth:**
- Don't assume last year's opex is a base. Justify from zero.
- Treat each incremental $1m of opex growth as a capex decision: what cash return does it generate?
- Recurring discretionary opex (R&D, marketing, headcount) can destroy capital silently if not held to return standards.

**Stage-gate for speculative growth:**
- Never commit multi-year opex or capex programs upfront for unproven initiatives
- Gate 1: small exploratory budget → Gate 2: proven concept → Gate 3: full commitment
- Treat the total commitment as a capital allocation envelope with a return hurdle

**4. Return of Capital** (when no better use exists)
- Cash accumulating with no deployment plan = poor capital allocation (latent capital problem)
- Buybacks: value-creating when stock trades below intrinsic value; value-destroying when used to offset SBC dilution without reducing share count meaningfully
- Dividends: signal capital discipline, but reduce flexibility. Don't set a dividend you can't sustain.
- Debt repayment: always beats a distribution if cost of debt > returns available elsewhere in portfolio

### 4c. The "Treat All Investments the Same" Principle

Capex, opex growth, M&A — all are capital allocation decisions. Evaluate all on the same cashflow return framework.

The common failure: opex growth escapes scrutiny because it's "just operating expense." A business that adds $10m/year in headcount, R&D, and marketing without measuring the return is destroying capital as surely as bad capex.

---

## Step 5: Assess Capital Allocation Quality

### 5a. MFCF Per Share Trend
- Calculate or estimate: MFCF ÷ diluted share count
- Is it growing? That's the north star metric.
- EBITDA growing but MFCF/share flat or declining → capital misallocation or dilution

### 5b. MFCF Return on Net Assets (capital efficiency)
- MFCF ÷ Net Assets (PP&E + NWC + Intangibles)
- Trend matters: improving = capital deployed at accretive returns; declining = capital base growing faster than returns

### 5c. Financial Policy — Does One Exist?
- A strong capital allocation culture has a written financial policy: leverage targets, dividend policy, return hurdle rates, M&A criteria
- Without it: decisions are ad hoc, math over-rides framework, outcomes are inconsistent
- In PE context: the 100-day plan IS the financial policy. Does it exist? Is capital being deployed against it?

### 5d. Strategy–Capital Alignment Check
The ultimate coherence test: does where the money goes match what management says their strategy is?

Red flag: management claims "we're a growth company" but 90% of capex is maintenance and there's no investment in new markets. Or: management claims "capital discipline" but approves every project that comes through the door.

---

## Step 6: Structured Output

### What We Like
Cite specific data:
- e.g., "MFCF/share has grown from $1.20 to $2.10 over 4 years — management is compounding value, not diluting it"
- e.g., "Build vs buy math shows organic expansion at 22% CROI vs acquisition targets at 14x EBITDA — management correctly choosing organic"
- e.g., "Stage-gate structure on R&D spend: $2m exploratory → $8m pilot → $25m rollout only after Gate 2 proven — disciplined"

### What We Don't Like
- e.g., "Opex has grown $15m over 3 years with no stated return metric — discretionary spend escaping capital allocation discipline"
- e.g., "Dividends being paid while net leverage is 4.2x with a covenant at 4.5x — wrong hierarchy, balance sheet risk ignored"
- e.g., "M&A at 11x EBITDA when organic growth is generating 25% CROI — management overpaying for speed"

### Where Is the Opportunity
- e.g., "$40m of cash on balance sheet with no deployment plan — ZBB review of opex + stage-gated growth initiative could deploy $25m at >20% return"
- e.g., "Company is mature, MFCF exceeds investment opportunities — buyback program at current valuation would be accretive at ~12% implied yield"
- e.g., "Growth opex has never been subjected to ZBB — a single review cycle could redirect $5–8m from low-return to high-return initiatives"

### Red Flags
- e.g., "3 years of acquisitions totaling $200m, MFCF/share is lower than at the start — serial acquisition strategy destroying value"
- e.g., "Capital allocation policy is verbal, not written — no financial policy means no guardrails"

---

## Red Flag Reference

**Capital allocation red flags:**
- [ ] EBITDA growing but MFCF per share flat or declining
- [ ] Strategy and capital flows don't align (growth narrative, maintenance capex spend)
- [ ] Latent capital (excess cash, undrawn facilities) with no stated deployment plan
- [ ] Dividends paid while balance sheet is impaired or covenants are tight
- [ ] Opex growth outpacing revenue growth with no articulated return metric
- [ ] M&A multiples consistently higher than organic return opportunities
- [ ] No written financial policy → ad hoc decisions, math over-rides framework
- [ ] "Every project is NPV positive" — hurdle rates aren't real
- [ ] SBC dilution growing faster than MFCF per share improvement
- [ ] Growth capex deployed without matching EBITDA improvement (see Nathan problem in capex-evaluation)

**Industry-specific red flags** → see [references/industry-contexts.md](../../references/industry-contexts.md#capital-allocation)

---

## Cross-References

- For MFCF calculation: see [cashflow-quality skill](../cashflow-quality/SKILL.md)
- For individual capex project evaluation: see [capex-evaluation skill](../capex-evaluation/SKILL.md)
- For M&A as a capital allocation decision: see [deal-structuring skill](../deal-structuring/SKILL.md)
- For funding the capital allocation (debt vs equity): see [capital-structure skill](../capital-structure/SKILL.md)
- For PE value creation plan: see [value-creation skill](../value-creation/SKILL.md)
