# Pages：清爽工具型 WebUI

## Single Tool Page

用途：最常見的單一任務工具頁。

結構：

1. Header：產品名、簡短導航、回饋入口。
2. Intro：一句價值主張與簡短說明。
3. Tool card：輸入、操作、輸出。
4. Advanced options：預設收合。
5. Tips / FAQ：使用提示或常見問題。
6. Footer：版本、隱私、回饋。

必要狀態：

- empty input
- invalid input
- processing
- completed output
- copy success
- output too large

## Converter Page

適用：格式轉換、單位轉換、檔案轉換。

結構：

1. Source selector：輸入格式或上傳方式。
2. Input area：文字或檔案。
3. Conversion options：目標格式、壓縮、縮排等。
4. Convert button。
5. Output preview。
6. Download / copy actions。

設計重點：

- 來源與目標格式要清楚。
- 若轉換會遺失資料，必須使用 warning。
- 大檔案需顯示進度與失敗原因。

## Generator Page

適用：prompt、文案、設定檔、程式碼片段產生器。

結構：

1. Form fields：必要輸入。
2. Optional settings：語氣、格式、長度。
3. Generate button。
4. Output variants：一個或多個結果。
5. Refine actions：重新產生、複製、下載。

設計重點：

- 欄位名稱必須具體。
- 輸出結果要可直接使用。
- 重新產生不應清空原輸入。

## Settings Tool

適用：小型設定器、config builder、內部設定表單。

結構：

1. 分類 tabs 或 section cards。
2. 表單區塊。
3. Preview / generated config。
4. Sticky action bar：儲存、重設、複製。
5. Unsaved changes warning。

必要狀態：

- pristine
- dirty
- saving
- saved
- validation error
- conflict / outdated

## Result Page

適用：工具執行後可分享或獨立查看結果。

結構：

1. Summary：結果摘要。
2. Result body：主要輸出。
3. Actions：copy、download、share。
4. Metadata：生成時間、輸入摘要、版本。
5. Next steps：再次輸入、查看範例。

## Batch Tool Page

適用：批次處理多筆資料。

結構：

1. Upload / paste area。
2. Mapping / validation table。
3. Batch action bar。
4. Progress list。
5. Result table 與下載。

注意：

- 批次錯誤要能定位到列與欄。
- 部分成功時要清楚區分成功與失敗。

## AI 提示模板

```text
建立一個清爽工具型 WebUI。主方案使用「方案-03-清爽工具型WebUI」。
請先輸出資訊架構、Design token 使用、元件清單、狀態設計與 RWD 策略，再輸出程式碼。
畫面需使用白底、大留白、單一主流程、清楚輸入與結果區。
必須包含 empty、invalid、processing、completed、copy success、error 狀態。
遵守本方案的 design-system.md、components.md 與共用規格/AI輸出契約.md。
不要加入複雜後台側欄、過多品牌裝飾或 emoji icon。
```
