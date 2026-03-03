# jake-financial-plugins

Private financial services plugins for Claude Code. Forked from [anthropics/financial-services-plugins](https://github.com/anthropics/financial-services-plugins) and customized for personal use.

## Plugins

### financial-analysis
Core financial modeling tools available in any Claude Code session.

| Command | Description |
|---------|-------------|
| `/dcf` | Full DCF valuation — projections, WACC, terminal value, sensitivity tables |
| `/comps` | Comparable company analysis → Excel with multiples |
| `/lbo` | LBO model for PE acquisition analysis |
| `/3-statements` | 3-statement financial model (IS, BS, CF) |
| `/competitive-analysis` | Competitive landscape analysis |
| `/check-deck` | QC a PowerPoint deck for errors and consistency |
| `/debug-model` | Audit spreadsheet for broken formulas, circular refs, hardcodes |
| `/ppt-template` | Build reusable PPT template skill from a .pptx file |

### private-equity
Deal workflow tools for PE professionals.

| Command | Description |
|---------|-------------|
| `/source` | Deal sourcing — company discovery and outreach |
| `/screen-deal` | Quick deal screen against investment criteria |
| `/dd-prep` | Due diligence meeting prep |
| `/dd-checklist` | Full DD checklist for a target company |
| `/ic-memo` | Investment committee memo |
| `/returns` | Returns analysis (IRR, MOIC scenarios) |
| `/unit-economics` | Unit economics breakdown |
| `/value-creation` | Value creation plan |
| `/portfolio` | Portfolio company monitoring |

### equity-research
Research workflows for coverage initiation and ongoing analysis.

| Command | Description |
|---------|-------------|
| `/initiate` | Initiate coverage report |
| `/earnings` | Earnings analysis |
| `/earnings-preview` | Earnings preview ahead of reporting |
| `/morning-note` | Morning note / quick take |
| `/thesis` | Investment thesis tracker |
| `/model-update` | Financial model update |
| `/catalysts` | Catalyst calendar |
| `/screen` | Stock screen |
| `/sector` | Sector overview |

---

## Installation

```bash
# Clone this repo
git clone https://github.com/[your-username]/jake-financial-plugins.git ~/jake-financial-plugins
cd ~/jake-financial-plugins

# Install all 3 plugins globally into Claude Code
claude plugin install ./financial-analysis
claude plugin install ./private-equity
claude plugin install ./equity-research

# Verify
claude plugin list
```

Plugins are installed globally — available in all Claude Code sessions and projects.

---

## MCP Data Providers

Commands work without live data (Claude uses its training knowledge for analysis). When you add subscriptions, update the `.mcp.json` in each plugin directory:

| Provider | Plugin | Data |
|----------|--------|------|
| PitchBook | private-equity, financial-analysis | PE/VC deals, company profiles |
| Chronograph | private-equity | PE portfolio management |
| FactSet | financial-analysis | Financial data and analytics |
| S&P Global / Capital IQ | financial-analysis | Company financials, M&A data |
| Aiera | financial-analysis | Earnings transcripts |
| Morningstar | financial-analysis | Fund and equity research |
| Daloopa | financial-analysis | Automated filing data extraction |

See `_note` fields in each `.mcp.json` for setup guidance.

---

## Customization

Skills are plain markdown — edit `skills/*/SKILL.md` in any plugin to tune prompts for your specific workflow. Changes take effect immediately on next Claude Code session.
