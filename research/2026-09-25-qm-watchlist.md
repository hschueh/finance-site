# Qullamaggie 觀察名單追蹤 — 2026-09-25

僅重新檢查既有觀察名單（未跑全市場掃描）。

> 📅 台股 9/25 **中秋節休市**，本次無台股資料；觀察名單目前也無台股名字。
> yfinance 的 9/25 美股日線 K 棒在收盤後尚未合併（OHLC 全 NaN、僅 volume 有值），
> 腳本已改為偵測到此情況時自動退回**盤中最後價**並標註（見下方 ⚠️），
> 不再靜默沿用前一交易日收盤。

## 📌 觀察名單追蹤 (watchlist)

> ⚠️ **日線尚未合併，以下以盤中最後價判定**：TRLV, GLND, FET, PD, GCT, SRZN, JOYY, VRNS

### 🔴 觸發 (TRIGGERED)

_本次無觸發。_


### 👀 持續觀察 (watching)

| Ticker | 型態 | 距觸發 / 跳空 | 已追蹤 | 區間高點 / 守價 |
|--------|------|--------------|--------|-----------------|
| [GLND](https://finance.yahoo.com/quote/GLND/chart) | EP | gap +11% | 1d | 守 2.91 |
| [SRZN](https://finance.yahoo.com/quote/SRZN/chart) | EP | gap +89% | 1d | 守 16.16 |
| [GCT](https://finance.yahoo.com/quote/GCT/chart) | breakout | -0.1% | 1d | 54.13 |
| [TRLV](https://finance.yahoo.com/quote/TRLV/chart) | breakout | -0.7% | 12d | 12.30 |
| [JOYY](https://finance.yahoo.com/quote/JOYY/chart) | breakout | -1.0% | 1d | 80.58 |
| [FET](https://finance.yahoo.com/quote/FET/chart) | breakout | -1.7% | 1d | 84.20 |
| [PD](https://finance.yahoo.com/quote/PD/chart) | breakout | -4.5% | 1d | 15.05 |


### ❌ 本次踢出 (kicked out)

| Ticker | 型態 | 結局 | 原因 |
|--------|------|------|------|
| CFFI | breakout | broken | 跌破 20DMA |
| VRNS | breakout | broken | 跌破 20DMA |


## 讀數

- **連續兩日零觸發。** 觀察名單 9 → 7 檔（CFFI、VRNS 雙雙跌破 20DMA 出局）。
- **VRNS 出局。** 9/24 週報點名它是名單裡唯一「緊縮型態 + 基本面雙合格」
  （41% BUY），週五 −3.55% 至 46.25，**險破 20DMA（46.35）0.2%**，
  依狀態機規則歸類 broken。差距極小，但規則就是規則——若要續抱須另有理由。
- **最接近觸發：GCT −0.1%、TRLV −0.7%。** 兩檔都在 1% 內，TRLV 已追蹤 12 天，
  接近 15 天 stale 上限。
- **SRZN −12.29%**，印證 9/24 週報判斷：+89% 跳空但 60 日 −36%、量化分 37% SELL，
  是深谷反彈不是強勢股催化。守價 16.16 未破，但不建議跟。

## ⚠️ 限制

- 觸發/壞掉判定依日線收盤；yfinance 延遲 15-20 分鐘
- 不構成投資建議
