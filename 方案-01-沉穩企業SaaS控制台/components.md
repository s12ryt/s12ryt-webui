# Components：沉穩企業 SaaS 控制台

## Button

- Primary：藍底白字，用於每頁唯一主要行動。
- Secondary：白底灰框，用於次要操作。
- Ghost：透明底，用於表格列操作或工具列。
- Danger：紅色，只用於刪除、停用、撤銷。

尺寸：

- sm：高度 32px，左右 padding 12px。
- md：高度 40px，左右 padding 16px。
- lg：高度 48px，左右 padding 20px。

## Card

- 白底、灰框、輕陰影。
- 標題置頂，右上角可放 action。
- 卡片內資訊需有清楚 label/value。

## Table

- 表頭背景 `#F8FAFC`。
- 列高 52px 起。
- hover row 使用 `#F8FAFC`。
- 狀態用 Badge，不直接改整列顏色。
- 大量操作放在最右欄，使用 icon button + tooltip。

## Badge

- Success：綠色，用於啟用、完成、正常。
- Warning：橘色，用於待處理、即將到期。
- Danger：紅色，用於停用、失敗、風險。
- Neutral：灰色，用於草稿、未知、無資料。

## Form

- label 必須存在。
- helper text 與 error text 不混用。
- error 狀態：紅框、紅色錯誤文字、必要時加 icon。
- 表單送出後需有 loading 與成功/失敗回饋。

## Dialog

- 寬度 480px / 640px / 840px 三種。
- 標題清楚描述動作。
- destructive action 需再次確認。

## Empty State

包含：

1. 簡潔標題。
2. 一句說明。
3. 可行動 CTA。
4. 中性 SVG 插圖或 icon。
