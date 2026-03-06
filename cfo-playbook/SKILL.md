---
name: cfo-playbook
description: Apply a seasoned CFO's analytical lens to any PE investment document, deal, or portfolio company. This is the master router for all CFO playbook skills. Proactively triggers when Jake is doing ANY PE investment work — reviewing a CIM, evaluating a deal, analyzing a portfolio company, reviewing financial documents, or thinking through a capital decision. Triggers on: "/cfo-lens", "apply the CFO lens", "CFO analysis", "what would a CFO think of this", "give me the full CFO view", "analyze this deal", "review these financials", "what are the red flags", "evaluate this company", or when any financial document is shared in a PE/investment context. Supports /cfo-lens --industry=[sector] to pre-load industry context. Also triggers as a complement to any existing PE skill: dd-checklist, ic-memo, returns-analysis, value-creation-plan, deal-screening.
---

# CFO Playbook — Master Router

This skill routes incoming analysis to the right CFO framework sub-skills and coordinates a comprehensive evaluation when requested. It always starts with industry identification.

---

## Step 1: Always Identify Industry First

Before routing to any sub-skill, identify the sector:

```
Sectors: SaaS/Software | Manufacturing/Industrial | Healthcare/Life Sciences |
         Consumer/Retail | Business Services | Infrastructure/Real Assets |
         Technology/Digital | Financial Services | Other (specify)
```

- Ask Jake if unclear, or infer from the document (product/service description, revenue model, asset base)
- Load the relevant section from [references/industry-contexts.md](references/industry-contexts.md)
- This changes thresholds, benchmarks, red flags, and analytical emphasis for every sub-skill

---

## Step 2: Detect Context and Route

### Document-Based Routing

| Document Provided | Primary Skills to Invoke |
|---|---|
| CIM / Information Memorandum | deal-diligence → cashflow-quality → working-capital → common-pitfalls |
| QoE report | deal-diligence (deep) → working-capital |
| Financial model / LBO | cashflow-quality → capex-evaluation → capital-structure |
| Management accounts / board pack | cashflow-quality → value-creation (if portco) |
| AR/AP aging schedule | working-capital (deep) |
| Capex schedule / investment proposal | capex-evaluation (deep) → capital-allocation |
| Value creation plan | value-creation (deep) → capital-allocation |
| Capital structure / term sheet | capital-structure (deep) → deal-structuring |
| Deal summary / LOI / term sheet | deal-structuring → deal-diligence |

### Intent-Based Routing

| Jake's Intent | Primary Skills to Invoke |
|---|---|
| "Is this a good deal?" | deal-diligence → common-pitfalls → cashflow-quality |
| "How should we structure this?" | deal-structuring → capital-structure |
| "How is this portco performing?" | cashflow-quality → value-creation |
| "Where is value being created/destroyed?" | value-creation → capital-allocation → capex-evaluation |
| "What are the red flags?" | common-pitfalls → deal-diligence |
| "Is the capital structure right?" | capital-structure |
| "Evaluate the WC situation" | working-capital |
| "Is the capex justified?" | capex-evaluation |

---

## Step 3: /cfo-lens — Full Comprehensive Evaluation

When Jake runs `/cfo-lens` (or asks for a full CFO view), run all relevant skills in sequence:

```
/cfo-lens [document or deal description]
/cfo-lens --industry=[sector] [document or deal description]
```

**Full evaluation sequence:**

1. **Industry identification** → load industry-contexts.md
2. **Cashflow quality** → is the EBITDA real? What's the MFCF?
3. **Working capital** → structural strength or drain? Peg implications?
4. **CapEx evaluation** → maintenance vs growth split, quality of projects
5. **Capital allocation** → how is management deploying cash? Strategy alignment?
6. **Deal diligence** → QoE, adjustment lines, hidden debt (if deal context)
7. **Deal structuring** → price vs terms, seller note, WC peg (if transaction context)
8. **Value creation** → 7 pillars score, exit readiness (if portco context)
9. **Capital structure** → leverage appropriateness, covenant headroom, flexibility
10. **Common pitfalls** → cross-cutting red flags, behavioral biases

**Output format for /cfo-lens:**

```
## CFO Lens: [Company/Deal Name] — [Industry]

### Industry Context
[Key industry-specific calibrations loaded]

### Cashflow Quality
What we like | What we don't like | Red flags | Opportunity

### Working Capital
[...]

### CapEx Quality
[...]

### Capital Allocation
[...]

### Deal Diligence [if applicable]
[...]

### Deal Structuring [if applicable]
[...]

### Value Creation Assessment [if portco]
[...]

### Capital Structure
[...]

### Cross-Cutting Red Flags
[Synthesis from common-pitfalls]

### Overall Assessment
[Concise CFO verdict: what this business/deal looks like through the CFO lens]
```

---

## Step 4: Integration with Existing PE Skills

The CFO playbook enhances (not replaces) the existing PE skills:

| Existing Skill | CFO Playbook Enhancement |
|---|---|
| [dd-checklist](../../private-equity/skills/dd-checklist/SKILL.md) | deal-diligence adds the CFO analytical judgment on top of the process tracker |
| [ic-memo](../../private-equity/skills/ic-memo/SKILL.md) | deal-diligence + common-pitfalls feeds the risk section; cashflow-quality validates the EBITDA basis |
| [returns-analysis](../../private-equity/skills/returns-analysis/SKILL.md) | capital-structure informs the leverage assumptions; value-creation contextualizes the return drivers |
| [value-creation-plan](../../private-equity/skills/value-creation-plan/SKILL.md) | value-creation scores the plan against 7 pillars and identifies missing levers |
| [deal-screening](../../private-equity/skills/deal-screening/SKILL.md) | common-pitfalls overlays industry-specific risk assessment |
| [lbo-model](../../financial-analysis/skills/lbo-model/SKILL.md) | capital-structure validates the debt assumptions; cashflow-quality validates EBITDA inputs |

---

## Reference Files

- [references/industry-contexts.md](references/industry-contexts.md) — Industry-specific calibrations for all 8 sectors
- [references/frameworks.md](references/frameworks.md) — Decision frameworks (MFCF, coffee machine test, capital allocation hierarchy, 7 pillars, etc.)
- [references/metrics-glossary.md](references/metrics-glossary.md) — MFCF, CFADS, CROI, CAG, CTG, WC peg, and all key metrics defined
- [references/checklist-templates.md](references/checklist-templates.md) — Red flag checklists by domain, for final sweeps

---

## Sub-Skills

- [skills/cashflow-quality/SKILL.md](skills/cashflow-quality/SKILL.md)
- [skills/working-capital/SKILL.md](skills/working-capital/SKILL.md)
- [skills/capex-evaluation/SKILL.md](skills/capex-evaluation/SKILL.md)
- [skills/capital-allocation/SKILL.md](skills/capital-allocation/SKILL.md)
- [skills/deal-diligence/SKILL.md](skills/deal-diligence/SKILL.md)
- [skills/deal-structuring/SKILL.md](skills/deal-structuring/SKILL.md)
- [skills/value-creation/SKILL.md](skills/value-creation/SKILL.md)
- [skills/capital-structure/SKILL.md](skills/capital-structure/SKILL.md)
- [skills/common-pitfalls/SKILL.md](skills/common-pitfalls/SKILL.md)
