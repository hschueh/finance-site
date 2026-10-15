# Qullamaggie Backtest MVP — S&P 500 + 台灣50（3年）

**Date:** 2026-05-16
**Backtest window:** 2023-05-17 → 2026-05-15 (752 bars)
**Universes:** S&P 500 (503 檔), Taiwan 50 (50 檔)
**Framework:** VectorBT 1.0.0 + yfinance OHLCV cache
**Code:** `scripts/qm/backtest/{data,signals,portfolio,run}.py`

---

## TL;DR

| Setup × Universe | Trades | Win % | 總報酬 | Sharpe | Max DD | Profit Factor |
|---|--:|--:|--:|--:|--:|--:|
| **EP × S&P 500** | **825** | **42.7%** | **+58.9%** | **1.72** | **-9.3%** | **1.61** |
| Breakout × S&P 500 | 18 | 33.3% | -1.2% | -0.09 | -7.5% | 0.82 |
| EP × Taiwan 50 | 55 | 43.6% | +15.0% | 0.96 | -5.1% | 2.08 |
| Breakout × Taiwan 50 | 3 | 33.3% | -2.2% | -0.72 | -3.5% | 0.07 |
| **Buy-and-hold SPY** (ref) | — | — | +85.0% | 1.44 | -18.8% | — |
| **Buy-and-hold 0050.TW** (ref) | — | — | +242.0% | 1.93 | -27.5% | — |

**單一最強發現：EP setup 在 S&P 500 大型股的風險調整後報酬贏過 buy-and-hold (Sharpe 1.72 vs 1.44)，且最大回撤只有 SPY 的一半 (-9.3% vs -18.8%)。** 雖然絕對報酬輸 (58.9% vs 85%)，但策略平均只佈署 ~10-30% 資金，per-deployed-capital 看其實顯著超越。

**Breakout setup 在大型股不可行：** 訊號太稀疏 (3年只有 18 / 3 筆)，且沒有 edge。原因下面說。

---

## 方法

### 策略
1. **Breakout** — 前期漲幅 ≥20% + 緊縮整理 (20 日 range ≤ 3× ADR) + 收盤突破 20 日高
2. **Episodic Pivot (EP)** — 開盤跳空 ≥5%、量 ≥2× 50日均量、前 60 日漲幅 ≤30%（平台底）

### 出場
- 停損 -7%（≈ 1.5× ADR）
- 時間停損 30 個交易日
- 動態停利：收盤跌破 20 日均線

### 部位
- 起始資金 $100k
- 每訊號 10% 資金（cap-based equal weight）
- 最多同時 10 個部位
- 手續費 + 滑價各 10 bps

### 訊號生成（vectorized, no look-ahead）
所有條件用 `shift(1)` 確保 T 日訊號只用 ≤ T-1 日資料。Cross-sectional RS rank 用當天截面排名，避免 backfill bias。

### Profile：`bigcap`
原始 QM 門檻針對小中型股 (ADR ≥ 4%, prior runup ≥ 30%)。S&P 500 大型股 ADR 中位數只有 2.5%，所以 `bigcap` profile 放寬到：
- `min_adr_pct = 2.0`
- `max_base_range_mult = 3.0`
- `min_prior_runup = 0.20`
- `ep_min_gap_pct = 0.05`

---

## 結果解讀

### ✅ EP × S&P 500 是真正的 alpha 候選

825 筆交易在 3 年是相當有統計意義的樣本。Sharpe 1.72、profit factor 1.61、win rate 42.7% (avg winner +9.7% / avg loser -4.6%，賠率 ~2:1)。最大回撤 -9.3% 在 2022-23 升息環境裡很乾淨。

關鍵：策略不是常時 fully invested 的，所以 58.9% vs SPY 85% 的比較不公平。更貼切的指標是 Sharpe，1.72 vs 1.44 → 風險調整後贏。

### ❌ Breakout × 大型股不可行

3 年 SP500 只有 18 個 breakout 訊號，TW50 只有 3 個。原因：
1. **大型股不夠緊縮** — 大型股波動天然較低，但 20 日整理區間相對 ADR 反而較寬（流動性帶來持續成交）。緊縮型態本來就是小中型股的專利。
2. **前期漲幅不足** — 大型股 60 日內漲 20% 已經少見，這個門檻濾掉絕大多數。
3. **Sample size 太小無法下結論** — 18 筆只能看出「策略沒打到」，不能判定「策略不好」。

→ Breakout 應該用小中型股 universe 跑，不該用 S&P 500/TW50。

### ❌ TW50 EP 樣本邊緣

55 筆在 3 年偏少，但 profit factor 2.08 / Sharpe 0.96 顯示有一點 edge。考慮台股漲跌停 ±10% 截斷 EP 訊號（很多應該觸發的跳空被截到 +9.9% 漲停），實際 edge 可能被低估。

### Buy-and-hold 在這 3 年贏太多

2023-05 → 2026-05 是 AI 與半導體狂熱期，SPY +85%、0050.TW +242%（大部分由 TSMC 貢獻）。任何 long-only 擇時策略都很難贏 fully-invested B&H。Sharpe 才是公平的比較。

---

## 已知陷阱

1. **Survivorship bias** — yfinance 只回傳目前上市的股票，過去被下市的失敗案例不會出現 → 結果系統性偏高。Constituent rebalance 也沒處理（用今天的 S&P 500 反向應用到 3 年前）。
2. **0050.TW universe 是 2026-05 快照** — 早期的 TW50 成份股可能不同，目前的 list 同時是 winner-biased。
3. **無 fundamental filter** — EP 訊號可能包含財報失常、併購消息等 noise，未驗證催化劑性質。
4. **TW 漲跌停未模擬** — EP 在 TW 會被 ±10% 限制截斷。
5. **VectorBT cash-sharing 行為簡化** — 真實 broker 可能在多訊號同日下會排隊；模擬假設可全部按比例分配。

---

## 下一步建議

**v1（高 ROI）：**
- 跑 **Russell 2000 / NASDAQ 中小型** universe，breakout setup 用 strict profile。這是 QM 真正設計的場景。
- 加 sector rotation overlay（XLK / XLE 等），避免在弱勢族群進場。

**v2（中 ROI）：**
- 修 survivorship bias：用 NASDAQ Trader 歷史 delisted symbol directory 補回。
- 修 constituent drift：歷史 S&P 500 成份股表（可從 Wikipedia revision history 或付費資料）。
- TW 漲跌停模擬 (clip gap at +10%)。

**v3（投資前必做）：**
- Walk-forward optimization 避免 in-sample overfit。
- Out-of-sample 用更早期的 2020-2022 熊市段資料驗證 EP 是否在弱勢市場仍有 edge。

---

## 持久化

每次跑都在 `data/backtest/runs/{date}_{universe}_{setup}_{profile}_{years}y/` 留：
- `stats.json` — 結果摘要
- `trades.parquet` — 個別交易記錄
- `equity_curve.parquet` — 淨值曲線
- `entries.parquet` — 訊號矩陣

OHLCV cache 在 `data/ohlcv/{us,tw}/{TICKER}.parquet`，永久保留，重跑只 incremental download。

---

## 怎麼跑

```bash
# 安裝（首次）— vectorbt 透過 uv run --with 即時拉
# Universe 在 data/universe/{sp500,tw50}.txt

# 跑 EP × S&P 500（強推薦的起點）
uv run scripts/qm/backtest/run.py --universe sp500 --setup ep --profile bigcap --years 3

# 跑 breakout × Taiwan 50
uv run scripts/qm/backtest/run.py --universe tw50 --setup breakout --profile bigcap --years 3

# 跑兩種訊號合併
uv run scripts/qm/backtest/run.py --universe sp500 --setup both --profile strict --years 5
```

**Profile：** `strict` (Qullamaggie 原始, 適合小中型) / `bigcap` (放寬, 適合大型指數)
**Setup：** `breakout` / `ep` / `both`

---

*本回測不構成投資建議。所有數字基於 yfinance 公開資料，可能有錯漏。Sample sizes 偏小的結論需更多市場期間驗證。*
