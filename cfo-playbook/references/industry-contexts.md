# CFO Playbook — Industry Contexts

Industry-specific calibration for all CFO playbook skills. Every skill loads the relevant section here before running analysis.

---

## How to Use This File

When a skill is invoked, identify the target company's industry and load the relevant section. This changes:
- What "normal" looks like for each metric
- Which frameworks are most important
- What red flags apply (vs what's normal for the sector)
- Where the highest-leverage analysis time should go

---

## Software / SaaS

### Cashflow Quality
- MFCF: SBC is the defining distortion. Strip out the SBC addback that inflates "adjusted EBITDA." Rule of 40 (revenue growth % + FCF margin %) as a proxy for MFCF efficiency.
- Real "capex" in SaaS is R&D and CAC — apply envelope thinking to both. Capitalized development costs inflate margins and understate cashflow consumption.
- Revenue recognition (ASC 606): billings vs revenue divergence reveals underlying growth trajectory. Billings growing faster = healthy; billings lagging = demand warning.
- Net Dollar Retention (NRR) is a cashflow predictor: NRR > 120% = self-compounding; NRR < 100% = churn destroying value.

### Working Capital
- Typically **negative NWC** (deferred revenue > receivables) — this is healthy, not a concern.
- Red flag: POSITIVE NWC in a SaaS company = deferred revenue shrinking = billings declining = revenue quality deteriorating.
- DSO benchmarks: 30–60 days typical; annual contract billing cycles create receivable spikes.

### CapEx Evaluation
- Physical capex is minimal. Apply capex envelope thinking to:
  - R&D budget: maintenance R&D (existing product) vs growth R&D (new products/markets)
  - S&M spend: treat CAC as capex-equivalent; evaluate payback period (CAC payback should be <24 months for efficient growth)
  - Cloud/hosting: increasingly opex but evaluate as capex (multi-year commitments = quasi-capex)
- No coffee machine test needed — the machine IS the software.

### Capital Allocation
- Growth-stage: almost all MFCF (if positive) flows into growth. Return capital only when growth opportunities are exhausted.
- Rule of 40 is the balancing test between growth investment and profitability.
- ZBB on S&M and R&D still applies — just because growth is the priority doesn't mean waste is acceptable.

### Deal Diligence
- Priority focus areas: cohort analysis (are early cohorts degrading?), NRR trend, logo churn vs expansion revenue, ARR bridge, billings quality.
- Capitalized dev costs: compare to total R&D spend — if >30% capitalized, scrutinize the policy.
- Professional services revenue mixed into SaaS metrics inflates multiples and distorts comparables. Separate and value independently.
- SBC: normalize by stripping SBC addback; "adjusted EBITDA" that adds back SBC on a 50%+ of EBITDA basis is not EBITDA.

### Value Creation
- Primary pillars: Open the Throttle → Polish the Trophy
- Key value creation levers: NRR improvement, CAC efficiency, enterprise market expansion, international GTM
- Multiple expansion story: path to Rule of 40+, NRR above 120%, enterprise contract mix

### Capital Structure
- Recurring revenue supports leverage. ARR-based lending increasingly available.
- Typical range: 3–6x ARR or 3–5x EBITDA (if profitable)
- Covenant light common (institutional TLB market)
- Be careful: SaaS churn can collapse revenue quickly; don't over-lever

### Red Flags Specific to SaaS
- Cohort LTV/CAC degrading across vintages
- Logo churn masked by expansion (NRR > 100% but logo churn > 15%)
- Revenue growth from professional services bundled into ARR
- Billings declining while revenue still growing (revenue is a lagging indicator)
- SBC > 20% of revenue treated as purely non-cash

---

## Manufacturing / Industrial

### Cashflow Quality
- Cyclicality makes "maintainable" hard: normalize MFCF across the full cycle, not just the last 12 months.
- Asset replacement cycles are long (10–25 years for heavy equipment): maintenance capex in any given year may be low, but cumulative needs to match asset base replacement cost.
- Watch for deferred maintenance: a company that has spent below-cycle maintenance capex for 3+ years has a cliff coming.

### Working Capital
- Inventory is the primary WC driver. Raw materials, WIP, and finished goods each have different dynamics.
- DIO benchmarks: 30–90 days depending on cycle time. Seasonal patterns massive.
- DSO benchmarks: 45–60 days typical for B2B manufacturing.
- Positive NWC is normal and expected. Red flag: WC improving rapidly in LTM — ask why.

### CapEx Evaluation
- This is the core domain for manufacturing — spend 50% of analysis time here.
- Maintenance vs growth split is the critical question. The coffee machine test is literally this sector.
- Deferred maintenance cliff: compare cumulative maintenance capex over 5 years to (asset base × estimated replacement rate). If there's a gap, a buyer will inherit the spend.
- Environmental capex: compliance-driven spend should be treated as maintenance even if it's technically new investment.

### Capital Allocation
- Mature industrials: conservative hierarchy. Fix balance sheet → maintain assets → disciplined growth → return capital.
- Growth capex requires thorough J-curve analysis and stage-gate structure.
- Build vs buy: organic capacity expansion often competes with acquisition; run the math on both.

### Deal Diligence
- Priority: asset condition assessment (physical site visit is non-negotiable), environmental DD, maintenance capex history vs D&A, union/labor contract timing.
- Normalized EBITDA: strip out any year where deferred maintenance boosted margins; adjust for the capex shortfall.
- Single-source supplier dependency: what % of COGS comes from one supplier? What's the consequence of loss?

### Value Creation
- Primary pillars: Squeezing the Lemon → Traveling Light → Stop the Bleed (if turnaround)
- Procurement savings and overhead rationalization are the fastest levers.
- Asset optimization: sale-leaseback of real estate, equipment financing to release capital.
- Operational excellence: lean manufacturing, yield improvement, energy efficiency.

### Capital Structure
- Asset-heavy = supports more secured debt. Equipment financing, real estate mortgage, ABL against inventory/AR.
- Sale-leaseback: release capital from owned assets without losing operational control.
- Cyclicality requires conservative leverage. Size for trough EBITDA, not peak.
- Typical range: 2–4x EBITDA (higher for infrastructure-like assets with contracted revenue).

### Red Flags Specific to Manufacturing
- Maintenance capex < 50% of D&A for 2+ consecutive years
- No formal asset condition assessment in the last 3 years
- Environmental site assessments (Phase I/II) not completed in DD
- Union contract expiring within 12 months of close
- 70%+ of revenue from one end market or customer

---

## Healthcare / Life Sciences

### Cashflow Quality
- Reimbursement rate changes can shift the cashflow profile overnight — normalize for known regulatory changes.
- Payer mix is critical: government payer reimbursement rates are lower and more volatile than commercial.
- Working capital is complex: insurance AR reimbursement cycles are long and uncertain.

### Working Capital
- DSO benchmarks: 45–90 days depending on payer mix (government pays slowest).
- DPO: limited optimization — regulatory relationships and supply criticality constrain stretching payables.
- Contractual adjustments and allowances are a major source of accounting judgment — scrutinize AR net of allowances.

### CapEx Evaluation
- Regulatory-driven capex (equipment certifications, compliance upgrades) is effectively maintenance even if it's technically new.
- Technology capex (EMR systems, imaging equipment): long replacement cycles; assess where the company is in those cycles.
- Reimbursement per procedure/visit/bed: the unit economics of capex decisions.

### Deal Diligence
- Priority: payer mix trend (shifting toward Medicaid/Medicare = cashflow headwind), regulatory inspection history, staffing cost inflation, compliance deficiencies.
- CMS reimbursement rate risk: model the cashflow impact of a 5% and 10% rate reduction.
- Compliance: any outstanding CMS findings, state license issues, or billing audits?

### Value Creation
- Primary pillars: Open the Throttle → Polish the Trophy (regulatory moat creates multiple expansion)
- Revenue per provider/bed/patient as the key unit economics metric.
- Bolt-on acquisitions are common (geographic density for referral networks).

### Capital Structure
- Predictable reimbursement contracts support moderate leverage.
- Government contracts can be pledged as collateral.
- Typical range: 2–4x EBITDA (lower if regulatory risk is high).

### Red Flags Specific to Healthcare
- Payer mix shifting toward government over 3-year trend
- Any CMS exclusion risk or compliance investigations
- Nursing/clinical staffing cost inflation not modeled into forward EBITDA
- Revenue recognition on contractual adjustments overstated

---

## Consumer / Retail

### Cashflow Quality
- Rent/lease obligations are quasi-debt (IFRS 16/ASC 842 makes this visible). EBITDAR (before rent) is not the same as free cashflow.
- Negative WC flywheel is the gold standard (Amazon, Costco model). Assess whether the business has it.
- Same-store vs new store contribution: new stores can mask same-store deterioration in aggregate revenue.

### Working Capital
- Negative NWC is a structural strength — supplier funding the growth flywheel.
- DPO benchmarks: 60–90 days for large retailers with pricing power.
- Inventory DIO: 30–60 days typical; seasonal spikes are normal but must be funded.
- Pre-season inventory buildup creates massive WC swings — assess liquidity through peak.

### CapEx Evaluation
- Store buildouts = growth capex. Unit economics per new store IS the capex decision.
- Same-store refurbishment = maintenance capex.
- E-commerce platform investment: growth capex with long payback; evaluate with stage-gate discipline.
- Apply coffee machine test: is that refurbishment maintaining customer traffic, or is it growth?

### Deal Diligence
- Priority: same-store sales trend (is aggregate growth hiding same-store decline?), inventory aging/markdown risk, franchise vs company-owned economics, channel shift to e-commerce.
- Customer acquisition costs: rising CAC signals brand erosion or channel saturation.
- Lease liabilities: full operating lease schedule; mark-to-market on renewals.

### Value Creation
- Primary pillars: Open the Throttle → Squeezing the Lemon → Polish the Trophy
- Brand strength → pricing power → margin expansion is the classic playbook.
- Dr Martens model: brand investment + DTC channel + geographic expansion = 12x EV in 8 years.
- Omnichannel as growth accelerator: integrated online/offline drives traffic and margin.

### Capital Structure
- Asset-light (leasehold), so leverage supported primarily by cashflow quality.
- Lease-adjusted leverage matters: include IFRS 16/ASC 842 debt in total leverage assessment.
- Seasonal WC swings require RCF headroom through peak inventory period.
- Typical range: 2–4x EBITDA (higher for brands with pricing power and negative WC flywheel).

### Red Flags Specific to Consumer/Retail
- Same-store sales negative for 2+ quarters while aggregate revenue grows
- Inventory aging: % of inventory >120 days old and markdown exposure
- DTC (direct-to-consumer) as % of revenue declining — losing pricing power
- Franchise mix increasing at expense of company-owned (lower margin, lower control)

---

## Business Services / Professional Services

### Cashflow Quality
- High cash conversion should be the norm. If MFCF conversion is below 70%, investigate — services businesses have low capex and should convert well.
- Utilization rates and bill rates drive everything. Revenue per employee is the key metric.
- WIP (Work in Progress) accounting: major area of judgment in project-based businesses. Aggressive WIP recognition inflates revenue and WC.

### Working Capital
- Receivables-heavy: cash collection is the #1 operational challenge.
- DSO benchmarks: 45–75 days for B2B services; longer for government clients.
- WIP: treat as quasi-receivables; apply the same scrutiny as AR aging.
- Advance billings / retainers: negative WC benefit where clients pay upfront.

### CapEx Evaluation
- Physical capex is minimal (<1–2% of revenue).
- Apply capex evaluation frameworks to: headcount expansion plans (treat as capex — build the business case), system/technology investment, training programs.
- The real "maintenance capex" is replacing key employees.

### Capital Allocation
- Buy-and-build is the classic PE playbook: fragmented market → roll-up → multiple expansion (Audax model).
- Headcount growth must be stage-gated: hire ahead of revenue (investment mode) vs after revenue (maintenance mode).

### Deal Diligence
- Priority: key person dependency (who leaves → how much revenue at risk?), client concentration (top 3 clients as % of revenue), utilization rate sustainability, non-compete enforceability in relevant jurisdiction.
- Contractor vs employee mix: misclassification risk, margin sustainability if contractors reclassified.
- Management team: is it "one person is the business"? Test by asking who clients call.

### Value Creation
- Primary pillars: Playing Lego → Squeezing the Lemon → Open the Throttle
- Roll-up economics: buy at 5–7x, build to 10x+ through scale and margin
- Shared services, offshore leverage, pricing power from market leadership.

### Capital Structure
- Asset-light; leverage supported purely by cashflow.
- Key person risk limits leverage — if the business walks out the door, there's no asset backing the debt.
- Typical range: 2–4x EBITDA; higher for platforms with recurring revenue or multi-year contracts.

### Red Flags Specific to Business Services
- Key person (1–2 individuals) generating >50% of revenue
- Top 3 clients representing >60% of revenue
- Utilization at historical peak at time of sale — not sustainable
- Non-compete agreements in states where enforcement is limited (California, etc.)
- WIP growing faster than revenue — revenue recognition too aggressive

---

## Infrastructure / Real Assets

### Cashflow Quality
- Contracted cashflows make MFCF highly predictable — use this as a strength in the analysis.
- Contract renewal risk is the key uncertainty: what % of contracted revenue renews in the next 3 years?
- Regulatory rate reset risk: for regulated assets, model the impact of regulatory reviews.
- Volume sensitivity: take-or-pay contracts minimize this; volume-exposed contracts don't.

### Working Capital
- Minimal traditional WC — value is in long-lived assets with contracted revenues.
- Focus on liquidity management: are maintenance reserves funded? Are capex reserves adequate?

### CapEx Evaluation
- Maintenance capex on existing assets IS the core business. Asset condition is everything.
- Growth capex = new assets / capacity expansion. Evaluate against contracted revenue.
- Asset condition assessment: independent engineering report is non-negotiable in DD.
- Capex reserves: are reserves being funded at a rate that will sustain the asset base?

### Capital Structure
- High leverage appropriate given cashflow predictability: 5–8x EBITDA typical.
- Project finance structures (ring-fenced, non-recourse): common for greenfield; each asset can be independently financed.
- Tax equity and government incentives: renewables, energy storage.
- Complex capital stacks with multiple tranches (senior secured, mezzanine, equity) are normal.
- Covenant light relative to mid-market PE: lenders comfortable with asset backing.

### Red Flags Specific to Infrastructure
- Deferred maintenance backlog not disclosed in asset condition assessment
- Contract maturity wall in years 3–5 with no renewal negotiation underway
- Regulatory review risk (rate-setting authority review upcoming)
- Counterparty credit quality deteriorating (who is the off-taker or contracted customer?)
- Environmental liability from historical operations

---

## Technology / Digital (Non-SaaS)

### Cashflow Quality
- Varies widely by sub-sector. Hardware = manufacturing. Marketplace/platform = may have negative WC.
- Cloud infrastructure costs often classified as opex but function like capex — multi-year cloud commitments are quasi-capex; apply envelope thinking.
- Network effects create durable moats; value the moat separately from current cashflow.

### Working Capital
- Hardware: inventory-heavy, looks like manufacturing.
- Marketplace/platform: typically negative WC (merchants funded by platform float).
- Two-sided marketplace: deferred payouts to one side create WC benefit; model this carefully.

### CapEx Evaluation
- Cloud/infrastructure spend: evaluate multi-year commitments as capex; assess ROI on cloud vs on-premise.
- R&D: separate maintenance (existing product) from growth (new platform capabilities).
- Data infrastructure and security: compliance-driven; treat as maintenance.

### Deal Diligence
- Customer concentration in marketplace businesses: take rate × GMV by top 5 merchants.
- Take rate compression: has the platform had to reduce take rates to retain merchants? Trend matters.
- Open source substitution risk: is there a free alternative emerging?
- Regulatory risk: antitrust (large platforms), data privacy (GDPR, CCPA), AI governance.

### Value Creation
- Network effects and data moats: quantify defensibility before applying growth investment.
- Primary pillars: Open the Throttle → Polish the Trophy
- Platform switching costs: measure as part of exit multiple thesis.

### Capital Structure
- Typically moderate leverage (2–4x EBITDA) unless infrastructure-like recurring revenues.
- High growth = preserve capital structure flexibility; don't over-lever early.

### Red Flags Specific to Technology/Digital
- Take rate declining without merchant/user retention improvement
- Network density declining in a geography (network effects are reversible)
- Regulatory action or antitrust investigation not disclosed in CIM
- Open source equivalent gaining adoption in the core use case

---

## Financial Services

### Cashflow Quality
- Traditional MFCF concepts don't apply well — the balance sheet IS the business.
- Focus on: net interest margin (NIM), fee income stability, credit loss normalization.
- "Maintainable" earnings must account for the credit cycle: normalize credit losses across the cycle, not just last year's benign period.

### Working Capital
- WC concepts don't apply. Focus on: liquidity (LCR/NSFR ratios), capital adequacy (Tier 1/CET1), asset quality (NPL ratio, provision coverage).

### CapEx Evaluation
- Low physical capex. Main "capex" categories: technology investment (core banking modernization) and regulatory compliance programs.
- Technology transformation projects are high-risk, high-cost — apply stage-gate discipline.

### Capital Structure
- Regulatory capital requirements (Tier 1, CET1, leverage ratio) constrain everything.
- Traditional PE leverage doesn't apply — structure through holding company above the regulated entity.
- Regulatory relationships matter as much as financial metrics.
- Stress test results are the real capital adequacy measure.

### Deal Diligence
- Priority: asset quality (NPL ratio trend, provision adequacy), regulatory examination findings, compliance function maturity, model risk (are loan loss reserves adequate?).
- Credit concentration: geographic, sector, or single-name concentration creates binary risk.
- Pending regulatory examinations or enforcement actions: must be disclosed and assessed.

### Value Creation
- Primary pillars: Traveling Light (efficiency ratio improvement) → Polish the Trophy (regulatory moat)
- Cost efficiency ratio is the operating metric: non-interest expense ÷ revenue.
- M&A: regulatory approval adds 12–24 months to close timeline; build into LBO hold period.

### Red Flags Specific to Financial Services
- NPL ratio trending up while provisioning is flat or declining
- Regulatory examination findings not disclosed or minimized
- Significant model risk (loan loss model not independently validated)
- Credit concentration: >20% exposure to single sector
- Tier 1 ratio near regulatory minimum with no credible capital raise plan
