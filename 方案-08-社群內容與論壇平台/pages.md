# Pages：社群內容與論壇平台

## Home Feed

結構：

1. Left nav：首頁、探索、通知、訊息、我的社群。
2. Feed header：分頁或排序。
3. Composer shortcut。
4. Feed list。
5. Right rail：熱門標籤、推薦社群、公告。
6. Loading / empty / error state。

規則：

- Feed item 間距穩定，避免視覺跳動。
- 新內容提示用 banner，不自動把使用者捲走。
- 手機版用 bottom nav 或 top tabs。

## Thread Detail

結構：

1. Breadcrumb 或返回。
2. Main post。
3. Engagement summary。
4. Reply composer。
5. Reply list。
6. Related threads。
7. Moderation tools（有權限才顯示）。

規則：

- 標題與主文寬度適合閱讀。
- 回覆排序清楚。
- 鎖定討論需顯示原因。

## Composer Page / Modal

結構：

1. Title input。
2. Category selector。
3. Editor toolbar。
4. Content editor。
5. Attachment area。
6. Preview。
7. Publish action bar。

狀態：

- Draft saved。
- Validation error。
- Publishing。
- Publish failed。

## Notification Center

結構：

1. Header：通知、全部已讀。
2. Tabs：全部、提及、回覆、系統。
3. Notification list。
4. Empty state。
5. Preferences link。

規則：

- 未讀狀態明確。
- 通知 item 可導向具體內容。
- 批次操作需可復原或確認。

## User Profile

結構：

1. Cover。
2. Avatar + name + role。
3. Bio and links。
4. Stats。
5. Follow / Message action。
6. Tabs：貼文、回覆、收藏、關於。
7. Content list。

## Moderation Queue

結構：

1. Queue metrics：待處理、已處理、逾時。
2. Filter：類型、原因、嚴重度、社群。
3. Report table/list。
4. Detail panel。
5. Action bar。
6. Audit log。

## Search / Explore

結構：

1. Search input。
2. Filters：貼文、使用者、社群、標籤。
3. Result list。
4. Trending topics。
5. Empty result suggestions。

## AI 提示模板

```text
建立一個社群平台首頁 Feed。請使用方案-08 的社群內容與論壇平台風格：內容可讀、互動清楚、紫色 primary、白底卡片、作者資訊與 reaction bar 明確。
頁面需包含 left nav、feed header、composer shortcut、feed item、right rail、notification badge、loading/empty/error 狀態。
不要使用 emoji 當 UI icon；互動 active 狀態不可只靠顏色；hover 不可造成 layout shift。
```
