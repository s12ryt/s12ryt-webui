# 方案 05：資料可視化監控

## 定位

適合 NOC、營運儀表板、監控中心、分析平台、即時狀態看板、風險監控、SRE / DevOps 控制台、商業指標追蹤與告警處理系統。核心目標是讓使用者快速理解目前狀態、發現異常、追蹤趨勢並採取行動。

## 設計關鍵字

- 即時
- 精準
- 狀態清楚
- 高密度
- 監控感
- 趨勢可讀
- 異常突出
- 可 drill-down

## 視覺摘要

以資料優先，強調圖表、告警、趨勢與異常。可以是深色也可以是淺色，但狀態色與資訊層級必須非常明確。畫面要讓使用者先看狀態，再看原因，最後能進一步處理。

## 典型使用者

- SRE / DevOps，需要監控服務健康度。
- 營運人員，需要追蹤即時業務指標。
- 管理者，需要看趨勢、異常與報告摘要。
- 風控或安全團隊，需要處理警示與事件。
- 分析師，需要切換時間範圍與匯出資料。

## 適合頁面

- Global overview
- Metrics dashboard
- Alerts center
- Incident timeline
- Service health
- Report view
- Log analytics
- SLA / uptime dashboard
- Business operations dashboard
- Risk monitoring

## 不適合

- 以故事為主的品牌頁。
- 只有單一輸入輸出的簡單工具。
- 過度依賴大圖形裝飾的展示頁。
- 需要低刺激閱讀的文件中心。
- 電商結帳或付款流程。

## 資訊密度

高。需善用 grid、分組、顏色、數字字級、篩選器與 drill-down。高密度不代表混亂，所有元件必須回答明確問題。

## 核心問題

每個監控頁應明確回答：

1. 現在是否正常？
2. 哪裡異常？
3. 異常有多嚴重？
4. 從什麼時候開始？
5. 影響誰或哪些服務？
6. 下一步要做什麼？

## 實作優先順序

1. 先定義 KPI 卡、狀態色、時間範圍與 refresh 規則。
2. 建立圖表 grid、告警面板、事件列表。
3. 補 drill-down、filters、service / region / severity 維度。
4. 補 empty、loading、stale data、partial failure 狀態。
5. 補 export、share、incident action 與報告頁。

## 風格邊界

- 可以使用深色與科技感，但不可犧牲可讀性。
- 狀態色必須有語意，不可純裝飾。
- 不要把所有資訊都變成紅黃綠。
- 不用 emoji 當告警或服務 icon。
