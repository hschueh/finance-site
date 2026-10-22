# 2026-10-22 週中更新 — 選擇權收租候選首測：權利金最肥的八檔，全卡在財報前

**涵蓋期間：** 2026-10-17 ~ 2026-10-21（美股收盤）/ 10-22（台股收盤）
**資料來源：** QM 全市場掃描 + 覆蓋池量化（含 `--vol` 選擇權收租排名）+ 少量盤勢 / 個股搜尋
**性質：** 非週末的測試跑，主要驗證新加的 **💵 選擇權收租候選** 章節。B 段研究只補上週週報沒涵蓋的部分，產業判斷沿用 [2026-10-17 週報](2026-10-17-weekly-report.md)。

---

## 0. 三個結論

1. **權利金最肥的八檔全卡在財報前。** 照「INCOME = 量化分數 × 年化 put 殖利率」排序，前段的 BE、AAOI、FN、COHR、APP、VRT、SMCI、LITE 年化殖利率 54–96%，但 30 天到期內**全部都有財報**（BE 今天 10/22、VRT 10/28、AAOI/COHR/APP/LITE 11/4–11/5）。它們的 IV 高，是因為財報會跳空，不是白送的錢。**這週真正能做的名單只有 MU、SNOW、DELL、PL，以及 CRWD 的 Covered Call。**
2. **首選是 MU Sell Put。** 履約價約 858，現價 914（−6%），年化約 40%，財報在 12/23，晚於到期日。上週已確認它的 HBM 產能整個 CY2027 已售完，也是 ram 群裡受長鑫衝擊最小的一檔，被指派也願意長抱。南亞科（2408）的理論殖利率差不多（44%），但長鑫 4F² 瞄準的正是它，**同一個記憶體曝險，Sell Put 選 MU**。
3. **DELL 殖利率 51%、沒有財報，但刻意降級。** 上週它是覆蓋池裡處在「neocloud 融資鏈」最弱一環的名字。CoreWeave CDS 這週**還在擴大**，超過 1,000bp。現在賣 Put，等於在信用利差還沒穩定前就先承諾接貨。

---

## 1. 盤勢（10/17 → 10/21）

- **股債分歧。** 10/19–20 Dow 反彈約 500 點，S&P 小漲、Nasdaq 持平，費半在週一反彈後週二又回吐。CNBC 的標題很直白：**股票投資人準備翻篇了，信用投資人還沒。** CoreWeave 5 年期 CDS 仍在 1,000bp 以上、週二再擴大，2032 年到期債殖利率約 14.9%，Oracle 債殖利率也維持在高檔。
- **財報季開打。** GM 財報 beat，但指引不如預期，股價一度 −7%。META 10/21 盤後公布財報，盤後先漲後跌，2027 年 capex 的說法是拉鋸焦點；目前只有初步報導，**尚未確認收盤反應**。下週 10/28 有 GOOGL 和 VRT。
- **覆蓋池 1 日漲跌（10/21 美 / 10/22 台）：** 美股反彈，SMCI +9.5%、BE +7.1%、DDOG +6.5%、DELL/CRWD/NET +5%；台股被動元件和記憶體回落，2492 −9.2%、3026 −7.2%、2327 −6.5%、2408 −5.2%。

**Sources:** [CNBC 10/20](https://www.cnbc.com/2026/10/19/stock-market-today-live-updates.html) · [CNBC 信用 vs 股票](https://www.cnbc.com/2026/10/19/coreweave-oracle-ai-credit-stress.html) · [Closing Look 10/20](https://cappnotes.substack.com/p/closing-look-tuesday-october-20-2026) · [GM Q3](https://www.cnbc.com/2026/10/20/general-motors-gm-earnings-q3-2026.html) · [24/7 Wall St. META](https://247wallst.com/investing/2026/10/21/live-will-meta-crush-q3-earnings-tonight-after-the-bell) · [TradingView META preview](https://www.tradingview.com/news/coinpedia:ee1373083094b:0-meta-platforms-earnings-today-why-2027-spending-guidance-could-move-meta-stock/)

---

## 2. 覆蓋池量化前段（BUY ≥ 40%）

| 代號 | 群組 | 分數 | EPS 驚喜 | Beats | Fwd P/E | 分析師目標價空間 |
|------|------|-----|---------|-------|--------|---------------|
| GOOGL | bigtech | 52% | +214% | 3/4 | 21.9x | +28.5% (54) |
| VRT | aiinfra | 50% | +6.3% | 3/4 | 23.1x | +57.0% (28) |
| BE | power | 48% | +90% | 3/4 | 48.4x | +20.2% (26) |
| ALKS | health | 46% | +141% | 3/4 | 24.1x | +29.3% (19) |
| CEG | power | 45% | +11.8% | 3/4 | 20.4x | +24.9% (22) |
| 2408.TW | ram | 45% | +8.8% | 3/4 | 3.5x | +48.6% (14) |
| FN | optics | 44% | +7.6% | 3/4 | 16.2x | +93.2% (9) |
| PL | leo | 44% | +200% | 2/4 | — | +120.8% (11) |
| 3026.TW | passives | 44% | +30.7% | 3/4 | 21.6x | +39.1% (3) |
| DELL | aiinfra | 44% | +43.1% | 3/4 | 16.2x | +22.0% (25) |
| MU | ram | 43% | +5.0% | 3/4 | 4.4x | +70.8% (46) |

和上週相比，DELL 從 55% 降到 44%，主要是分析師分項被 Barclays 降評拖累。

---

## 💵 選擇權收租候選

> 篩選邏輯：量化分數 × 年化權利金殖利率（30Δ、11/20 到期，約 29 天）。
> 只列「看好、而且波動大到權利金值得收」的名字。非投資建議。
> 本次殖利率是用選擇權鏈 ATM 價格反推 IV 後，以 Black-Scholes 估算。原因是美股收盤後 Yahoo 的 bid/ask 全為 0，**沒有可用的 mid 價**，實際成交價可能有幾個百分點的差距。

| 代號 | 策略 | 量化分數 | IV | IV/HV | 30Δ 履約價（現價） | 年化殖利率 | 備註 |
|------|------|---------|----|------|------------------|-----------|------|
| **MU** | Sell Put | 43% | 52% | 1.15 | 858（914） | 40% | **首選**：HBM 鎖約到 CY2027，財報 12/23 晚於到期日；HV%ile 只有 1，代表實際波動在年內低點，但 IV 仍偏高 |
| SNOW | Sell Put | 34% | 54% | 1.02 | 302（323） | 42% | 財報 12/2 晚於到期日。Cortex AI 帶動用量的說法有分析師背書；Fwd P/E 107x 偏貴、GAAP 仍虧損，被指派的成本要想清楚 |
| CRWD | Covered Call | 32%（HOLD） | 56% | 1.09 | Call 履約價約 264（239） | 35%（CC） | 持股才做。財報 12/1 晚於到期日；HOLD 訊號配 CC 正好對上 |
| DELL | Sell Put（**降級**） | 44% | 64% | 0.98 | 451（486） | 51% | 財報 11/27 晚於到期日，但屬 neocloud 融資鏈。CoreWeave CDS 還在擴大，**等信用利差穩定再做**；IV/HV < 1，權利金也不算貴 |
| PL | Sell Put（**降級**） | 44% | 68% | 0.94 | 12.7（13.7） | 55% | 從高點跌超過 60%，Morgan Stanley 是 Equal Weight（擔心投資期壓縮毛利），2/4 beats 達標紀錄不穩。殖利率高，但「願意長抱」這條沒過 |
| 3026.TW 禾伸堂 | Sell Put（理論值） | 44% | HV 78% | — | 690（756） | 64% | **理論值，台灣個股選擇權流動性低，實際成交可能差很多**；今天才 −7.2% |
| 2408.TW 南亞科 | Sell Put（理論值） | 45% | HV 56% | — | 386（414） | 44% | 理論值；長鑫 4F² 瞄準的正是它，**同一個曝險改做 MU** |

**本週重點：** MU 是唯一同時滿足三個條件的名字：基本面有長約保護、到期前沒有財報、IV 高於實際波動。SNOW 次之。DELL 的量化分數和殖利率都夠，**刻意不推**，理由不是數字而是 B 段的判斷：它的客戶在借錢，這週信用市場還沒放行。

**財報後再看（⚠E）：** BE（10/22，今天）、VRT（10/28）、GOOGL（10/28）、FN（11/2）、SMCI（11/3）、COHR / APP（11/4）、AAOI / LITE（11/5）、CEG（11/9）、NVDA（11/17）。其中 FN 和 APP 的 IV/HV ≥ 1.2（💰），財報後如果 IV 沒有完全回落，是下一輪最值得看的兩檔。也可以直接選 12 月到期，跨過財報。

**本週不建議收租：** 2382 廣達（分數 42%，年化只有 16%）和 RTX（20%）是看好但權利金太薄，**不是因為不看好**。GOOGL 的 IV 37% 看起來不低，但它的 HV20 只有 19%，多出來的部分全是 10/28 財報溢價，財報後會回到年化 15% 以下。

**和 QM 觀察名單的交集：** 無。本期觀察名單 18 檔裡沒有覆蓋池名字，所以沒有「在 base 下緣賣 Put 等突破」的組合。

---

## 3. QM 動能掃描（摘要）

全市場 8,587 → Stage 1 998 → Stage 2 12 檔，和上週一樣接近乾涸。觸發 5 檔：JOYY、CRVL、ENGS、CERT、UFCS。踢出 5 檔，其中 3 檔是台股：3044 健鼎觸發後跌破 20DMA、2357 華碩跌破 base、3014 跌破 20DMA。

觀察名單 18 檔，**低於 25 檔的群聚寬度門檻**。Financial Services 有 5 檔群聚，但只能視為雜訊，不構成覆蓋池新增的理由。完整內容見 [QM 掃描報告](2026-10-22-qm-scan.md)。

**覆蓋池調整建議：** 無。週中測試跑不改覆蓋池。

---

## 4. 這次測試順便抓到並修掉的兩個 bug

1. **`vol_metrics.py` 原本信任 Yahoo 的 `impliedVolatility` 欄位。** 收盤後 bid/ask 為 0 時，這個欄位是解算器失敗後吐出的佔位值（1e-5、1/64、2/64），所以**第一次跑出來的結果是錯的**：美股幾乎全部靜默退回 HV，而 SMCI 顯示 IV 2%。已改成自己用 Black-Scholes 從價格反推，有 live bid/ask 用 mid，沒有就用 4 天內的 `lastPrice`，並加上 5%–300% 的合理範圍檢查。美股抓鏈失敗現在標成 `HV*`，跟台股的 `HV` 分開。本報告的數字都是修正後的版本。
2. **QM 掃描和 `analyze.sh all` 同時跑，會搶 Yahoo 額度。** 第一次有 10 檔（CEG、RTX、APP、HOOD 等）被 rate limit 打掉，而且沒有任何警告。已重跑補齊，weekly-scan skill 也改成兩個長任務依序執行，跑完要檢查錯誤數。

---

## ⚠️ 限制

- 美股殖利率是用收盤前最後成交價反推的 IV 去估算，不是 live mid；開盤後的實際報價可能差幾個百分點。
- 台股全部是 HV20 理論值，台灣個股選擇權實際流動性很差。
- META 財報反應、PL / SNOW 的分析師資料部分來自單一或日期不明的來源，未逐一核對原始資料。

**Sources（個股）：** [MarketBeat PL](https://www.marketbeat.com/articles/planet-labs-has-fallen-back-to-earth-but-wall-street-still-sees-a-rebound/) · [Yahoo MS 調升 PL 目標價](https://finance.yahoo.com/markets/stocks/articles/morgan-stanley-raises-planet-labs-143620987.html) · [Benzinga PL](https://www.benzinga.com/node/61512415) · [Yahoo SNOW 目標價](https://finance.yahoo.com/markets/stocks/articles/wall-street-sees-66-upside-142811048.html) · [Oppenheimer SNOW Cortex](https://finance.yahoo.com/markets/stocks/articles/oppenheimer-says-cortex-code-driving-134832298.html) · [TIKR SNOW](https://www.tikr.com/blog/snowflake-stock-has-lost-half-its-value-in-2026-why-analysts-still-say-buy?)
