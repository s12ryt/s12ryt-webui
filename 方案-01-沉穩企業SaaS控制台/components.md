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

規則：

- loading 時保留按鈕寬度，避免 layout shift。
- danger 操作文案要明確，例如「刪除此團隊」。
- icon button 需要 tooltip 與 aria-label。

## App Shell

包含：

1. Sidebar：主功能導覽。
2. Top bar：搜尋、通知、帳號、環境切換。
3. Breadcrumb：深層頁面必備。
4. Content container：頁面內容。

規則：

- Sidebar active 狀態清楚。
- 收合 sidebar 不可讓 icon 無說明。
- 手機版 sidebar 改 drawer。

## Card

- 白底、灰框、輕陰影。
- 標題置頂，右上角可放 action。
- 卡片內資訊需有清楚 label/value。
- KPI card 顯示 label、value、delta、comparison note。

狀態：loading、empty、error、disabled。

## Data Table

必備能力：

- Sticky header。
- Sorting。
- Filtering。
- Pagination。
- Row selection。
- Column visibility（可選）。
- Empty / loading / error。

規則：

- 表頭背景 `#F8FAFC`。
- 列高 52px 起。
- hover row 使用 `#F8FAFC`。
- 狀態用 Badge，不直接改整列顏色。
- 大量操作放在最右欄，使用 icon button + tooltip。
- 長文字截斷需提供 tooltip 或 detail drawer。

## Filter Bar

包含：

- 搜尋。
- 狀態下拉。
- 日期範圍。
- 更多篩選。
- 已套用篩選 chip。

規則：

- 篩選後需顯示結果數。
- 空結果提供清除篩選。
- 手機版可改成 filter drawer。

## Badge

- Success：綠色，用於啟用、完成、正常。
- Warning：橘色，用於待處理、即將到期。
- Danger：紅色，用於停用、失敗、風險。
- Info：藍綠色，用於處理中、同步中。
- Neutral：灰色，用於草稿、未知、無資料。

Badge 必須有文字，不只顯示色點。

## Form

- label 必須存在。
- helper text 與 error text 不混用。
- error 狀態：紅框、紅色錯誤文字、必要時加 icon。
- 表單送出後需有 loading 與成功/失敗回饋。
- 多欄表單在手機改單欄。

## Dialog / Drawer

Dialog 用於短流程確認；Drawer 用於查看/編輯列表項目。

尺寸：

- Dialog：480px / 640px / 840px。
- Drawer：420px / 560px / 720px。

規則：

- 標題清楚描述動作。
- destructive action 需再次確認。
- 關閉前若有未儲存變更需提示。

## Tabs

- 用於 detail page：概覽、設定、成員、紀錄。
- active 狀態使用 primary underline 或 soft background。
- 不要在一頁內使用多層 tabs。

## Toast / Inline Alert

- Toast：短暫成功、背景操作完成。
- Inline alert：表單錯誤、權限不足、風險提示。
- 錯誤訊息需提供下一步。

## Empty State

包含：

1. 簡潔標題。
2. 一句說明。
3. 可行動 CTA。
4. 中性 SVG 插圖或 icon。

情境：尚無資料、篩選無結果、沒有權限、載入失敗。

## Audit Log Item

- 操作者。
- 操作內容。
- 目標資源。
- 時間。
- IP / 裝置（可選）。
- 詳情展開。

稽核紀錄不可被任意刪除，UI 上需避免誤導。
