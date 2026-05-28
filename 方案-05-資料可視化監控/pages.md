# Pages：資料可視化監控

## Global Dashboard

用途：提供整體系統或營運狀態總覽。

結構：

1. Header：系統名稱、時間範圍、refresh、export。
2. Status summary：全域健康度、open incidents、SLA。
3. KPI row：核心指標。
4. Main chart area：趨勢與比較。
5. Alerts panel：目前告警。
6. Recent events table：最新事件。
7. Footer notes：資料來源與 last updated。

必要狀態：

- loading
- stale data
- partial failure
- no incidents
- critical incident

## Service Detail

用途：查看單一服務或產品線狀態。

結構：

1. Service summary：狀態、owner、SLO、last deploy。
2. KPI row：uptime、latency、error rate、traffic。
3. Time-series charts：延遲、錯誤、吞吐。
4. Deployment / incident timeline。
5. Logs / traces / drill-down table。
6. Related alerts。

設計重點：

- 圖表時間範圍需同步。
- Deployment marker 應可疊在線圖上。
- 異常時間點需可回到 logs。

## Alerts Center

用途：集中處理告警。

結構：

1. Severity tabs 或 filters。
2. Alert list / table。
3. Alert detail drawer。
4. Affected services。
5. Resolution actions。
6. Audit trail。

必要狀態：

- new alert
- acknowledged
- assigned
- muted
- resolved
- no alerts

## Incident Detail

用途：處理與回顧事件。

結構：

1. Incident header：標題、severity、status、owner。
2. Impact summary：影響範圍、開始時間、目前狀態。
3. Timeline：偵測、確認、處理、緩解、恢復。
4. Metrics around incident。
5. Communication log。
6. Postmortem / action items。

## Report View

用途：週報、月報、營運摘要與管理層檢視。

結構：

1. Report header。
2. Date range and export actions。
3. Executive summary。
4. Charts and comparative tables。
5. Notes and anomalies。
6. Appendix / raw data link。

設計重點：

- 可讀性比即時密度更重要。
- 適合支援淺色模式與 PDF 匯出。

## Log Analytics Page

用途：搜尋、篩選與分析大量 log。

結構：

1. Query bar。
2. Time range picker。
3. Level / source filters。
4. Histogram。
5. Log table。
6. Detail drawer。

必要狀態：

- query running
- timeout
- too many results
- no results
- permission denied

## Business Operations Dashboard

用途：追蹤訂單、收入、轉換、客服、供應鏈等業務指標。

結構：

1. Business KPI row。
2. Funnel / conversion chart。
3. Region / channel comparison。
4. Anomaly list。
5. Action queue。

注意：

- 商業指標與系統指標需要分區。
- 金額、比例、數量需有單位。

## AI 提示模板

```text
建立一個資料可視化監控頁面。主方案使用「方案-05-資料可視化監控」。
請先輸出資訊架構、Design token 使用、元件清單、狀態設計與 RWD 策略，再輸出程式碼。
畫面需有 KPI 卡、圖表分區、告警面板、時間範圍、refresh state、事件列表與 drill-down 入口。
必須包含 loading、stale data、empty、partial failure、critical alert 狀態。
遵守本方案的 design-system.md、components.md 與共用規格/AI輸出契約.md。
不要做成行銷頁、一般表單頁或使用 emoji icon；圖表與狀態色必須有明確語意。
```
