# Components：教育學習課程平台

## Button

- Primary：開始學習、繼續課程、提交答案。
- Secondary：儲存筆記、下載資源、查看討論。
- Ghost：章節列操作、更多選項。
- Danger：刪除課程、重設進度。

## Course Card

結構：

1. 封面。
2. 課程名稱。
3. 講師或來源。
4. 難度與時長。
5. 進度條。
6. 下一步 CTA。

狀態：

- not-started。
- in-progress。
- completed。
- locked。
- archived。

## Lesson List / Curriculum

欄位：

- 章節名稱。
- 類型：影片、文章、測驗、作業。
- 時長。
- 完成狀態。
- 鎖定狀態。

規則：

- 當前章節清楚 highlight。
- 未解鎖章節要顯示條件。
- 手機版可收合分章。

## Progress Indicator

形式：

- Linear progress。
- Circular progress。
- Stepper。
- Completion checklist。

規則：

- 必須顯示文字或數字，例如「完成 6/12」。
- 不只用顏色。
- 進度更新要即時但不干擾。

## Learning Player

區塊：

1. Video / article content。
2. Lesson title。
3. Previous / next。
4. Notes。
5. Resources。
6. Discussion。
7. Mark as complete。

規則：

- 影片播放器控制清楚。
- 筆記可與時間點連動。
- 下一課 CTA 在完成後更明顯。

## Quiz Question

類型：

- Single choice。
- Multiple choice。
- Text answer。
- Code answer。

規則：

- 提交後顯示正確/錯誤與解析。
- 錯誤不可只用紅色，需文字說明。
- 可顯示剩餘題數與時間。

## Assignment Card

- 作業說明。
- 截止時間。
- 提交狀態。
- 評分狀態。
- 回饋。

逾期要 warning，但避免羞辱性文案。

## Note Panel

- 新增筆記。
- 搜尋筆記。
- 連到章節或影片時間。
- 編輯/刪除。

## Resource List

- 檔案名稱。
- 類型。
- 大小。
- 下載狀態。
- 外部連結標示。

## Achievement / Completion Card

- 完成標題。
- 課程名稱。
- 完成日期。
- 下一步建議。
- 下載證書 CTA（若有）。

動畫需克制。

## Teacher Analytics Card

- 完成率。
- 平均分數。
- 掉隊學生。
- 熱門問題。

## Empty State

- 尚無課程：推薦開始學習。
- 尚無筆記：提供新增筆記。
- 尚無作業：說明目前沒有待辦。
