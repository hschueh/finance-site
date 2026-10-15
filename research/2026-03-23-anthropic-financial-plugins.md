# Anthropic Claude for Financial Services Plugins

**Date:** 2026-03-23
**Source:** https://www.blocktempo.com/anthropic-claude-financial-services-plugins-41-skills-11-data-providers/
**Repo:** https://github.com/anthropics/financial-services-plugins (Apache 2.0, ~6.5k stars, 745 forks)

---

## Overview

Anthropic open-sourced a plugin framework that turns Claude Code into a financial domain tool. No coding required — slash commands drive entire workflows (DCF modeling, IC memos, earnings updates).

---

## Architecture

### Core Plugin (required first)
- `financial-analysis` — shared base with DCF, Comps (comparable company analysis), LBO models + 11 MCP data connectors

### Add-on Plugins
| Plugin | Key workflows |
|---|---|
| `investment-banking` | CIM drafting, buyer lists, merger models, deal tracking |
| `equity-research` | Post-earnings updates, research reports, catalyst tracking, morning note summaries |
| `private-equity` | Deal sourcing automation, due diligence, IC memos, KPI tracking |
| `wealth-management` | Client meeting prep, financial planning, portfolio rebalancing, tax-loss harvesting |

### Partner Plugins
- **LSEG** — bond pricing, yield curves, FX, options valuation
- **S&P Global** — company tearsheets, earnings previews

---

## Data Sources (11 MCP connectors)

Daloopa, Morningstar, FactSet, Moody's, PitchBook, LSEG, S&P Global, MT Newswires, Aiera, Chronograph, Egnyte

> Note from article author: ~80% functionality available without paid subscriptions. Only edge cases need live premium data.

---

## Key Stats

- **41 skills** — auto-triggered, no user invocation needed
- **38 slash commands** — user-initiated
- **11 data sources**

## Useful Commands

```
/comps [company]           — comparable company analysis
/dcf [company]             — DCF valuation model
/earnings [company] [Q]    — post-earnings update report
/ic-memo [project]         — investment committee memo
/source [criteria]         — deal sourcing automation
/client-review [client]    — client meeting prep
```

---

## Installation (Claude Code CLI)

```bash
# Add marketplace
claude plugin marketplace add anthropics/financial-services-plugins

# Core (required)
claude plugin install financial-analysis@financial-services-plugins

# Add-ons (pick as needed)
claude plugin install equity-research@financial-services-plugins
claude plugin install investment-banking@financial-services-plugins
claude plugin install private-equity@financial-services-plugins
claude plugin install wealth-management@financial-services-plugins
```

---

## Notes

- Released same week as Claude Code Channels (Telegram/Discord integration)
- Signals Anthropic pushing Claude Code from dev tool → vertical industry solution
- Worth testing equity-research plugin for TW/US stock workflow — especially `/earnings` for post-earnings call summaries and analyst debate framing

---

## Existing Workflow Evaluation

### Current pipeline
```
analyze.sh → /tmp/batch_<sector>.json   # Yahoo Finance quant data
parse_results.py → table view           # SIGNAL, CONF, EPS%, BEATS, REV%, MARGIN, FWD_PE, ANALYST
research/*.md → inject_reports.py → index.html → build_site.sh → here-now URL
```

### What the existing scripts already cover (no plugin needed)
- Quantitative screening: EPS surprise %, revenue growth, operating margin, fwd P/E, analyst upside
- Beat/miss track record (last 4Q)
- Sector batch runs with confidence scores and BUY/HOLD/SELL signals
- Auto-publish to static site via here-now

### What the Anthropic plugins add (genuinely new)
- **Earnings call narrative** — management tone, guidance raise/maintain/cut, sandbagging detection
- **Analyst debate framing** — bull vs bear case, key debate (not just consensus rating count)
- **Sector/competitive analysis** — moat, market position, tailwinds/headwinds
- **Formatted research reports** — structured `.md` output matching your CLAUDE.md analysis philosophy

### Overlap assessment
**Minimal overlap.** Existing scripts = quantitative screener. Plugins = qualitative narrative layer. They're complementary.

### Integration fit
Plugin output (e.g. `/earnings NVDA Q4`) is markdown text → save as `research/YYYY-MM-DD-earnings-nvda.md` → `inject_reports.py` picks it up automatically → `build_site.sh` publishes. **Zero pipeline changes needed.**

---

## TODO / Next Session Plan

### Step 1 — Install the plugins
```bash
cd ~/misc/finance-research
claude plugin marketplace add anthropics/financial-services-plugins
claude plugin install financial-analysis@financial-services-plugins
claude plugin install equity-research@financial-services-plugins
```

### Step 2 — Test on a stock from the existing watchlist
Pick one from `analyze.sh` (e.g. NVDA, 2330.TW) — run quant first, then qualitative:
```bash
bash scripts/analyze.sh bigtech        # existing quant
python3 scripts/parse_results.py /tmp/batch_bigtech.json
```
Then in Claude Code:
```
/earnings NVDA Q4 2025
/comps NVDA
```
Compare: does the qualitative output add to what parse_results already shows?

### Step 3 — Save output in the right format
Pipe `/earnings` output into a dated `.md` file in `research/`:
```
research/2026-03-23-earnings-nvda-q4.md
```
Run `python3 scripts/inject_reports.py` — should pick it up automatically alongside existing reports.

### Step 4 — Build & verify site
```bash
bash scripts/build_site.sh
```
Check that the new report appears in the published site correctly.

### Step 5 — Evaluate free tier gap
Note any data that's stale or missing (estimates, guidance numbers). Decide if Morningstar or Daloopa connector is worth adding.

### Step 6 — Optional: automate the quant+qual combo
Could add a wrapper that: runs analyze.sh for a sector → generates `/earnings` reports for top BUY signals → saves all as `.md` → rebuilds site in one shot.
