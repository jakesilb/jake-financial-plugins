---
name: deal-structuring
description: Apply CFO-level deal structuring analysis to any transaction document or deal scenario. Use when Jake shares a term sheet, LOI, SPA draft, deal summary, or is evaluating how to structure an acquisition. Triggers on: "structure this deal", "review the deal terms", "price vs terms analysis", "seller note mechanics", "earnout design", "how should we structure this acquisition", "WC peg negotiation", "locked box vs completion accounts", "what should the terms look like", "SMB deal structure", "asset vs stock deal", "is this fairly structured", or when analyzing any deal where price, financing structure, or risk allocation is at play.
---

# Deal Structuring — CFO Framework

Deal structuring is where CFO judgment creates or preserves equity value beyond the headline price. Terms can transform the risk profile of a deal without changing what you pay — or dramatically reduce effective price through the right mechanics.

**Relationship to other skills:**
- Use [deal-diligence skill](../deal-diligence/SKILL.md) for the financial quality assessment that informs structure
- Use [working-capital skill](../working-capital/SKILL.md) for WC peg mechanics
- Use [returns-analysis skill](../../../private-equity/skills/returns-analysis/SKILL.md) to model how structure impacts IRR/MOIC
- Use [ic-memo skill](../../../private-equity/skills/ic-memo/SKILL.md) to document the final deal terms

---

## Step 1: Identify Deal Type & Industry Context

Deal structure varies significantly by deal size and sector. Load context from [references/industry-contexts.md](../../references/industry-contexts.md#deal-structuring).

| Deal Type | Structural Characteristics |
|---|---|
| **SMB** (<$5m EV) | Seller note dominates; earnout common; focused DD; personal guarantees; 1.5–3x net earnings multiples |
| **Lower mid-market** ($5–50m EV) | Mix of bank debt + seller note + equity; standard QoE; full FDD; completion accounts common |
| **Mid-market** ($50–250m EV) | Senior + junior debt stack; equity from fund; sell-side QoE package; locked-box common |
| **Large-cap** (>$250m EV) | Complex cap stack (TL, RCF, mezz, PIK); full sell-side DD package; no seller note; auction process |

---

## Step 2: Price vs Terms Framework

**The most important principle in deal structuring**: Agree price and terms together. Terms can transform risk without changing headline price.

```
Headline Price ≠ Effective Price

Effective Price = Headline Price
               - WC peg benefit / (detriment)
               - Debt-like items identified and deducted
               - Earnout contingency (reduces upfront cash)
               + Seller note (defers cash outflow)
               ± Completion accounts adjustment
```

**Classic mistake**: CEO agrees headline price based on IM before anyone has reviewed terms. By the time terms are negotiated, the other side has anchored to the number and you've lost leverage on everything else.

**The rule**: Price and terms are a package. Evaluate both simultaneously.

---

## Step 3: Seller Note — Mechanics & Strategic Value

A seller note (vendor financing) is where the seller accepts deferred payment rather than cash at close.

### Why Seller Notes Matter

1. **Funds the deal**: In SMB acquisitions, a seller note can fund the entire transaction (the $0-down structure). At mid-market, it bridges valuation gaps.

2. **Keeps the seller honest**: The seller has ongoing skin in the game. If business deteriorates post-close, they feel it. This is truth serum — sellers who are confident in the business accept notes. Sellers who know something's wrong resist.

3. **Aligns transition incentives**: Seller is motivated to make the handover work while the note is outstanding.

4. **Improves buyer returns**: Deferred cash outflow improves Day 1 equity metrics and IRR.

### Seller Note Design

| Element | Typical Range | Considerations |
|---|---|---|
| Note size | 20–100% of EV (SMB); 10–30% (mid-market) | Higher note = seller retains more risk |
| Interest rate | 4–8% (market rate) | Below-market rate = economic benefit to buyer |
| Term | 24–60 months | Shorter = seller gets paid faster; longer = buyer has more runway |
| Payment holiday | 6–12 months | Gives buyer time to stabilize before payments begin |
| Security | Often unsecured (junior to bank debt) | Senior lenders typically require seller note to be subordinated |
| Offset rights | Buyer can offset indemnity claims against note | Critical protection — must negotiate this in |

**Seller note red flags:**
- Seller demands cash-only → they know something's wrong, or they don't trust the buyer to perform
- No offset rights → you lose protection on undisclosed liabilities
- Note structured senior to bank debt → creates capital structure problems

---

## Step 4: Working Capital Peg Negotiation

WC is worth 1–3% of enterprise value. Full mechanics in [working-capital skill](../working-capital/SKILL.md).

### Deal Structuring Lens on WC

**The negotiation is about the peg level, not the mechanic.** Both sides agree NWC will be normalized — the fight is what "normal" is.

**Buyer strategy:**
- Set peg HIGH (want more WC delivered at close)
- Challenge the 12-month average if it contains favorable outliers
- Exclude Q4 or seasonal peaks from the normalization if they inflate the average
- Push for detailed monthly NWC schedule — reveals volatility and seasonality
- Defer negotiation as long as possible — later in process, you've analyzed more data, seller is under time pressure

**Seller strategy:**
- Set peg LOW (deliver less WC, keep more cash)
- Argue the most favorable period is "normal"
- Lump unusual items into the WC definition that buyer should exclude

**Key negotiation levers:**
1. What's included in NWC definition (cash float, accruals, deferred items)
2. Whether overdue payables are WC or debt-like
3. Seasonal normalization methodology
4. Locked-box date vs completion accounts (locked-box eliminates WC negotiation post-signing)

---

## Step 5: Earnout Design

Earnouts bridge valuation gaps — buyer pays for performance, seller earns upside if they deliver.

### When to Use Earnouts
- When seller and buyer have different views on future performance
- High-growth business where value is mostly in the future
- Key person dependency — incentivize seller to stay
- Life sciences / milestone-based businesses

### Earnout Design Principles

**Metric selection:**
| Metric Type | Best For | Risks |
|---|---|---|
| Revenue | Growth companies; hard to manipulate; forward-looking | Seller can chase revenue at the expense of margin |
| EBITDA | Mature, stable businesses; aligns to delivered value | Subject to accounting discretion; buyer can manage costs to depress it |
| Milestone | Life sciences, pre-revenue tech; specific deliverables | Binary risk; disputes over milestone definition |
| MFCF | When cashflow quality matters most | Complex to define and track; less common |

**Structural rules for clean earnouts:**
- [ ] Short duration: 12–24 months maximum. Longer = higher dispute risk.
- [ ] Simple metric: one metric, clear definition agreed in the SPA. Two metrics = confusion.
- [ ] Buyer can't game it: if buyer controls the metric (e.g., EBITDA), define what costs can be allocated to the earnout entity
- [ ] Seller must run the business: specify any restrictions on buyer interfering with earnout business decisions
- [ ] Cash settlement: pay in cash, not equity (avoids dilution disputes)
- [ ] Hard cap: total earnout has a maximum payout
- [ ] Offset rights: buyer can offset any SPA claims against earnout

**Earnout red flags:**
- Duration >3 years → dispute probability approaches certainty
- EBITDA earnout with no cost allocation restrictions → buyer can kill the earnout by loading costs
- No offset rights → you lose protection on post-close claims
- Seller is not staying post-close → earnout without the seller present is nearly unenforceable

---

## Step 6: Shares vs Assets

**Assets deal** (buyer acquires assets, not the legal entity):
- Buyer chooses which liabilities to assume → avoids unknown/undisclosed liabilities
- Seller retains entity (and its liabilities)
- Step-up in tax basis → higher depreciation deductions for buyer
- More complex to execute (title transfer, contract novation)

**Shares deal** (buyer acquires the legal entity):
- Buyer assumes ALL liabilities, known and unknown
- Simpler execution — entity continues trading as-is
- No step-up in tax basis
- Requires thorough DD to identify hidden liabilities (see [deal-diligence skill](../deal-diligence/SKILL.md))

**CFO guidance**: Prefer assets deal when DD is limited or when there are known/suspected liability exposures. Shares deal is fine when DD is thorough and representations/warranties insurance is in place.

---

## Step 7: Locked-Box vs Completion Accounts

**Completion accounts** (traditional):
- Price set at signing, adjusted after close based on actual balance sheet
- WC adjustment happens post-close
- More protection for buyer (gets actual delivered value)
- Creates uncertainty and post-close disputes

**Locked-box** (increasingly common in PE):
- Price set at a historical balance sheet date (the "locked-box" date)
- No post-close adjustment — seller keeps/delivers exactly the locked-box balance sheet
- Any "leakage" (dividends, management fees, related party payments) between locked-box date and close is prohibited
- Simpler and more certain — no post-close price disputes
- Better for sellers who want certainty; requires strong DD on the historical BS

---

## Step 8: Structured Output

### What We Like
Cite specific terms:
- e.g., "25% seller note at 5% interest, 6-month holiday, with offset rights — keeps seller motivated, protects against undisclosed liabilities, improves buyer Day 1 IRR by ~200bps"
- e.g., "Assets deal structure given the environmental uncertainty — eliminates the risk of inheriting undisclosed remediation liabilities"
- e.g., "WC peg set at $4.2m based on 12-month average excluding the seasonal Q4 spike — accurately reflects the run-rate business"

### What We Don't Like
- e.g., "Revenue-based earnout over 48 months with no seller remaining post-close — unenforceable and will end in dispute"
- e.g., "Completion accounts structure with a broad NWC definition — sets up a post-close dispute; push for locked-box with a clean BS"
- e.g., "No offset rights on the seller note — we're exposed to post-close claims with no recourse"

### Where Is the Opportunity
- e.g., "WC peg negotiation hasn't started — based on our analysis, moving the peg from $3.8m to $4.5m is worth ~$700k at close"
- e.g., "Seller is highly motivated to close quickly — offer a slightly higher headline price in exchange for a larger seller note; improves our IRR while appearing generous"
- e.g., "Earnout on new product launch milestones (not EBITDA) would bridge the $2m valuation gap without buyer assuming execution risk"

### Red Flags
- e.g., "Cash-only demand from seller on a business where 30% of revenue is from one customer — seller knows something about that customer relationship"
- e.g., "SPA representations and warranties are weak with 12-month limitation period — this is not enough given the complexity of the tax exposure found in DD"
