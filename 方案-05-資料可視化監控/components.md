# Components：資料可視化監控

## Metric Card

包含：

- label
- value
- delta
- sparkline 或小圖示
- comparison note

## Chart Container

- 標題區：圖表名、說明、時間範圍、操作。
- 內容區：圖表本體。
- Footer：數據來源、last updated、legend。

## Alert Card

- 嚴重程度 badge。
- 影響範圍。
- 開始時間。
- 建議動作。

## Timeline

- 用於 incident、release、uptime、審計紀錄。
- 每個節點需有時間與事件摘要。

## Filters

- 預設收合或集中在工具列。
- 支援 date range、environment、region、service、severity。

## Data Table

- 支援 sticky header。
- 欄位排序需有視覺狀態。
- 長字串需截斷並提供 tooltip。

## Refresh State

- 自動刷新與手動刷新都要顯示。
- 顯示 last updated。
- 資料陳舊時要有提示。
