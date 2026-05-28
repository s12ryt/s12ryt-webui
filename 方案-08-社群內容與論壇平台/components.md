# Components：社群內容與論壇平台

## Button

- Primary：發佈、回覆、加入社群、追蹤。
- Secondary：儲存草稿、預覽、分享。
- Ghost：更多操作、貼文內輕量操作。
- Danger：刪除貼文、封鎖、移除內容。

## Avatar

- 尺寸：24px、32px、40px、56px、80px。
- 預設用字母 fallback，不用 emoji。
- 可顯示線上狀態，但不要過度干擾。
- 管理員或官方可用 badge 標示。

## Feed Item

結構：

1. Author row：頭像、名稱、身份、時間、社群/分類。
2. Content：標題、摘要或全文。
3. Media preview：可選。
4. Tags。
5. Reaction bar：讚、回覆、收藏、分享。
6. More menu。

狀態：

- pinned：置頂標示。
- locked：關閉回覆。
- deleted：顯示已刪除與原因。
- reported：管理員可見檢舉狀態。

## Composer

功能：

- 標題輸入。
- 內容編輯器。
- 附件/圖片。
- 標籤與分類。
- 發佈、草稿、預覽。

規則：

- 未儲存離開需提示。
- 發佈中 disabled，避免重複發文。
- 錯誤顯示在對應欄位或 composer top。

## Reaction Bar

- Like / Upvote。
- Comment。
- Bookmark。
- Share。
- More。

規則：

- active 狀態需同時有顏色、icon fill 或文字變化。
- 不只靠顏色。
- 數字格式：999、1.2k、12k。

## Comment / Reply

結構：

1. Author。
2. Time。
3. Content。
4. Actions：回覆、讚、更多。
5. Nested replies。

規則：

- 巢狀最多視覺呈現 3 層，再改「查看回覆」。
- 被封鎖或隱藏留言需顯示原因。
- 編輯過的留言顯示 edited。

## Thread View

- 主貼文完整呈現。
- 回覆排序：熱門、最新、最舊。
- 回覆 composer 可在底部或主文下方。
- 右側可放相關討論、熱門標籤。

## Notification Item

類型：

- 新回覆。
- 被提及。
- 新追蹤。
- 管理通知。
- 系統公告。

規則：

- 未讀狀態用背景與小點，不只用粗體。
- 點擊後可導向具體內容。
- 批次標為已讀。

## Report / Moderation Panel

必備：

- 被檢舉內容。
- 檢舉原因。
- 歷史紀錄。
- 操作：保留、移除、警告、封鎖。
- 審核備註。

高風險操作需二次確認。

## User Profile Card

- 頭像、名稱、帳號。
- Bio。
- 統計：貼文、追蹤、聲望。
- Follow / Message CTA。
- Badge / Role。

## Empty State

- Feed 空：建議追蹤主題或建立第一篇貼文。
- 通知空：說明尚無新動態。
- 搜尋空：提供調整關鍵字。

## Toast

- 發佈成功：提供查看貼文。
- 草稿已儲存：短暫提示。
- 檢舉已送出：說明後續處理。
