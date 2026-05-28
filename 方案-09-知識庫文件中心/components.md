# Components：知識庫文件中心

## Button

- Primary：開始使用、提交回饋、建立文件。
- Secondary：查看範例、下載、切換版本。
- Ghost：文章工具列、複製連結、編輯。
- Danger：刪除文件、取消發布。

## Search Box / Command Search

功能：

- 快捷鍵 `Ctrl/Cmd + K`。
- 即時搜尋建議。
- 顯示分類、路徑、摘要。
- 支援空結果建議。

規則：

- 搜尋結果要高亮關鍵字。
- 鍵盤上下選取與 Enter 開啟。
- Loading 時顯示 skeleton list。

## Sidebar Navigation

結構：

- 分類標題。
- 可展開章節。
- active item。
- locked / beta / deprecated badge。

規則：

- 左側捲動不影響文章主體。
- 目錄層級不超過 3 層視覺縮排。
- 手機使用 drawer。

## Table of Contents

- 顯示 H2/H3。
- 捲動時同步 active。
- 章節過長時可折疊。
- 右側 TOC 在小螢幕隱藏。

## Article Header

必備：

1. 標題。
2. 摘要。
3. 更新時間。
4. 適用版本。
5. 作者或維護者。
6. 回饋入口。

## Callout

類型：

- Note：一般補充。
- Tip：建議。
- Warning：注意限制。
- Danger：破壞性或安全風險。

規則：

- 必須有文字標籤。
- 不只靠顏色。
- Danger 不可使用輕淡樣式。

## Code Block

- 語言標籤。
- Copy button。
- 行號可選。
- 高亮重點行可選。
- 長行可水平捲動。

複製成功顯示「已複製」，失敗顯示可手動選取。

## API Reference Block

結構：

- Method + Endpoint。
- 說明。
- Parameters table。
- Request example。
- Response example。
- Error codes。

方法色彩：GET/POST/PATCH/DELETE 使用不同 badge，但仍要有文字。

## Feedback Widget

- 問「這篇文章有幫助嗎？」
- Yes / No。
- No 後顯示原因選項與文字欄位。
- 提交後感謝並提供聯絡或 issue 連結。

## Version Banner

- 最新版本。
- 舊版提示。
- Deprecated warning。
- Beta warning。

版本警告要出現在文章標題附近。

## Breadcrumb

- 顯示文件路徑。
- 手機可只顯示上一層。
- 每層可點擊。

## Empty State

- 搜尋無結果：提供清除篩選、查看熱門文章。
- 分類無文章：提供建立文章或返回首頁。
- 無權限：說明需要登入或申請權限。
