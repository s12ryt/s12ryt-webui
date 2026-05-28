# Components：資料可視化監控

## Metric Card

包含：

- label
- value
- unit
- delta
- sparkline 或小圖示
- comparison note
- status badge

狀態：

- normal
- warning
- critical
- loading
- stale
- no data

規則：

- value 是視覺焦點。
- delta 必須說明比較基準，例如「vs last 24h」。
- 若資料過期，value 不可看起來像即時資料。

## Chart Container

結構：

1. Header：圖表名、說明、時間範圍、操作。
2. Content：圖表本體。
3. Legend：固定顏色與分類。
4. Footer：數據來源、last updated、註解。

狀態：

- loading skeleton
- empty data
- partial data
- error
- stale

規則：

- 每個圖表只回答一個主要問題。
- Tooltip 需完整顯示單位與時間。
- 圖表錯誤不應讓整個 dashboard 崩壞。

## Alert Card

包含：

- severity badge
- alert title
- affected service / region
- started time
- current status
- suggested action
- owner / assignee

狀態：

- open
- acknowledged
- investigating
- mitigated
- resolved
- false positive

規則：

- Critical alert 必須高於一般資料卡。
- 已確認與已解決狀態不可混淆。
- CTA 要清楚，例如「查看事件」、「指派處理」、「靜音」。

## Incident Timeline

用途：incident、release、uptime、審計紀錄。

每個節點需有：

- timestamp
- event type
- summary
- actor / source
- impact
- linked artifact

規則：

- 時間排序需明確。
- 目前事件可高亮。
- 長 timeline 支援收合與篩選。

## Filters

常見篩選：

- date range
- environment
- region
- service
- severity
- owner
- status

規則：

- 高頻篩選放工具列。
- 低頻篩選放 drawer。
- active filter 要可一鍵移除。
- Filter 改變時顯示 loading 或更新狀態。

## Data Table

功能：

- sticky header
- sorting
- filtering
- column visibility
- row action
- pagination 或 virtual scroll

規則：

- 長字串截斷並提供 tooltip。
- 數字欄位右對齊。
- 狀態欄位使用 badge + 文字。
- 危險行動不可只放 icon，需有 label 或 tooltip。

## Service Health Card

包含：

- service name
- uptime
- latency
- error rate
- current status
- last incident

規則：

- 適合放在 service overview。
- 點擊可進入 service detail。
- status 與 KPI 需一致。

## Log Row / Log Viewer

包含：

- timestamp
- level
- source
- message
- trace id
- action

規則：

- 使用 monospace。
- 支援 level filter 與搜尋。
- Error row 可展開 stack trace。
- 大量 log 需使用 virtualized list。

## Refresh State

必備顯示：

- last updated
- auto refresh interval
- manual refresh button
- stale warning
- refresh failed alert

規則：

- 手動刷新時按鈕 loading。
- 自動刷新不應打斷使用者正在查看 tooltip 或選取文字。

## Export Menu

選項：

- CSV
- JSON
- PNG
- PDF report
- share link

規則：

- 匯出前顯示目前時間範圍與 filter。
- 大量資料匯出需進入 background job 狀態。

## Empty State

場景：

- 尚無資料。
- 篩選條件無結果。
- 尚未設定服務。
- 權限不足。

規則：

- 必須說明原因與下一步。
- 不要把 no data 誤顯示成 0。
