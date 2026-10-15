# 觀察名單分析 (按產業) — 2026-05-23

Quant pass across the 11 tracked sector baskets (52 names) using the 8-dimension
`stock-analysis` scorer. Confidence is a **starting-point signal**, not the thesis —
see the philosophy note at the bottom. Sorted within each sector; ★ marks the
basket's strongest read.

> Run note: `analyze.sh all` ran clean (no rate-limiting). `MACOM` is delisted as a Yahoo symbol — re-run as **MTSI**.

---

## 🏆 全名單前段班 (Conf ≥ 38%, the only actionable-BUY tier)

| Ticker | 產業 | Conf | 一句話 |
|--------|------|------|--------|
| **META** | bigtech | 47% BUY | +56.8% EPS surprise, +40.6% margins, 16.9x fwd P/E, +35.5% PT gap / 58 analysts — best risk/reward on the board |
| **GOOGL** | bigtech | 44% BUY | +91.4% EPS surprise, 3/4 beats, 26.5x fwd — clean compounding |
| **MCHP** | defsemi | 44% BUY | analog/MCU cycle turning, +35% rev, +21% PT gap / 25 analysts |
| **6669.TW 緯穎** | tw | 42% BUY | AI server ODM, +62% rev, 12.2x fwd — cheapest high-grower in TW set |
| **2408.TW 南亞科** | ram | 40% BUY | DRAM upcycle, +583% rev, +61% margins, 5.8x fwd |
| **WDC** | ram | 40% BUY | +283% EPS surprise, NAND/HDD storage cycle, 27.8x fwd |
| **CRM** | saas | 39% BUY | +25% EPS surprise, 12.0x fwd (cheapest large SaaS), +45.7% PT gap |

---

## 🧠 Big Tech (bigtech)

| Ticker | Conf | EPS surp | Rev | Fwd P/E | PT gap |
|--------|------|----------|-----|---------|--------|
| META ★ | 47% BUY | +56.8% | +33.1% | 16.9x | +35.5% (58) |
| GOOGL | 44% BUY | +91.4% | +21.8% | 26.5x | +12.0% (53) |
| NVDA | 30% BUY | +5.6% | +85.2% | 17.0x | +36.6% (58) |
| MSFT | 29% BUY | +5.2% | +18.3% | 21.6x | +33.9% (54) |
| AMD | 31% HOLD | +6.2% | +37.8% | 36.1x | +1.0% (48) |
| AAPL | 9% HOLD | +3.6% | +16.6% | 32.2x | −0.1% (43) |

**Read:** META/GOOGL lead on margin expansion + cheap multiples. NVDA/MSFT score lower only because the small EPS *surprise* (already-high bar) caps the earnings dimension — both still BUY with huge PT gaps and are core holds, not avoids. **AAPL is the clear laggard** — flat growth, zero PT upside, richest multiple of the cohort.

## 💾 Memory / DRAM (ram)

| Ticker | Conf | EPS surp | Rev | Fwd P/E | PT gap |
|--------|------|----------|-----|---------|--------|
| 2408.TW 南亞科 ★ | 40% BUY | +16.6% | +582.9% | 5.8x | +3.4% (11) |
| WDC | 40% BUY | +283.2% | +45.5% | 27.8x | +4.8% (23) |
| MU | 37% BUY | +33.2% | +196.3% | 7.3x | −18.3% (40) |
| 2344.TW 華邦電 | 34% BUY | +5.3% | +91.3% | 5.5x | +16.8% (6) |

**Read:** The standout theme of the whole watchlist — every name in BUY, explosive rev growth, single-digit multiples on the TW names. The memory upcycle is in full swing. Caveat: MU's −18% PT gap says the sell-side thinks the move is largely priced; 2408/2344 still show upside. These are cyclicals — ride the cycle, don't marry them.

## 🇹🇼 Taiwan core (tw)

| Ticker | Conf | EPS surp | Rev | Fwd P/E | PT gap |
|--------|------|----------|-----|---------|--------|
| 6669.TW 緯穎 ★ | 42% BUY | +14.3% | +62.0% | 12.2x | +20.9% (17) |
| 3711.TW 日月光 | 37% BUY | +13.2% | +17.2% | 24.1x | −4.4% (17) |
| 2382.TW 廣達 | 31% HOLD | +8.7% | +66.6% | 11.2x | +22.6% (19) |
| 2330.TW 台積電 | 28% BUY | +5.3% | +35.1% | 18.4x | +14.8% (33) |
| 2317.TW 鴻海 | 21% HOLD | +0.8% | +28.9% | 11.7x | +25.1% (18) |
| 2303.TW 聯電 | 16% HOLD | +50.0% | +5.5% | 22.1x | −31.1% (22) |
| 2379.TW 瑞昱 | 16% HOLD | −0.1% | +4.0% | 15.9x | +1.6% (16) |

**Read:** AI-server supply chain (緯穎, 廣達, 鴻海) carries the basket on revenue, but only 緯穎 combines the beat + PT gap to score top-tier. TSMC scores modestly (small surprise vs its own high bar) yet remains the anchor with +14.8% PT upside / 33 analysts. 聯電 flagged weakest — −31% PT gap signals overvaluation vs foundry peers.

## 🔲 ABF substrate / server (abf)

| Ticker | Conf | EPS surp | Rev | Fwd P/E | PT gap |
|--------|------|----------|-----|---------|--------|
| 3037.TW 欣興 ★ | 34% BUY | +50.0% | +24.5% | 33.3x | −4.0% (17) |
| SMCI | 29% BUY | +35.5% | +122.7% | 11.1x | +4.3% (16) |
| 8046.TW 南電 | 29% HOLD | +5.2% | +41.9% | 33.5x | −4.6% (11) |
| 3044.TW 健鼎 | 8% HOLD | −1.1% | +22.4% | 14.1x | +24.4% (6) |

**Read:** Substrate names (欣興/南電) riding the AI-server PCB build-out but rich multiples + negative PT gaps temper them. SMCI screens cheap (11x) with strong growth but the thin score reflects its volatile beat history (2/4) and recurring governance overhang — handle as high-beta, not a core hold.

## ⚙️ AI Infra — networking/server/power (aiinfra)

| Ticker | Conf | EPS surp | Rev | Fwd P/E | PT gap |
|--------|------|----------|-----|---------|--------|
| VRT ★ | 34% BUY | +15.8% | +30.1% | 37.1x | +12.9% (25) |
| ANET | 30% BUY | +7.4% | +35.1% | 34.6x | +22.2% (27) |
| DELL | 32% HOLD | +10.8% | +39.5% | 19.8x | −28.1% (23) |

**Read:** VRT (power/cooling) + ANET (networking) are the cleaner AI-infra plays — both BUY, both with positive PT gaps. DELL grows fastest but the −28% PT gap says the AI-server revenue is dilutive/low-margin and the stock has run ahead of targets.

## ☁️ SaaS / Security (saas)

| Ticker | Conf | EPS surp | Rev | Fwd P/E | PT gap |
|--------|------|----------|-----|---------|--------|
| CRM ★ | 39% BUY | +24.9% | +12.1% | 12.0x | +45.7% (53) |
| PLTR | 35% BUY | +17.9% | +84.7% | 66.0x | +34.2% (27) |
| SNOW | 31% BUY | +18.5% | +30.1% | 71.0x | +33.4% (48) |
| OKTA | 30% HOLD | +5.9% | +11.6% | 21.8x | +9.5% (43) |
| DDOG | 25% HOLD | +17.6% | +32.2% | 78.2x | +0.3% (47) |
| PANW | 25% HOLD | +9.6% | +14.9% | 65.5x | −13.8% (49) |
| NET | 23% HOLD | +8.7% | +33.5% | 141.7x | +8.3% (31) |
| NOW | 17% HOLD | +0.0% | +22.1% | 20.3x | +39.8% (44) |
| CRWD | 11% HOLD | +1.8% | +23.3% | 107.7x | −19.3% (51) |

**Read:** Huge multiple dispersion. **CRM is the value anomaly** — 12x fwd with the biggest PT gap (+45.7%) in the entire watchlist; the market treats it as ex-growth while it still beats. PLTR/SNOW score well on momentum + PT gap but pay 66–71x. The expensive-and-stalling cohort (CRWD 107x / −19% gap, NET 141x) screens worst. NOW's +39.8% PT gap is interesting against a flat surprise — a name to watch for a re-rate.

## ☢️ Nuclear / Power (nuclear)

| Ticker | Conf | EPS surp | Rev | Fwd P/E | PT gap |
|--------|------|----------|-----|---------|--------|
| VST ★ | 34% BUY | +53.5% | +43.4% | 14.3x | +44.2% (17) |
| CEG | 30% HOLD | +5.4% | +63.8% | 21.6x | +24.4% (20) |
| FSLR | 27% HOLD | +8.4% | +23.6% | 11.0x | −5.5% (27) |
| SMR | 11% HOLD | −16.7% | −95.8% | — | +34.7% (14) |
| OKLO | 7% HOLD | −68.8% | — | — | +34.7% (19) |

**Read:** **VST is the only investable-grade name here** — real earnings (+53% surprise), 14x, +44% PT gap. CEG is the steadier utility play. The SMR/OKLO small-modular-reactor story is pure narrative — negative/no revenue, −10181% "margin" on SMR is noise from a near-zero base. Big PT gaps reflect analyst hope, not fundamentals. Trade these on momentum only (see QM scan), don't buy-and-hold on quant.

## 🛰️ LEO / Space (leo)

| Ticker | Conf | EPS surp | Rev | Fwd P/E | PT gap |
|--------|------|----------|-----|---------|--------|
| RKLB ★ | 20% HOLD | +12.5% | +63.5% | — | −25.7% (15) |
| LUNR | 19% HOLD | +16.7% | +198.7% | — | −0.7% (9) |
| PL | 14% HOLD | +40.0% | +41.1% | — | −20.0% (10) |
| ASTS | 37% SELL | −230.0% | +1952.2% | — | −21.2% (9) |

**Read:** Pre-profit, no usable P/E across the board. **ASTS scores 37% but the signal is SELL** — −1014% margins and −230% EPS; the +1952% revenue is off a tiny base and the cash burn dominates. RKLB is the operational leader but already past analyst targets (−25.7% gap). This is a venture-style basket — momentum/thesis names, not quant buys. (LUNR also surfaced as a QM breakout candidate today — see the QM scan.)

## 🛡️ Defense primes (defense)

| Ticker | Conf | EPS surp | Rev | Fwd P/E | PT gap |
|--------|------|----------|-----|---------|--------|
| GD ★ | 28% BUY | +11.1% | +10.3% | 18.9x | +14.2% (21) |
| RTX | 28% BUY | +17.1% | +8.7% | 23.4x | +21.6% (22) |
| NOC | 27% HOLD | +1.3% | +4.4% | 18.4x | +27.0% (21) |
| LMT | 14% HOLD | −3.7% | +0.3% | 16.6x | +17.5% (19) |

**Read:** Steady, low-beta basket — modest single-digit growth, reasonable multiples, decent PT gaps. GD/RTX edge ahead on the beats. LMT lags (EPS miss, flat revenue). These are ballast/defensive holds; none is a high-conviction quant BUY but all carry positive analyst upside.

## 🔬 Defense semis (defsemi)

| Ticker | Conf | EPS surp | Rev | Fwd P/E | PT gap |
|--------|------|----------|-----|---------|--------|
| MCHP ★ | 44% BUY | +14.0% | +35.1% | 22.8x | +21.2% (25) |
| MTSI | 20% HOLD | +1.9% | +22.5% | 56.4x | +1.8% (14) |
| AXTI | 18% HOLD | +80.0% | +39.1% | 187.3x | −37.7% (4) |

**Read:** **MCHP is the surprise top-3 name of the entire watchlist** — the analog/MCU inventory cycle is turning, +35% rev, +21% PT gap / 25 analysts at a reasonable 22.8x. MTSI (RF/microwave) is solid but pricey. AXTI (gallium-arsenide materials) shows a big EPS beat off a depressed base but 187x fwd and −38% PT gap flag it as un-investable on fundamentals.

---

## 🔭 跨產業重點 (cross-sector takeaways)

1. **Memory/DRAM is the cleanest theme** — 2408.TW, WDC, MU, 2344.TW all BUY with explosive growth and (on the TW names) single-digit multiples. Cyclical, so position-trade it.
2. **Value anomalies worth a deep dive:** CRM (12x, +46% PT gap), MCHP (cycle turn), META (16.9x for that margin profile).
3. **Avoid the narrative baskets on quant:** SMR/OKLO (nuclear SMR) and ASTS/PL (space) are pre-revenue stories — only touch via the momentum lens, never as buy-and-hold.
4. **Laggards to trim/avoid:** AAPL (9%, no upside), 聯電 2303.TW (−31% PT gap), DELL (−28%), CRWD (107x / −19%).
5. **AI-server supply chain** (緯穎, 廣達, VRT, ANET) remains broadly constructive but increasingly priced — selectivity matters; 緯穎 is the standout.

## ⚠️ 方法論 / 限制

- Confidence score is the **quant starting point only**. Per workspace philosophy, durable buy-and-hold calls require industry analysis, analyst bull/bear reasoning, earnings-call guidance, and management track record — none captured here. Treat ≥38% as "earns a deep dive," not "buy."
- yfinance data lags 15–20 min; short interest ~2 weeks stale.
- A small EPS *surprise* penalizes mega-caps (NVDA/MSFT/TSMC) whose beats are already expected — don't read their mid-pack scores as bearish.
- Not investment advice.
