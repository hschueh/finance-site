# 2026-10-17 週報 — 折現率的另一半：這週壞掉的是信用利差，不是殖利率

**涵蓋期間：** 2026-10-03 ~ 2026-10-16
**資料來源：** QM 全市場掃描（含 universe 更新）+ 覆蓋池 76 檔量化 + 約 30 則產業/法說/分析師搜尋

---

## 0. 本週三個結論

1. **這週覆蓋池下跌的主因是「客戶需不需要借錢」，不是「現金流在多遠以後」。** 10Y 殖利率這週其實**下跌約 15bp**，從 24 年高點回到 5% 附近；照上兩期的久期判準，遠期現金流資產應該喘一口氣。結果 SMR −19%、OKLO −19%、BE −21%、光通訊 −25~−31%、DELL −23%，跌得比殖利率創高的那兩週還慘。原因是**折現率的另一半——信用利差——爆開了**：CoreWeave 2031 年債殖利率衝到 15–16%，5 年期 CDS 一度超過 1,100bp，已經是困境（distressed）水位。把覆蓋池按「客戶的錢從哪裡來」重新分組，跌幅排序幾乎完全對得上（第 2 節）。

2. **基本面這週是上修的，跌的是 2027 年以後「需求由誰出錢」的信心。** 同一週，台積電 Q3 營收 $467 億（年增 41%，超出預期 $449 億），Q4 指引 $523–543 億；ASML 說 2027、2028 年的 EUV 供給**都無法滿足客戶需求**，有客戶已經在問 2029–2030 年的訂單；鴻海 9 月營收 1.15 兆（首度破兆，年增 38%）；國巨、華新科 9 月營收年增 46%、54%。DELL 下跌 **19% 的兩個交易日裡，公司的財報和指引都沒有任何變動**。上期寫的「融資條件是這個故事唯一真正的單點故障」，這週被直接測試了。

3. **長鑫 4F² 用上期的「擴產前置期」檢查表檢驗：是中期威脅，不是這個週期的威脅，但威脅的對象是 2408/2344，不是 MU。** 長鑫宣布年底推出 4F² 架構的 DDR5 RDIMM，10/13 外資單日賣超台股 1,653 億（史上第三大），南亞科、華邦電兩天各跌約 7%。但長鑫還沒公布良率、容量和客戶認證結果，它瞄準的是**伺服器標準型 DDR5**，不是 HBM。這代表 MU（HBM 已鎖長約到 CY2027）和南亞科/華邦電（賣的就是標準型 DRAM）面對的是不同程度的威脅，ram 群內的排序要再往 MU 傾斜（第 4 節）。

---

## 1. 宏觀：殖利率回落，科技股反而跌出 6 月以來最差的一週

| 項目 | 上期 (10/03) | 本期 (10/16) |
|------|------------|-------------|
| 10Y 美債殖利率 | 5.306%（2002 年來最高） | **約 5.0%**（單週 −15bp，三週低點） |
| 9 月 CPI（10/14 公布） | — | 整體 +0.6% MoM / 3.7% YoY；**核心 +0.3% MoM（預期 +0.2%）/ 2.6% YoY** |
| 10 月 FOMC 升息機率 | 34% → 市場不再預期 | CPI 後一度升高，週末回到約 **15%** |
| Brent | — | 高檔震盪（價格來源互相矛盾，未採用單一數字） |
| S&P 500 單週 | — | 約 **−2%** |
| Nasdaq 單週 | — | **−4% 以上**，6 月以來最差 |
| 費半（SOX） | — | 單週約 **−11.4%**，連跌 8 個交易日，2025 年 4 月以來最差的一週 |
| Dow 單週 | — | **+0.7%** |

**Dow 漲、Nasdaq 跌 4%** 是本週最重要的一張圖：這不是全面的 risk-off，是**資金從「需要融資才能兌現的成長」撤出，換到「現金流已經在帳上」的資產**。

本週引爆 AI 賣壓的三件事，依時間排序：

1. **10/8 — FT：OpenAI 9 月底年化營收接近 $500 億**，比 9 月底在媒體流傳的約 $700 億少了一截。差距的來源是口徑：Anthropic 的數字含透過 AWS/Google Cloud 賣出的營收，OpenAI 不含。OpenAI 企業端上季成長 107%，成長本身沒問題，但**市場拿來替整條供應鏈估值的「終端需求」數字被下修了 30%**。
2. **10/14 — 9 月核心 CPI 高於預期**，升息機率回升。同一天 Barclays 把 DELL 從 Overweight 降到 Equal Weight。
3. **10/14–16 — CoreWeave 股價單日 −15%，債殖利率衝破 15–16%，CDS 一度超過 1,140bp。** CoreWeave 的債務與承諾約 **$500 億**，S&P 評等 B+。Bloomberg 報導高收益債買家開始**拒絕新的 AI 資料中心發債**。

**Sources:** [CNN AI 債務](https://cnn.com/2026/10/16/investing/tech-stocks-ai-coreweave) · [CNN 晶片賣壓](https://www.cnn.com/2026/10/15/business/tech-selloff-nasdaq-ai-intl) · [Yahoo 週線](https://finance.yahoo.com/markets/live/stock-market-today-dow-sp-500-nasdaq-futures-mixed-amid-volatile-week-112939401.html) · [Schwab](https://www.schwab.com/learn/story/stock-market-update-open) · [XTB CPI](https://www.xtb.com/en/market-analysis/us-cpi-above-expectations) · [FTPortfolios CPI](https://www.ftportfolios.com/Commentary/EconomicResearch/2026/10/14/the-consumer-price-index-cpi-rose-0.6percent-in-september) · [Bloomberg Tax / FT OpenAI](https://news.bloombergtax.com/artificial-intelligence/openais-annualized-revenue-nears-50-billion-ft-says) · [Zawya/Reuters OpenAI](https://www.zawya.com/en/special-coverage/openais-september-annualized-revenue-nears-50bln-less-than-previously-indicated-source-says-1586243) · [Eurasia Business News](https://eurasiabusinessnews.com/2026/10/17/stock-market-today-ai-selloff-sends-wall-street-to-worst-week-since-june/)

---

## 2. 本週最重要的觀察：覆蓋池按「客戶的錢從哪來」重新排序

上兩期用「久期」（現金流在多遠以後）解釋覆蓋池的分化，這週這個解釋**失效**了——殖利率下跌，遠期資產卻跌更多。換一個軸就對上了：**你的客戶（或你自己）需不需要靠外部融資才能付錢？**

| 資金來源 | 覆蓋池代表 | 5 日 % | 判讀 |
|---------|-----------|-------:|------|
| **政府預算** | NOC / LMT / RTX / GD | **+8.1 / +8.3 / +4.3 / +3.9** | 客戶是國防部，不需要發高收益債 |
| **自有現金流的 hyperscaler** | AAPL / MSFT / META / GOOGL | +2.0 / −1.1 / −1.3 / −3.1 | 自己就是付錢的人，融資壓力最小 |
| **賣給 hyperscaler 的上游** | 2330 / 2382 / 2317 | −5.1 / −1.1 / −2.0 | 客戶有錢，跌幅有限 |
| **已被 SaaSpocalypse 打過一輪的 SaaS** | CRM / PAYC / PCTY | **+5.0 / +8.4 / +8.0** | 空方論點已被定價，反而變成避風港 |
| **資安 SaaS（高倍數）** | PANW / CRWD / NET / OKTA | −18.3 / −17.3 / −17.9 / −19.3 | 見 5.3 |
| **伺服器/網通（客戶含 neocloud）** | DELL / SMCI / ANET / VRT | **−22.9 / −24.4 / −18.3 / −15.0** | CoreWeave 等 neocloud 是直接客戶 |
| **光通訊** | COHR / LITE / FN / AAOI | **−25.5 / −25.3 / −25.2 / −31.1** | 上期的漲幅全數吐回 |
| **自己還要融資的電力** | BE / OKLO / SMR | **−21.1 / −19.4 / −19.0** | BE 透過 Brookfield JV 的關係人營收，正是融資鏈的一環 |
| **運轉中的電力** | CEG / VST / FSLR | −9.0 / −5.9 / **−2.9** | FSLR 只跌 2.9%：它的問題是利率，而利率這週是下跌的 |

**三個值得記下來的細節：**

- **FSLR vs BE 是最乾淨的對照。** 兩者都在 power 群、都是「替資料中心供電」的敘事。上兩期 FSLR 是被殖利率打下來的；這週殖利率回落，FSLR 只跌 2.9%。BE 是這週才被打的（−21%），因為它的成長有很大一塊是透過 Brookfield 的合資架構——**本質上是融資驅動的訂單**。覆蓋池 note 裡寫的「watch related-party revenue via Brookfield JVs」，這週就是那個風險被定價的時刻。
- **上期 5 日漲幅前段班幾乎全數反轉**：環球晶 +25.3% → −20.2%、光通訊 +11~15% → −25%、南電 +20.7% → −8.1%、欣興 +12.5% → −14.2%。上期第 5.6 節寫過「光通訊這 5 日的漲幅相當程度是資金面的」——這週證實了那筆帳該分開記。
- **國防四檔這週全數上漲**，但我**沒有找到單一催化劑**。這和「資金從需要融資的 AI 鏈輪動到預算型客戶」的解釋一致，但這是推論，不是新聞驗證過的因果。上期列為待追蹤的「backlog 飆、股價跌」落差，這週開始收斂。

### 2.1 CoreWeave 為什麼重要：它是需求鏈裡「借錢的那一環」

上期第 6 節引用過一組數字：hyperscaler 的 capex 已達雲端營收的 **102%**，六大中 2027 年預計只有 **1 家**有正自由現金流。Macquarie 8 月的報告也指出，**債務在 hyperscaler capex 資金來源中的比重正在上升**；Epoch AI 估計 hyperscaler 的現金 capex 約在 **2026 Q3** 超過營運現金流。

CoreWeave 是這條鏈上信用最弱的一環（B+ 評等、約 $500 億債務與承諾、backlog 約 $550 億）。CEO Intrator 的回應是「backlog 足以覆蓋債務義務」——但 **backlog 本身就是對 OpenAI、Microsoft 等客戶的未來應收款**，在 OpenAI 營收被下修 30% 的同一週，市場不接受這個說法。Jensen Huang 說 CoreWeave「每天都在變強」，但這不構成 NVDA 新的財務支持。

**對覆蓋池的意義：** 真正的問題不是 CoreWeave 會不會違約，而是**高收益債市場對 AI 資料中心的融資窗口會不會關上**。Bloomberg 10/17 報導高收益債買家已開始拒絕 AI 新創的發債。如果這個窗口關上，第一個受影響的是 neocloud 的新訂單，再往上傳到 DELL/SMCI 的伺服器、ANET 的交換器、光通訊的模組。**hyperscaler 本身不受影響（它們的債是投資等級），所以 2330/2382 的影響比 DELL/SMCI 晚、也比較小。**

**Sources:** [CNBC CoreWeave CDS](https://www.cnbc.com/2026/10/15/coreweave-credit-default-swaps-hit-distress-levels-as-investors-sour-on-ai-debt.html) · [Bloomberg AI 高收益債](https://www.bloomberg.com/news/articles/2026-10-17/coreweave-woes-risk-shutting-down-ai-junk-market-credit-weekly) · [Globe and Mail/Reuters](https://www.theglobeandmail.com/investing/article-coreweave-shares-bonds-slide-further-as-ai-debt-fears-mount/) · [Axios](https://www.axios.com/2026/10/15/ai-coreweave-bonds-stocks) · [ROIC Huang 談 CoreWeave](https://www.roic.ai/news/huang-says-coreweaves-strength-is-improving-every-day-but-debt-concerns-persist-10-15-2026) · [Macquarie 8/21](https://www.macquarie.com.au/assets/bfs/documents/private-bank/investment-insights/investment-strategy-insights-21-august-2026.pdf) · [Epoch AI](https://epoch.ai/data-insights/hyperscaler-capex-vs-cash-flow)

---

## 3. 基本面這週是上修的

| 公司 | 本週公布 | 數字 |
|------|---------|------|
| **台積電 (2330)** | Q3 財報（10/15） | 營收 **$467 億，年增 41%**（預期 $449 億）；EPS NT$29.43；毛利率 66.4%、營益率 58.7%。**Q4 指引 $523–543 億**；全年營收成長約 44%；capex 維持 $600–640 億 |
| **ASML** | Q3 財報（10/14） | 營收 €117 億、毛利率 57.5%；Q4 指引 €142–152 億，全年 €440–450 億。2027 年 low-NA EUV 產能 +30%、2028 年研議再 +30%，**但兩年的供給都無法完全滿足需求**；有客戶已在洽談 2029–2030 年訂單 |
| **鴻海 (2317)** | 9 月營收 | **1.15 兆，首度單月破兆**，月增 25.7%、年增 38.4%；Q3 3.02 兆、年增 47.1% |
| **廣達 (2382)** | 9 月營收 | 9 月年增 77%，**Q3 首度突破 1.1 兆**；GB300 是 Q4 主要動能，Vera Rubin Q4 小量出貨、**2027 Q1 放量** |
| **國巨 (2327)** | 9 月營收 | 170.68 億，月增 4.5%、**年增 46.1%**；前 9 月年增 36.3% |
| **華新科 (2492)** | 9 月營收 | 48.89 億，月增 7.0%、**年增 53.9%**；Q3 EPS 2.07 元 |
| **DELL** | （無新數字） | 9 月初上調 FY27 營收指引到約 **$1,920 億**，AI 伺服器約 **$740 億**（約為去年的 3 倍），EPS $25.50。本週**沒有任何變動** |

**台積電的市場反應（ADR 隔夜 −1.7%）值得注意：** 原因不是營收，是管理層說擴產投資會持續稀釋毛利率（全年約 2 個百分點，Q4 壓力更大）。**在信用利差擴大的這一週，市場對「繼續砸錢擴產」的容忍度變低了，連台積電都不例外。**

**Sources:** [TSMC 6-K](https://www.sec.gov/Archives/edgar/data/0001046179/000104617926000726/a3q26e_withguidancexfinal.htm) · [TSMC 新聞稿](https://pr.tsmc.com/schinese/news/3346) · [stockhub TSMC](https://stockhub.kr/en/news/news_b40c7d7eea3f) · [MarketBeat ASML 法說](https://www.marketbeat.com/instant-alerts/transcript-what-asml-asml-said-on-its-q3-earnings-call-2026-10-14/) · [ASML 6-K](https://www.sec.gov/Archives/edgar/data/0000937966/000162828026065813/pressreleasefinancialresul.htm) · [優分析 鴻海](https://uanalyze.com.tw/articles/2032056538) · [財報狗 廣達](https://statementdog.com/news/17848) · [TechNews 國巨](https://finance.technews.tw/2026/10/08/yageo-2327-202609-financial-report/) · [TechNews 華新科](https://finance.technews.tw/2026/10/08/wtc-2492-202609-financial-report/) · [Dombey DELL](https://www.dombey.capital/market/why-dell-stock-fell)

---

## 4. 記憶體：長鑫 4F²，用上期的檢查表來量

上期從 WDC/東芝事件整理出一個檢查表：**替一個「短缺」出價之前，先量 (a) 新產能的前置期；(b) 新產能需要什麼價格才有 IRR；(c) 現有玩家有多少閒置設備可以直接開回來。**這週拿來量長鑫：

| | 東芝 HDD（上期） | **長鑫 4F² DRAM（本期）** |
|---|---|---|
| 公布內容 | $3.8 億、FY2027 產能翻倍 | 年底推出 4F² 架構 DDR5 RDIMM |
| 已驗證程度 | 資本支出已承諾 | **未公布容量、速度、功耗、良率、客戶認證** |
| 製程門檻 | 設備可複製 | 6F² → 4F² 要重新調整製程，原有工序不能沿用 |
| 鎖定市場 | 全部 HDD | **伺服器標準型 DDR5**（不是 HBM） |
| 市佔 | 東芝為 HDD 第三大 | 長鑫 Q2 DRAM 營收市佔約 **7%**，全球第四 |
| 供給反應風險 | **高、近期** | **中、2027 年以後** |

**結論：** 這是技術路線的公開，不是產能的公開。Morningstar 分析師的提醒是對的——「技術突破不等於能商業化量產」。三星計畫 2028 年量產 4F²，外媒推算長鑫可能早約兩年，但比較的是兩家的**預期時間表**，不是已經達成的量產。

**但威脅的方向要分清楚：**
- **MU**：HBM3E/HBM4 整個 CY2027 已售完、FY27 產出 75% 以上已簽約（上期資料）。長鑫在 HBM 仍是後進者。**受影響最小。** 量化分 50% BUY、Fwd P/E 4.2x，分析師目標價 +77.6%（46 位）。
- **南亞科 (2408) / 華邦電 (2344)**：賣的正是標準型 DRAM，**長鑫瞄準的就是這個市場**。凱基把南亞科目標價從 720 上調到 800 元（增持），富邦維持買進、目標 660 元——賣方並沒有因為長鑫下調。但結構上，這兩檔比 MU 更直接暴露在長鑫的風險下。
- **韓國連動**：三星、SK 海力士同週連跌 5 日、各跌超過 5%，且據報兩家的庫藏股回購**提前結束**。10/13 台股外資賣超的重心是記憶體 + 台積電，近 5 日累計賣超 3,130 億。

**這再一次說明 ram 群要拆開看：** MU（HBM 長約）、WDC（HDD，東芝產能）、2408/2344（標準型 DRAM，長鑫）是三種不同的瓶頸，保存期限各不相同。

**Sources:** [財報狗 長鑫](https://statementdog.com/news/17876) · [優分析 長鑫良率](https://uanalyze.com.tw/articles/2269156987) · [unwire.hk](https://unwire.hk/2026/10/11/cxmt-4f2-ddr5-rdimm-samsung/parts/) · [今周刊 記憶體](https://www.businesstoday.com.tw/article/category/183008/post/202610130003/) · [工商時報 外資](https://www.ctee.com.tw/news/20261015701932-430201) · [優分析 外資 1653 億](https://uanalyze.com.tw/articles/1530456995) · [風傳媒](https://www.storm.mg/article/11171854) · [SamMobile HBM 佔比](https://www.sammobile.com/?p=16680504) · [Yahoo Baird MU](https://finance.yahoo.com/news/micron-estimates-raised-baird-surging-192800868.html)

---

## 5. 覆蓋池量化排序與重點名字

### 5.1 BUY ≥ 35%（共 40 檔，列前 15）

| Ticker | 群組 | 分數 | EPS% | Beats | Fwd P/E | 分析師 | 5日 % |
|--------|------|-----:|-----:|:-----:|--------:|-------:|------:|
| **DELL** | aiinfra | **55%** | +43.1% | 3/4 | 15.1x | +31.3%(25) | **−22.9** |
| CEG | power | 54% | +11.8% | 3/4 | 20.4x | +24.4%(22) | −9.0 |
| ANET | aiinfra | 54% | +14.6% | 3/4 | 33.9x | +38.5%(29) | −18.3 |
| 2382 廣達 | tw | 53% | +15.9% | 3/4 | 10.1x | +32.9%(19) | −1.1 |
| GOOGL | bigtech | 52% | +214.1% | 3/4 | 22.3x | +26.4%(54) | −3.1 |
| VRT | aiinfra | 51% | +6.3% | 3/4 | 22.4x | +61.7%(28) | −15.0 |
| HOOD | fins | 50% | +44.2% | 2/4 | 28.9x | +35.9%(29) | −9.3 |
| MU | ram | 50% | +5.0% | 3/4 | 4.2x | +77.6%(46) | −14.6 |
| WDC | ram | 50% | +7.9% | 3/4 | 10.0x | +101.4%(24) | −16.4 |
| BE | power | 50% | +90.2% | 3/4 | 44.8x | +29.0%(26) | −21.1 |
| FSLR | power | 47% | +36.1% | 2/4 | 7.3x | +58.6%(30) | −2.9 |
| SMCI | abf | 46% | +77.1% | 3/4 | 5.9x | +33.6%(15) | −24.4 |
| NOC | defense | 46% | +12.6% | 3/4 | 17.1x | +19.1%(24) | +8.1 |
| 2303 聯電 | tw | 46% | +203.6% | 2/4 | 18.2x | +5.8%(24) | −9.8 |
| ALKS | health | 45% | +141.4% | 3/4 | 22.8x | +36.4%(19) | +1.5 |

**先講結論：這張表本週的資訊量很低。** BUY 名單從上期 30 檔增加到 40 檔，主因是**價格下跌讓 Fwd P/E 和分析師目標價差距同時改善**——量化分機械性地上升了。上期 5.4 節對 FSLR 寫過的話，這週適用在半張表上：**便宜本身不是論點，便宜加上「造成便宜的原因即將消失」才是論點。**這週造成便宜的原因（信用利差）**還沒有消失的跡象**。

### 5.2 DELL（55%，本週最高）— 排第一的原因就是要小心的原因

**量化面：** EPS +43.1%、3/4 beats、Fwd P/E 15.1x、分析師目標價 +31.3%。兩天跌 19%。

**法說指引：** 9 月初上調 FY27 營收指引 $250 億到約 **$1,920 億**，AI 伺服器營收約 **$740 億**（約為去年 3 倍），EPS 指引 $25.50。本週沒有任何修正。**管理層紀錄：** 3/4 beats，且是在季中主動上調——偏保守文化。

**空方論點（Barclays Tim Long，10/14 降評至 Equal Weight，目標 $603 → $574）：** 企業端營收的強勁「**比較是記憶體成本轉嫁的結果，而不是企業 AI 採用**」。這個論點很重要，因為它和第 4 節是同一件事的兩面：**DRAM 合約價漲了將近一倍（Q1 季增 93–98%），伺服器 ASP 跟著漲，營收看起來在成長，但量和毛利未必。** Barclays 對 AI 伺服器營收的預估其實還是約 $750 億，和公司指引一致——它質疑的是**營收品質**，不是營收數字。

**多方論點：** AI Factory 企業客戶 5,000 家；新一代 Vera Rubin NVL72 的 CDU 冷卻方案已推出；指引剛上調、季中沒有修正。

**我的判讀：** DELL 的客戶組合裡 **neocloud（CoreWeave 是最大的之一）佔比顯著**，這是它比 2382 廣達（客戶以 hyperscaler 為主）跌得多的原因——同樣是 AI 伺服器組裝，**5 日 −22.9% vs −1.1%**。量化分 55% 排第一，**正是因為市場在定價一個量化分看不到的風險（客戶的融資能力）**。要轉多的觀察點：(1) 11 月底 Q3 FY27 財報的 AI 訂單與 backlog 是否維持；(2) 客戶組合中 neocloud vs hyperscaler/企業的比重是否有揭露；(3) 高收益債市場對 AI 資料中心的發債窗口是否重新打開。

### 5.3 資安 SaaS 單週 −17~−19%：三個原因疊在一起

PANW / CRWD 單週各跌約 18%，CIBR 單週約 −10%，**2020 年 3 月以來最差的一週**。原因有三個，來源沒有說哪一個最重要：
1. **OpenAI 被報導洽談收購資安公司 Trail of Bits** — 重新喚起「AI 開發商會直接和資安廠商競爭」的擔憂。諷刺的是 PANW 和 CRWD 同時也是 Anthropic 新資安計畫的合作夥伴：**AI 公司同時是合作夥伴和潛在對手。**
2. **PANW 防火牆平台被揭露遭利用的漏洞**，賣壓擴散到 Fortinet、Zscaler。
3. **AI 融資疑慮外溢到高倍數成長股。** PANW 的 forward normalized P/E 從 9/30 的約 95x 降到約 82x——還是很貴。

**對照組：CRM +5.0%、PAYC +8.4%、PCTY +8.0%。** 上期把 CRM 稱為「市場已付錢給空方論點」的案例（Fwd P/E 14.7x），這週在科技股大跌中逆勢上漲。**空方論點已經被充分定價的名字，在下一個空方論點出現時反而是避風港。** 這是一個可以重複使用的判斷：高倍數名字（PANW 70x、CRWD 141x、NET 177x）面對新的空方論點時沒有緩衝。

### 5.4 2382 廣達（53%）— 同樣是 AI 伺服器，客戶不同就是不同的股票

9 月營收年增 77%，Q3 首度突破 1.1 兆。管理層：AI 伺服器全年營收**年增三位數的展望不變**；GB300 是 Q4 主要動能；Vera Rubin Q4 小量、**2027 Q1 放量**；AI 伺服器佔整體伺服器營收 75–80%，目標 2026 年達 80%。Fwd P/E 10.1x、3/4 beats、分析師目標價 +32.9%（19 位）。

**5 日只跌 1.1%**，和 DELL −22.9% 形成本週覆蓋池最清楚的對照。廣達的主要客戶是自己發投資等級債的 hyperscaler，**不在第 2.1 節描述的融資鏈弱環上**。**這是本週覆蓋池裡「基本面在上修 + 不在信用風險傳導路徑上 + 量化分高」三者同時成立的少數名字之一。**

**風險：** Vera Rubin 的時程在不同報導裡有「Q4 放量」（鴻海口徑）和「2027 Q1 放量」（廣達口徑）的差異；新一代機櫃單價接近倍增，代表營收數字會被 ASP 墊高，和 DELL 的「營收品質」問題同源，只是程度較輕。

### 5.5 GOOGL（52%）與 CEG（54%）

- **GOOGL**：Google Cloud 營收年增 63% 至約 $200 億、backlog 接近翻倍到 **$4,600 億以上**（7 月資料）。空方：2026 capex 指引 $1,750–1,850 億、Q1 自由現金流 −47%。**本週 5 日只跌 3.1%，因為在第 2 節的分類裡它是「付錢的人」而不是「等著收錢的人」。**下個觀察點是 10 月底的 Q3 財報：capex 是否再上調，以及 cloud backlog 的成長。
- **CEG**：上期已詳述（Q2 上調全年指引、920MW 長期 PPA、平均年期 18.5 年）。本週 −9.0%，跌幅在 power 群裡屬溫和。和 BE/OKLO/SMR 的差距（−19~−21%）是**同一條判準的再一次驗證**：運轉中的機組 + 投資等級的交易對手，不需要靠高收益債市場。

### 5.6 落後段班（5 日）

| Ticker | 群組 | 5日 % | 原因 |
|--------|------|------:|------|
| AAOI | optics | **−31.1** | 光通訊整群吐回上期漲幅；AAOI 是群內最小、毛利率最低的一檔 |
| COHR / LITE / FN | optics | −25.5 / −25.3 / −25.2 | 同上；客戶含 neocloud |
| RKLB | leo | −25.5 | leo 四檔全數 −18~−26%；SpaceX 6/12 上市後下跌約 11%，整個太空板塊失去比價錨 |
| SMCI | abf | −24.4 | 伺服器組裝 + neocloud 客戶 |
| DELL | aiinfra | −22.9 | 見 5.2 |
| BE | power | −21.1 | 見第 2 節 |
| MTSI | defsemi | −20.5 | 雖然國防業務年增約 25%，但另一半是資料中心光通訊——它被當成光通訊股賣 |
| 6488 環球晶 | siwafer | −20.2 | 上期 +25.3%，全數吐回 |

**MTSI 是一個小但有用的提醒：** 同樣在 defsemi 群，MCHP 只跌 2.3%，MTSI 跌 20.5%——市場這週替 MTSI 定價的是它的**資料中心光通訊**曝險，不是國防。一家公司屬於哪個群組，要看市場這週在交易哪個風險因子。

**Sources:** [Barclays DELL / KuCoin](https://www.kucoin.com/news/flash/dell-stock-drops-11-as-barclays-cuts-rating-amid-ai-server-growth-concerns) · [Admiral DELL](https://admiralmarkets.com/education/articles/shares/dell-stock-forecast-barclays-downgrade) · [indmoney AI 賣壓](https://www.indmoney.com/blog/us-stocks/ai-stock-sell-off-inflation-rate-hike-fears) · [Yahoo 資安](https://finance.yahoo.com/markets/stocks/articles/cybersecurity-stocks-slide-ai-financing-165659411.html) · [247WallSt 資安](https://247wallst.com/investing/2026/10/16/cybersecurity-stocks-slide-as-ai-financing-jitters-spread-palo-alto-falls-7-sentinelone-sinks-9-zscaler-drops-6/) · [TIKR PANW](https://www.tikr.com/blog/palo-alto-networks-fell-nearly-8-a-day-after-citi-raised-its-target-to-440-heres-where-the-stock-could-go-by-2031) · [Motley Fool 資安平台](https://www.fool.com/investing/2026/10/17/as-ai-supercharges-hackers-cybersecurity-stocks-sp/) · [Yahoo GOOGL](https://finance.yahoo.com/markets/stocks/articles/google-price-prediction-bull-bear-180743428.html) · [247WallSt GOOGL](https://247wallst.com/investing/2026/07/10/alphabet-stock-looks-undervalued-after-a-100-rally-in-a-year-analysts-see-more-upside/) · [MarketBeat MTSI](https://www.marketbeat.com/instant-alerts/macom-technology-solutions-q3-earnings-call-highlights-2026-08-06/) · [heygotrade 太空股](https://www.heygotrade.com/en/blog/space-stocks-rklb-asts-lunr-spacex-ipo/) · [Yahoo SpaceX IPO](https://finance.yahoo.com/markets/stocks/articles/spacex-2-trillion-ipo-coming-115204460.html)

---

## 6. QM 動能掃描：Stage 1 變多、Stage 2 幾乎歸零

| | 08-29 | 09-09 | 09-24 | 10-03 | **10-17** |
|---|---:|---:|---:|---:|---:|
| Universe | — | — | — | — | 8,587（本期更新） |
| Stage 1（RS + ADR + 流動性） | — | — | 1,049 | 885 | **1,006** |
| Stage 2（型態候選） | 30 | 13 | 7 | 14 | **4** |
| 觀察名單總數 | 49 | 24 | 9 | 18 | **11** |

**Stage 1 增加、Stage 2 掉到這個系列的最低點**，這兩件事放在一起看才有意義：這週波動大到讓更多股票過了 ADR ≥ 2% 的門檻，但同樣的波動也把緊縮的整理型態全部震散了。**大跌週本來就不會出現 base**，這週的 4 檔候選不代表動能消失，只代表型態還沒來得及形成。

**群聚寬度門檻：** 觀察名單只有 11 檔，**< 25**。Technology 群 5 檔（4 檔台股）**不能**當成主題訊號，依規則也**不能**作為覆蓋池新增的理由。

### 6.1 覆蓋池 × 觀察名單交集

| Ticker | 群組 | 狀態 | 細節 |
|--------|------|------|------|
| **3044 健鼎** | abf | 🔴 **觸發** | 上期距觸發價 547 只差 −0.9%；本期收 **584（+6.8%）**。觸發的這一週，同群的欣興 −14.2%、南電 −8.1%，費半單週 −11.4% |
| AMD | bigtech | ❌ 破線出局 | 跌破 base 低點；5 日 −13.0% |

**健鼎是本週唯一值得記下的 QM 訊號。** 在 SOX 單週 −11% 的環境裡突破，是相對強度最直接的證據。它的客戶以伺服器/網通板和車用為主，在第 2 節的分類裡不屬於 neocloud 融資鏈的直接下游。但只是一次觸發，還要看能不能撐過 5 個交易日的追蹤期。
**AMD 出局不影響覆蓋池。** 依規則，QM 破線不是覆蓋池的退出條件。

### 6.2 其他候選（不在覆蓋池）

- **2357 華碩**：前期漲幅 97%，距區間高點 1,010 差 −1.6%。屬 AI 伺服器/PC 組裝。值得注意的是它和 2382 廣達一樣，這週沒有被賣成 DELL/SMCI 那樣。目前只是一個型態，未跑四道檢查。
- **3014 聯陽**（−1.0%）、**3055 蔚華科**（EP，跳空 +5.8%、2.0× 量，**不在財報窗口內**，催化劑需人工確認）：都是小型台股，沒有新聞面驗證。
- **觸發中的美股**：JOYY、CRVL（保險經紀）、ENGS；CRVL 和 UFCS（產險）兩檔保險股，在第 2 節的框架裡屬於「不需要外部融資」的那一類，但 2 檔遠低於可解讀的寬度。

**上期觸發的追蹤結果：** PD 守住 5 日（held）；IRDM 跌破 base 低點出局，上期那次事件驅動的檢查沒有轉成持續的突破。

**Sources:** `research/2026-10-17-qm-scan.md` · `data/qm/watchlist.json`

---

## 7. 覆蓋池調整建議

**本期不新增、不移除。**

- **新增：無。** QM 觀察名單只有 11 檔，低於 25 檔的群聚門檻；2357 華碩是唯一和覆蓋池主題相關的非覆蓋池候選，但四道檢查還沒跑，不構成新增理由。
- **移除：無。** 本週覆蓋池有 35 檔 5 日跌幅超過 10%，AMD 也在 QM 破線出局，但這些都是價格訊號。依「覆蓋池不因動能訊號移除」原則，賽道本身（AI 基礎建設、記憶體、光通訊、電力）的產業論點沒有被證偽；**這週公布的基本面（台積電、ASML、鴻海、廣達）反而是上修的**。
- **3044 健鼎** 已在 abf 群，本期觸發，下期追蹤能否守住 5 日。

**待追蹤項：**
- **新判準（本期建立）：「客戶的錢從哪來」是和「久期」並列的第二個軸。** 久期回答「利率上升時誰受傷」，資金來源回答「信用利差擴大時誰受傷」。兩個軸在 9 月同向（殖利率和信用利差一起惡化），這週第一次分開，所以才看得出來。之後判讀覆蓋池分化時兩個都要量。
- `ram` 群拆成三種瓶頸敘事：MU（HBM 長約）/ WDC（HDD，東芝擴產）/ 2408・2344（標準型 DRAM，長鑫 4F²）。
- `power` 群：BE 的 Brookfield JV 關係人營收——這週是這個風險第一次被市場定價。下次 BE 財報要特別看非關係人營收的比重。
- `aiinfra` / `abf`：DELL 和 SMCI 的 neocloud 客戶佔比。若財報有揭露，這是判斷信用風險傳導程度的關鍵數字。
- 量化分在價格大跌後會機械性上升（本週 BUY 從 30 → 40 檔），下期判讀時要先問「分數上升是因為基本面變好，還是價格變低」。

---

## 8. 下週觀察清單

| 日期 | 事件 | 為什麼重要 |
|------|------|-----------|
| 持續 | **CoreWeave 債券殖利率 / CDS** | 本週的起火點；高收益債市場對 AI 資料中心的發債窗口是否關上 |
| 10/27–28 | FOMC | CPI 偏熱後升息機率回到約 15%；聲明對 12 月的措辭 |
| 10 月底 | MSFT / GOOGL / META / AMZN Q3 財報 | **2027 capex 指引是否維持**——這是第 2.1 節整條需求鏈的源頭；若 hyperscaler 不縮，neocloud 的信用問題就只是局部問題 |
| 年底 | 長鑫 4F² DDR5 RDIMM 實際推出 | 是否公布良率、容量、客戶認證 |
| 11 月底 | DELL Q3 FY27 財報 | AI 訂單、backlog、neocloud 客戶比重 |
| 持續 | 10Y 殖利率 | 這週回落到約 5%；若信用利差收斂而殖利率維持，久期資產（SMR/OKLO/FSLR）才有反彈的條件 |

---

## ⚠️ 限制

- yfinance 資料延遲 15–20 分鐘；本期覆蓋池收盤價為 **2026-10-16**
- 量化分數不含法說指引與管理層達標紀錄；本報告的這兩個維度全部來自網路搜尋
- CoreWeave 債務規模各來源從 $356 億（Q2 末本金）到 $500 億以上（含承諾，10/15）不等，口徑不同
- 國防四檔本週上漲**未找到單一催化劑**，第 2 節的解釋是推論
- DELL 的 neocloud 客戶佔比為公開報導的定性描述，未取得精確比例
- 不構成投資建議
