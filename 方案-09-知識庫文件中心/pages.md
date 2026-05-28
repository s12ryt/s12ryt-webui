# Pages：知識庫文件中心

## Documentation Home

結構：

1. Hero search：大搜尋框與熱門關鍵字。
2. Category cards：入門、帳號、API、疑難排解。
3. Popular articles。
4. Changelog preview。
5. Contact support / community link。

規則：

- 搜尋是首要行動。
- 分類卡文字要具體，不只寫抽象分類。
- 熱門文章顯示更新時間。

## Article Page

結構：

1. Top bar。
2. Left sidebar。
3. Breadcrumb。
4. Article header。
5. Version banner（需要時）。
6. Article body。
7. Feedback widget。
8. Previous / next navigation。
9. Right TOC。

狀態：

- 文章不存在：顯示搜尋與返回首頁。
- 無權限：顯示申請權限。
- 舊版本：顯示切換最新版 CTA。

## API Reference Page

結構：

1. API group sidebar。
2. Endpoint title。
3. Method + URL。
4. Authentication note。
5. Parameters。
6. Request examples。
7. Response examples。
8. Error codes。
9. SDK examples。

規則：

- Code block 可左右並排，但手機需上下堆疊。
- Endpoint URL 可一鍵複製。
- 錯誤碼 table 需要說明下一步。

## Search Results Page

結構：

1. Search input。
2. Result count。
3. Filters：分類、版本、更新時間、標籤。
4. Result list：標題、摘要、路徑、高亮。
5. Empty result suggestions。

規則：

- 空結果提供拼字建議或熱門文章。
- 結果摘要要顯示命中段落。

## FAQ Page

結構：

1. Category tabs。
2. Question accordion。
3. Related articles。
4. Contact support CTA。

規則：

- Accordion 展開後保留 URL anchor。
- 問題文案要接近使用者真實問法。

## Changelog Page

結構：

1. Version list。
2. Release date。
3. Change type badges：Added、Changed、Fixed、Deprecated。
4. Migration notes。
5. Related docs。

## Editor / Review Page

結構：

1. Metadata：標題、slug、版本、分類。
2. Markdown editor。
3. Preview。
4. Validation checklist。
5. Publish / save draft。

## AI 提示模板

```text
建立一個知識庫文章頁。請使用方案-09 的知識庫文件中心風格：白底、清楚側欄、文章最大寬度、右側 TOC、搜尋與版本提示。
頁面需包含 top bar、sidebar navigation、breadcrumb、article header、version banner、callout、code block、feedback widget、previous/next navigation。
不要讓文章過寬；不要使用 emoji 當 callout icon；code block 要有 copy 成功狀態；搜尋需支援鍵盤操作說明。
```
