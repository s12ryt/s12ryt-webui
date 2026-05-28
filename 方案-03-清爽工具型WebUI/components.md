# Components：清爽工具型 WebUI

## Tool Card

用途：承載單一工具的主要流程。

必要區塊：

1. 標題與一句說明。
2. Input 區。
3. Action bar。
4. Output 區。
5. Helper / tips。

狀態：

- empty：尚未輸入。
- dirty：輸入已改變但尚未執行。
- processing：執行中。
- completed：已有結果。
- error：輸入或處理失敗。

## Input

規格：

- label 必須明確。
- placeholder 提供真實範例。
- textarea 預設高度 160px-240px。
- 支援貼上、清空、載入範例。
- 若支援檔案，上傳區必須顯示格式與大小限制。

錯誤規則：

- 錯誤訊息放在欄位下方。
- 如果有多個錯誤，優先顯示最阻塞的錯誤。
- 錯誤文案要說明如何修正。

## Output

規格：

- 結果區使用淡灰背景或白底灰框。
- 提供 copy button。
- 長文字可捲動或切換 wrap。
- 空狀態提示「輸入內容後會顯示結果」。
- 若輸出是 code，使用 monospace 與語法標籤。

操作：

- copy
- download
- share
- open in new panel
- clear output

## Button

類型：

- Primary：執行、轉換、產生、查詢。
- Secondary：清空、重設、載入範例。
- Ghost：複製、下載、展開進階設定。
- Danger：刪除歷史、清除所有資料。

狀態：

- default
- hover
- focus
- loading
- disabled
- success feedback

規則：

- Primary button 只能有一個最主要操作。
- Loading 時保留按鈕寬度，避免跳動。
- Disabled 必須有 tooltip 或 helper 說明原因。

## Advanced Options

用途：放非必要但會影響輸出的設定。

規則：

- 預設收合。
- 用 disclosure / accordion 呈現。
- 分組命名要具體，例如「輸出格式」、「驗證規則」。
- 進階選項變更後需標示結果可能不同。

## Example Pills

用途：降低空白頁門檻。

規格：

- 放在輸入區下方或空狀態內。
- 提供 2-4 個範例。
- 點擊後填入真實資料。
- 不要使用過長文字造成換行混亂。

## File Dropzone

適用：檔案轉換、解析、驗證。

必備：

- 支援格式。
- 最大大小。
- 上傳進度。
- 成功與失敗狀態。
- 移除檔案操作。

## Copy Button

規則：

- 成功後顯示「已複製」1.5-2 秒。
- 失敗時提供手動選取提示。
- 有多個輸出時，每個輸出區有自己的 copy button。

## Toast

使用情境：

- 複製成功。
- 下載完成。
- 儲存偏好。
- 操作失敗但不需要阻塞流程。

不適合：

- 表單驗證錯誤。
- 會阻塞使用者完成任務的錯誤。
- 權限不足。

## Inline Alert

用途：顯示與目前輸入或輸出直接相關的資訊。

類型：

- info：格式提醒。
- warning：資料可能不完整。
- danger：無法處理。
- success：處理完成。

## History List

適用於重複工具。

規則：

- 不預設佔據主視覺。
- 可以用側邊 drawer 或下方列表。
- 每筆顯示時間、輸入摘要、操作。
- 支援清除歷史，且需確認。

## FAQ / Tips

- 放在主工具下方。
- 每項回答短而具體。
- 只放會幫助完成任務的內容。
