# 2026-10-23 週報 — 自己的錢夠不夠：現金流轉負的那一刻，營收再好也沒用

**涵蓋期間：** 2026-10-19 ~ 2026-10-23（美股收盤；台股資料只到 10/22，見限制）
**資料來源：** QM 全市場掃描（bigcap）+ 覆蓋池 76 檔量化（含 `--vol` 選擇權收租排名）+ 約 30 則產業 / 法說 / 分析師搜尋
**前情：** [2026-10-17 週報](2026-10-17-weekly-report.md) 提出「客戶的錢從哪來」這個判準；[2026-10-22 週中更新](2026-10-22-midweek-option-income.md) 第一次跑選擇權收租章節。

---

## 0. 本週三個結論

1. **判準再往上推一層：上週問的是「客戶的錢從哪來」，這週連付錢的人自己都開始缺錢。** META 營收 $646 億、年增 26%，優於預期，但**單季自由現金流 −$21 億**（去年同期 +$106 億），2026 年 capex 下限再上調到 $1,350 億，今年沒有買回任何一股，還宣布發行**無投票權的 Class C 股，公司寫明用途是「替成長融資」**。股價 −7%，5 年期 CDS 創歷史新高。上週表格裡 META 被歸在「自己就是付錢的人」那一類，這個分類本週已經不成立（第 2 節）。

2. **市場現在懲罰的是「燒錢」，不是「沒達標」。** BE 交出營收年增 138%、全年指引從 $39–42 億上調到 $44–46 億，隔天卻 **−11.2%**，原因是營運現金流轉負（−$2,700 萬），自由現金流約 −$1.8 億。LRCX 財報與指引都略優於預期，盤後 −6~7%；WDC 下季營收指引年增 66–72%，遠高於共識，股價也只換到 −3%。同一週，**資安 SaaS 從上週的 −18% 反彈 +10~14%**。上週被賣的是「需要外部融資的成長股」，這週被買回的是「自有現金流、而且有短期需求催化劑的軟體」。

3. **QM 觀察名單回到 31 檔，越過 25 檔的群聚門檻，但裡面沒有一檔是覆蓋池的主題。** 這 31 檔裡沒有台股，也沒有 AI 供應鏈的名字：醫療 7 檔、產險 / 區域銀行 5 檔、能源 4 檔，外加兩檔電塔 REIT 的 EP。動能資金從我們追的賽道撤出，換到防禦型和油價受惠的名字。醫療群聚是**數月來第一次通過寬度門檻的群聚**，依規則只能作為「值得跑四道」的候選，**不構成覆蓋池新增理由**（第 5 節）。

---

## 1. 宏觀：Brent $116、VIX 破 20、12 月升息機率約 75%

| 項目 | 上期 (10/16) | 本期 (10/23) |
|------|------------|-------------|
| S&P 500 單週 | 約 −2% | **−0.5%**（收 7,623.68） |
| Nasdaq 單週 | −4% 以上 | **−0.7%**（收 25,955.34） |
| Dow 單週 | +0.7% | **+0.4%**（週五單日 −653 點） |
| Brent | 高檔震盪 | **$116.72**，6 個月高點，單週 +6.2%，連三週上漲 |
| VIX | — | 6 月以來**首度收在 20 以上** |
| 10Y 殖利率 | 約 5.0% | 約 **5.1%** |
| 12 月升息機率 | — | 約 **75%**（10 月 FOMC 按兵不動的機率約 85%；**只有單一來源**） |

- **油價是本週新增的變數。** Houthi 攻擊沙烏地境內目標，市場也開始預期美國在未來幾週恢復對伊朗的空襲；美伊戰爭已進入第 9 個月，Brent 今年漲了 85% 以上。油價推升通膨，通膨推升升息機率，結果又回到上兩期「折現率」的那條線。
- **週五 Dow 跌得比 Nasdaq 多**，有評論形容這是投資人「從科技股和資料中心受惠股全力衝向安全資產」。但從覆蓋池看，週五資安股大漲、AI 電力股大跌，所以比較準確的說法是**資金在挑「現金流」，而不是單純避險**。
- **台股：** 外資 10 月累計賣超約 **6,621 億台幣**（10/20 當天賣超 795 億）。期貨未平倉淨空單約 9.2 萬口。

**Sources:** [CNBC 10/23](https://www.cnbc.com/2026/10/22/stock-market-today-live-update.html) · [Yahoo 10/23](https://finance.yahoo.com/markets/live/stock-market-today-friday-october-23-dow-sp-500-nasdaq-tesla-meta-093000521.html) · [CNBC 原油](https://www.cnbc.com/2026/10/23/oil-price-brent-wti-iran-war-saudi-arabia.html) · [Globe and Mail 原油](https://www.theglobeandmail.com/investing/article-brent-crude-hits-more-than-five-month-high-on-concern-over-middle-east/) · [Trading Economics 10Y](https://tradingeconomics.com/united-states/government-bond-yield/news/593147) · [Focus Taiwan 10/20](https://focustaiwan.tw/business/202610200013) · [investingLive](https://investinglive.com/stocks/dow-leads-stocks-lower-small-caps-win-the-week/)

---

## 2. 本週最重要的觀察：hyperscaler 從「付錢的人」變成「找錢的人」

上週把覆蓋池按「客戶的錢從哪來」分組，最穩的一層是「自有現金流的 hyperscaler」。這週 META 的財報把這一層打穿了：

| META Q3 2026 | 數字 | 意義 |
|---|---|---|
| 營收 | $646 億，年增 26%（預期約 $633 億） | 廣告本業沒問題 |
| 自由現金流 | **−$21.2 億**（去年同期 +$106 億） | capex 第一次超過營運現金流 |
| 2026 capex 指引 | $1,350–1,450 億（下限原為 $1,300 億） | 有分析師把 2027 年 capex 估到 **$2,490 億** |
| 2026 年買回 | **0**（去年同期 $262 億） | 現金全部投入 capex |
| Class C 無投票權股 | 2027/1/19 生效，每股配 1 股 | 公司列出的用途：**融資、員工薪酬、併購** |
| 5 年期 CDS | 歷史新高 | 信用市場開始替 hyperscaler 定價 |

**Class C 股為什麼重要：** 表面上像是一拆二，實質上是替 Zuckerberg 保留控制權、又能發新股募資的工具（和 Google 2014 年的做法一樣）。XTB 的判讀是：**AI 投資規模已經超過單靠獲利能支撐的範圍，發新股是現實選項。** 這是上週第 2.1 節 Epoch AI 那個預估（hyperscaler 現金 capex 約在 2026 Q3 超過營運現金流）第一次在單一公司的財報上被驗證。

**對覆蓋池需求鏈的意義，分兩面看：**

- **短期是利多：** META 沒有縮減 capex，反而上調下限。上週觀察清單的第一個問題是「hyperscaler 的 2027 capex 會不會縮」，**META 的答案是不會**。對 NVDA、ANET、光通訊、記憶體來說，訂單端沒有變化。
- **中期是新的單點故障：** 需求鏈的源頭從「hyperscaler 用自己的現金流付錢」，變成「hyperscaler 用發債 + 發股付錢」。這代表上游的訂單**開始和資本市場的開放程度綁在一起**——而這正是上週 CoreWeave 那條線的邏輯，只是現在往上延伸到了投資等級的公司。CoreWeave 和 IREN 週四再創 2026 年新低，CoreWeave 2032 年到期債殖利率仍在 15% 附近。

**本週覆蓋池 5 日表現，按「現金流狀態」重新分組：**

| 現金流狀態 | 代表 | 5 日 % | 判讀 |
|---|---|---:|---|
| **剛轉負 / 還在燒錢** | META / BE / OKLO / SMR | **−9.4 / −12.7 / −5.8 / −7.7** | BE 和 META 都是財報後才跌 |
| **自有現金流 + 需求催化劑** | CRWD / OKTA / PANW / NET / NOW | **+13.3 / +13.8 / +11.3 / +9.9 / +12.0** | 上週 −17~−19%，本週收回大半 |
| **政府預算** | LMT / NOC / GD / RTX | +9.4 / +6.1 / +1.5 / −1.5 | 連兩週相對強勢 |
| **財報在下週、市場先賣** | FN / AAOI / COHR / LITE | **−13.4 / −10.7 / −10.1 / −8.2** | 財報都在 11/2–11/5，連跌第二週 |
| **剛交出 beat-and-raise** | WDC / MU | +3.5 / −0.1 | 有交出成績的守得住，但也沒被獎勵 |
| **台股供應鏈（至 10/22）** | 2327 / 2472 / 6488 / 2408 / 3260 | −10.6 / −10.4 / −8.4 / −7.5 / −8.9 | 外資持續賣超，與基本面新聞無關 |

**資安反彈的原因是兩個具體事件**，不是單純的資金輪動：(1) 10/21 PHP 專案揭露兩個由 AI 找到的重大漏洞，PANW CEO 說接下來還會有更多；(2) Evercore ISI 的通路調查顯示年底資安預算轉強，點名 CRWD、PANW 是 AI 資安支出的主要受惠者。**這是一週的價格反應，還沒有反映在財報上**。

**Sources:** [CNBC META FCF](https://www.cnbc.com/2026/10/22/meta-stock-q3-earnings-free-cash-flow.html) · [BusinessToday META](https://www.businesstoday.in/markets/stocks/story/meta-shares-slide-7-as-ai-spending-push-drives-capex-higher-free-cash-flow-turns-negative-563170-2026-10-22) · [XTB META](https://www.xtb.com/int/market-analysis/news-and-research/record-breaking-meta-though-with-a-cash-loss-investors-for-now-are-buying-zuckerberg-s-plan-anyway) · [Crypto Briefing Class C](https://cryptobriefing.com/meta-raises-capex-nonvoting-class-c-stock/) · [Benzinga META 目標價](https://www.benzinga.com/analyst-stock-ratings/price-target/26/10/62543931/meta-analysts-revise-price-target-after-q3-core-ad-strength-muse-concerns-remain) · [CNBC 信用 vs 股票](https://www.cnbc.com/2026/10/19/coreweave-oracle-ai-credit-stress.html) · [Yahoo 資安 Evercore](https://finance.yahoo.com/markets/stocks/articles/crowdstrike-palo-alto-rally-evercore-182853152.html) · [Investing.com 資安](https://investing.com/news/stock-market-news/aipowered-cyber-threats-light-a-fire-under-cybersecurity-stocks-4970021) · [TipRanks PHP 漏洞](https://www.tipranks.com/news/cybersecurity-stocks-rally-as-web-code-flaws-spark-global-frenzy-crwd-jumps-6-panw-rises-4)

---

## 3. 財報季第一週：覆蓋池相關的四份財報

### 3.1 BE — beat-and-raise 之後 −11%，上週標記的風險換了一種形式出現

- **成績：** 營收 $12.36 億（年增 138%）、產品營收年增 179%、毛利率 33.8%（+453bp）。調整後 EPS $0.94，預期 $0.69。全年營收指引上調到 $44–46 億，EPS 指引 $3.10–3.40。12 月前產能倍增到 2GW，同時納入 S&P 500。
- **為什麼跌：** 營運現金流 −$2,700 萬，擴產 capex 跳升，自由現金流約 −$1.8 億。股價過去一年翻倍，市場預期本來就跑在財報前面。
- **管理層紀錄：** 9/11 加入覆蓋池時的紀錄是 4 季全數 beat-and-raise，這季延續（量化工具的 EPS beats 計為 3/4，口徑不同）。**BE 的問題不在執行力。**
- **和上週的連結：** 上週把 BE 歸在「自己還要融資的電力」，風險點是 Brookfield JV 的關係人營收。這季的現金流轉負是同一個問題的另一面：**營收在成長，但現金還沒收回來**。在信用利差敏感的環境裡，這是市場最不願意承擔的組合。
- **分析師：** Morgan Stanley 目標價從 $310 上調到 $335，維持 Overweight；KeyBanc 維持 Sector Weight。

### 3.2 WDC — 本週覆蓋池量化第一名，財報驗證了「HDD 是 AI 儲存瓶頸」

- 營收 $43.8 億（年增 55%），**高於公司 8 月自己給的指引中值約 $2.8 億**；非 GAAP 毛利率 58.1%（指引 55.5%）、EPS $4.64（指引 $4.00）。
- **下季指引：營收年增 66–72%**。用去年同期 $30.2 億推算約 **$50–52 億**（這是我的推算，不是公司給的數字），財報前的共識是 $45.1 億。
- 淨現金 $5 億，當季買回 $10 億。**現金流是正的**，這是它和 BE 最大的差別。
- 8 月法說提到：40TB ePMR 開始量產，44TB HAMR 預計 2027 上半年出貨；hyperscale 資料中心 80% 以上的資料仍存在 HDD 上。
- **管理層紀錄：** 這季對自己的指引全面超標，屬於保守給指引（sandbagging）的類型。
- 股價只換到週五 −3%、5 日 +3.5%。8 月那次也是財報超標、股價下跌，年初至今漲了兩倍，**市場對它的預期已經很高**。

### 3.3 LRCX（不在覆蓋池，但它是記憶體 / 晶圓廠 capex 的溫度計）

- 營收 $82.2 億、EPS $2.20，略優於預期 $81.3 億 / $2.18；營業利益率首度突破 40%。12 月季指引 $86 億 ± $4 億，略高於共識 $85.3 億。
- 盤後 −6~7%。XTB 的說法是「投資人在等一個更強的催化劑」。**設備端沒有轉弱的跡象**，這和上週 ASML「2027–2028 EUV 供不應求」的訊息一致。

### 3.4 META — 見第 2 節。量化分數掉到 **0%**

EPS 驚喜 −29.9%（不同來源的共識數字差異很大，$3.57 到 $5.75 都有，可比性存疑）、分析師分項和動能分項同時下滑。**這是價格訊號加上一次性的 EPS 比較問題**，廣告本業（營收年增 26%）並沒有轉弱。依「覆蓋池不因量化 / 動能訊號移除」原則，META 留在 bigtech 群。

**Sources:** [BE 8-K](https://www.sec.gov/Archives/edgar/data/0001664703/000162828026066890/ex991_q326financialresults.htm) · [Motley Fool BE](https://www.fool.com/investing/2026/10/23/bloom-energy-stock-sinks-despite-record-revenue-and-a-stellar-outlook-is-it-time-to-buy/) · [TheStreet BE](https://www.thestreet.com/investing/stocks/another-ai-power-stock-plunges-11-despite-earnings-beat-bloom-energy-be) · [The Crypto Basic BE 現金流](https://thecryptobasic.com/2026/10/23/bloom-energy-stock-falls-despite-q3-earnings-beat-as-operating-cash-flow-turns-negative/) · [WDC 8-K](https://www.sec.gov/Archives/edgar/data/0000106040/000162828026066882/a4ex991-pressreleaseq127.htm) · [Benzinga WDC 共識](https://www.benzinga.com/quote/WDC/earnings-forecasts) · [Investing.com LRCX](https://www.investing.com/news/earnings/lam-research-tops-firstquarter-targets-and-issues-upbeat-guidance-stock-falls-4963987) · [XTB LRCX](https://www.xtb.com/int/market-analysis/news-and-research/lam-research-strong-numbers-limited-upside-surprise) · [Morningstar LRCX](https://www.morningstar.com/stocks/lam-research-earnings-focus-fundamentals)

---

## 4. 各產業簡評

| 群組 | 本週重點 | 論點狀態 |
|------|---------|---------|
| **bigtech** | META 現金流轉負 + Class C；GOOGL / MSFT 下週 10/28 財報 | 需求端沒有縮，但**融資方式在改變**。下週 GOOGL、MSFT 的自由現金流比 capex 數字更重要 |
| **ram** | WDC beat-and-raise；TrendForce 預估 Q4 DRAM 合約價季增約 **20%**（Q2 約 80%、Q3 約 40%） | **漲幅收斂但仍在漲**。收斂的原因是基期高、買方購買力轉弱、長約價格上限開始生效。HBM 4 的 2027 年合約談判 Q2 已開始，預期大幅漲價。排序維持 MU / WDC > 2408 / 2344 |
| **tw** | 外資 10 月累計賣超約 6,600 億 | 本週沒有新的基本面消息，只有資金面 |
| **aiinfra** | VRT 10/28 財報（IV/HV 1.45）；ANET 11/3 | ANET 的多空：多方看 AI 網通（2026 年 AI 營收至少 $36 億），空方看毛利率被記憶體成本壓縮（指引 62–63%）和 CEO 4 月減持 |
| **saas** | 資安 +10~14%；NOW +12% | 見第 2 節。CRM 被量化評為 BUY（38%），屬於「空方論點已經被定價」的那一類 |
| **optics** | 連跌第二週，財報 11/2–11/5 | 產業面沒有變：Coherent 資料中心 book-to-bill 超過 4 倍，CY2026 已排滿；1.6T 用的 200G EML 單價約是 800G 用的 2 倍。**FN 的空方重點是客戶集中**（Cisco 20%、NVDA 11%、AMZN 11%）和庫存年增 76% |
| **power** | BE −11%（見 3.1） | CEG / VST 下跌 6–8%，主因是升息預期回升，而不是基本面 |
| **leo** | ASTS：Piper 降評到 Neutral，10/29 FCC 會議 | 事件驅動，沒有新的產業消息 |
| **defense** | RTX Q3 營收 $250 億（年增 11%），上調全年指引，backlog 達 **$3,400 億**；NOC 營收 $111 億（年增 7%） | 連兩週相對強勢；油價和中東情勢是額外的支撐 |
| **passives / siwafer** | 5 日 −3% 到 −11%（至 10/22） | 沒有新的價格新聞，最近一次確認的是 7–8 月的漲價（國巨約 50%、三星電機 30%）。下跌是資金面 |
| **health** | ALKS +5.8%、PGNY +7.9% | 和 QM 的醫療群聚同方向（第 5 節） |
| **fins** | OWL 週五 −3.6% | 私募信貸贖回壓力是 OWL 年初以來的老問題；在「信用利差」為主軸的環境裡，這一群要繼續追蹤 |

**Sources:** [StockHub / TrendForce Q4 DRAM](https://www.stockhub.kr/en/news/news_b7244c205001) · [TrendForce HBM](https://www.trendforce.com/research/download/RP260527UC) · [Simply Wall St / tikr ANET](https://www.tikr.com/blog/arista-networks-is-up-230-in-three-years-and-analysts-see-140-more) · [MarketBeat FN](https://www.marketbeat.com/articles/fabrinets-sell-off-may-prove-it-is-one-of-ais-most-misunderstood-stocks/) · [Panabee FN](https://www.panabee.com/news/fabrinet-earnings-q2-2026) · [Yahoo 光通訊](https://finance.yahoo.com/markets/stocks/articles/applied-optoelectronics-rips-24-lumentum-155212285.html) · [Finviz 國防](https://finviz.com/news/405352/defense-earnings-week-opens-with-three-raised-forecasts-and-two-record-backlogs) · [tikr ASTS](https://www.tikr.com/de/blog/ast-spacemobile-lost-18-in-a-week-roth-mkm-says-it-could-more-than-double) · [TrendForce MLCC](https://www.trendforce.com/news/2026/08/04/news-across-the-board-30-price-hike-mlcc-price-surge-intensifies/) · [TrendSpider OWL](https://trendspider.com/blog/owl-stock-slides-as-blue-owl-limits-redemptions-on-credit-funds/)

---

## 5. QM 動能掃描：觀察名單回到 31 檔，但全是「別的賽道」

| | 09-24 | 10-03 | 10-17 | 10-22（週中） | **10-23** |
|---|---:|---:|---:|---:|---:|
| Stage 1 | 1,049 | 885 | 1,006 | 998 | **986** |
| Stage 2 候選 | 7 | 14 | 4 | 12 | **17**（突破 11、EP 6） |
| 觀察名單總數 | 9 | 18 | 11 | — | **31** |

**觀察名單依產業：** Healthcare 7、Financial Services 5、Industrials 4、Energy 4、Communication 3，其餘各 2。**台股 0 檔、AI 供應鏈 0 檔。**

### 5.1 群聚判讀（≥ 25 檔，可解讀）

- **醫療（7 檔）：** ABBV、MDT 這種大型防禦股，加上 PNTG（照護機構）、WAY / CERT（醫療資訊）、ROIV / ZLAB（生技 EP）。**這是 9 月建立寬度門檻以來第一次通過門檻的群聚。** 覆蓋池的 health 群（ALKS / PGNY / LNTH）本週也同步走強。
- **產險 / 區域銀行（5 檔，4 檔已觸發）：** UFCS、UVE（產險）、CRVL（保險經紀）、CFFI / CIB（銀行）。上週提過 CRVL、UFCS 屬於「不需要外部融資」的類型，這週變成 5 檔。**和覆蓋池的 fins 群（券商、資產管理）是不同的生意**，fins 群本週並沒有跟著走強。
- **能源（4 檔）：** PBR 觸發、KNTK / DEC 待觸發，和 Brent $116 一致。
- **電塔 REIT EP：** CCI 跳空 +15.5%（3.0 倍量，10/21 財報後）、AMT +10.5%（2.5 倍量，**AMT 自己的財報在 10/27**，這次跳空應是跟著 CCI 的財報，催化劑未經新聞確認）。

**整體讀法：** 這是一張**「現金流穩定、和 AI 資本支出無關」的名單**，和第 2 節的結論同方向。依 9/24 建立的原則，**動能訊號對「這條賽道值不值得看」沒有發言權，兩個方向都沒有**：AI 賽道不會因為 QM 名單裡沒有它就被移出覆蓋池，醫療也不會因為群聚通過門檻就被加進來。

### 5.2 覆蓋池 × 觀察名單交集

**本週交集為零**，這個系列以來第一次。上週觸發的 **3044 健鼎** 在 5 日追蹤期內轉為 `faded`（收 556，仍在觸發價 547 之上，但沒有延續）；AMD 上週已經破線出局。

### 5.3 候選觀察

- **ABBV**（距觸發 −2.0%，前期漲幅 41%）、**MDT**（−1.5%，22%）：如果醫療群聚持續兩週以上，這兩檔是最適合跑四道、評估能不能放進 health 群的大型股。本週**沒有跑四道**。
- **PD**（前期漲幅 98%，距觸發 −0.3%）：上上期觸發後守住 5 日，現在形成第二個 base。
- **觸發中：** JOYY、CRVL（+10.4%）、ENGS（+38.8%）、CERT、UFCS、PBR、CFFI、UVE、EXPO。
- **踢出：** SPHL（EP 回補）、ECPG（跌破 base 低點）。

**Sources:** `research/2026-10-23-qm-scan.md` · `data/qm/watchlist.json`

---

## 6. 覆蓋池量化排序（BUY ≥ 45%）

| 代號 | 群組 | 分數 | EPS 驚喜 | Beats | 營收成長 | 分析師目標價空間 | 5 日 % |
|------|------|-----|---------|-------|---------|---------------|------:|
| **WDC** | ram | **55%** | +13.2% | 3/4 | +43.8% | +85.1% (24) | +3.5 |
| BE | power | 53% | +38.2% | 3/4 | +165.5% | +47.1% (26) | −12.7 |
| FN | optics | 52% | +7.6% | 3/4 | +44.6% | +118.4% (9) | −13.4 |
| ANET | aiinfra | 52% | +14.6% | 3/4 | +37.7% | +41.3% (29) | −2.6 |
| 2408.TW | ram | 50% | +8.8% | 3/4 | +611.7% | +48.6% (14) | −7.5 |
| ALKS | health | 50% | +141.4% | 3/4 | +27.0% | +28.8% (19) | +5.8 |
| PL | leo | 50% | +200% | 2/4 | +58.1% | +125.7% (11) | −1.1 |
| VRT | aiinfra | 49% | +6.3% | 3/4 | +24.1% | +71.4% (28) | −5.9 |
| DELL | aiinfra | 49% | +43.1% | 3/4 | +57.7% | +29.9% (25) | +1.2 |
| 3037.TW | abf | 49% | +140.1% | 3/4 | +32.1% | +24.2% (19) | −0.5 |
| GOOGL | bigtech | 48% | +214% | 3/4 | +24.2% | +34.0% (54) | −6.0 |
| 2303.TW | tw | 48% | +203.6% | 2/4 | +17.0% | +16.1% (25) | −5.6 |
| MU | ram | 48% | +5.0% | 3/4 | +379% | +78.0% (45) | −0.1 |
| 2382.TW | tw | 47% | +15.9% | 3/4 | +105.6% | +33.5% (19) | 0.0 |

**讀表提醒（延續上週）：** FN、2408、VRT 的分數上升有一部分是**價格下跌讓目標價空間機械性變大**。WDC 是表上少數「分數上升 + 剛交出 beat-and-raise + 股價沒有大跌」三者同時成立的名字，**這週的分數最可信**。

**估值（次要）：** WDC Fwd P/E 8.7x、MU 4.2x、2408 3.5x——記憶體 / 儲存的低本益比是市場在定價「週期頂點」，不是便宜，這點和過去幾期的判讀一致。ANET 33x、BE 39x 相對偏高。

---

## 💵 選擇權收租候選

> 篩選邏輯：量化分數 × 年化權利金殖利率（30Δ、約 28 天到期，11/20）。
> 只列「看好、而且波動大到權利金值得收」的名字。非投資建議。
> 美股殖利率由選擇權鏈 ATM 價格反推 IV 後，以 Black-Scholes 估算（本週美股全部 `SRC = IV`，沒有 HV 代替值）。收盤後沒有可用的 bid/ask mid 價，實際成交價可能差幾個百分點。

| 代號 | 策略 | 量化分數 | IV | IV/HV | 30Δ 履約價（現價） | 年化殖利率 | 備註 |
|------|------|---------|----|------|------------------|-----------|------|
| **WDC** | Sell Put | 55% | 67% | 0.95 | 320（343.67，−6.9%） | **60%** | **首選**：財報 10/22 已過，下季指引遠高於共識，現金流為正、當季買回 $10 億。HDD 是 Seagate / WDC / Toshiba 三家寡占，被指派也願意長抱 |
| **MU** | Sell Put | 48% | 54% | 1.08 | 820（877.55，−6.6%） | 43% | 次選，延續週中更新的判斷：HBM 長約鎖到 CY2027，財報 12/23 晚於到期日。HV%ile 只有 7，波動處在一年低檔，權利金比週中薄 |
| **CRM** | Sell Put | 38% | 43% | **1.33 💰** | 240（248.57，−3.4%） | 42% | 💰 本週唯一「權利金偏貴 + 到期前沒有財報」的美股（財報 12/2）。屬於「SaaSpocalypse 已經被定價」那一類，Fwd P/E 15.5x。**30Δ 履約價離現價只有 3.4%**，被指派的機率比其他幾檔高 |
| SNOW | Sell Put | 35% | 54% | 0.97 | 310（325.43） | 50% | 財報 12/2。分數剛好過 BUY 門檻，Fwd P/E 108x，只適合小部位 |
| PL | Sell Put | 50% | 72% | 1.05 | 12（13.41） | 46% | 營收年增 58%，但營業利益率還是 −12%，屬於小型股。**被指派的話要能接受它還在虧損**，降級為小部位 |
| 3026.TW 禾伸堂 | Sell Put | 43% | 78%（HV） | — | 690（756） | 64% | **理論值，實際成交可能差很多**：台灣個股選擇權流動性低。被動元件的漲價循環仍在，這週的下跌是資金面 |

**本週重點：** **WDC 是本週最乾淨的收租標的**——量化第一、財報剛過（沒有跳空風險）、下季指引大幅超出共識、現金流為正。這三件事加在一起，正好是第 2 節說的「市場現在願意付錢的條件」。在履約價 320 被指派，等於用比財報前更低的價格買進一家剛上修指引的公司。

**分數高但刻意降級：**
- **BE（分數 53%、殖利率 66%、財報已過）**：殖利率和財報時點都符合條件，但這季**自由現金流約 −$1.8 億**，而且它的成長有一部分來自 Brookfield JV 這條融資鏈。上週的結論是「信用利差擴大時誰受傷」，BE 正好在答案裡。IV（80%）還低於 HV20（95%），權利金也不算偏貴。**不列**。
- **DELL（殖利率 51%、財報 11/27）**：延續週中更新的降級。CoreWeave 週四再創 2026 年新低，neocloud 信用壓力還沒緩解。
- **2408 南亞科（理論殖利率 43%）**：同樣是記憶體曝險，長鑫 4F² 瞄準的正是它的標準型 DDR5。**要做記憶體 Sell Put 就選 MU 或 WDC。**

**財報後再看（⚠E，到期前有財報）：** AAOI（99%）、FN（84%，11/2）、SMCI（79% 💰）、LITE（72%）、APP（80% 💰）、COHR（68%）、HOOD（70% 💰）、DDOG（81% 💰）、MTSI（77%）、**VRT（57% 💰，10/28）**、ANET（48% 💰，11/3）。這幾檔 IV 高是因為財報會跳空。VRT 和 ANET 的 IV/HV 都在 1.2 以上，**財報後如果 IV 沒有完全回落**，可以改賣 12 月到期的合約。

**本週不建議收租：** 2382 廣達（分數 47%，但年化只有 16%，而且有財報）、RTX（21%）、GOOGL / MSFT（29%，而且 10/28 有財報）。這幾檔被排除是因為**沒有權利金**，不是因為不看好。

---

## 7. 覆蓋池調整建議

**本期不新增、不移除。**

- **新增：無。** 醫療群聚通過寬度門檻（31 檔裡有 7 檔），但依規則，群聚只能決定「值得跑四道的候選」。ABBV、MDT 列為下期候選，**連續兩週群聚 + 四道通過**才考慮放進 health 群。
- **移除：無。** META 量化分數 0%、BE 財報後 −11%、光通訊連跌兩週，都是價格或一次性訊號。產業論點（AI capex 沒有縮、HBM / HDD 供不應求、光通訊 2026 年已排滿）**本週沒有被證偽，META 反而上調了 capex**。
- **待追蹤：** fins 群的 OWL / VRTS 量化分只有 11% / 15%，連續多週墊底。fins 群是 8/29 依「金融服務 10 檔群聚」加入的，那次群聚後來被證偽（10 檔 → 1 檔），9/24 才因此訂下寬度門檻。**這一群當初是在新規則之前、沒有跑完四道就加進來的**，建議下期補跑四道，結果再決定要不要保留。這是**基本面的複查**，不是因為 QM 破線。

**判準更新（本期建立）：** 上兩期建立了「久期」（利率上升時誰受傷）和「客戶的錢從哪來」（信用利差擴大時誰受傷）兩個軸。本週加上第三個：**「自己的現金流是正還是負」**。前兩個軸問的是外部環境，第三個軸問的是公司本身。META 和 BE 證明了：在目前的環境裡，**現金流轉負比營收沒達標更容易被懲罰**。

---

## 8. 下週觀察清單

| 日期 | 事件 | 為什麼重要 |
|------|------|-----------|
| 10/27 | AMT 財報 | 本週跟著 CCI 跳空 +10.5%，看自己的財報能不能接住 |
| 10/27–28 | **FOMC** | 12 月升息機率約 75%；聲明裡對油價和通膨的措辭 |
| 10/28 | **GOOGL / MSFT 財報** | 這次重點不是 capex 數字，而是**自由現金流是否還是正的**。如果 GOOGL / MSFT 也轉負，第 2 節的結論就從「一家公司」變成「整個產業」 |
| 10/28 | VRT 財報 | aiinfra 唯一在下週公布的；IV/HV 1.45 |
| 10/29 | ASTS FCC 會議 | leo 群事件 |
| 11/2–11/5 | FN / ANET / COHR / LITE / AAOI / APP 財報 | 光通訊連跌兩週後的第一次基本面檢驗 |
| 持續 | Brent、CoreWeave 債殖利率 | 油價 → 通膨 → 升息機率；CoreWeave → AI 信用窗口 |
| 持續 | QM 醫療群聚 | 連續第二週 ≥ 25 檔且醫療仍居首，就對 ABBV / MDT 跑四道 |

---

## ⚠️ 限制

- **台股 10/23 資料缺漏**：`coverage_moves.py` 的台股 1 日漲跌全為 0.0，判斷是 Yahoo 尚未更新 10/23 的 K 棒。台股 5 日漲跌實際是**至 10/22**，選擇權章節的台股 HV 也是。
- META 的 EPS 共識各來源差異很大（$3.57 到 $5.75），EPS 驚喜 −29.9% 的可比性存疑。
- 12 月升息機率 75% 只有 Trading Economics 一個來源；WDC 下季營收的絕對金額是我依成長率推算的。
- AMT / CCI 的 EP 催化劑沒有經過新聞確認。
- 選擇權殖利率是收盤後以理論價估算，台股是 HV 理論值。
- 不構成投資建議。
