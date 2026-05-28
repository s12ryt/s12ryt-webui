# Pages：暗色 AI 工作台

## Chat Workspace

用途：AI 對話、長文本生成、問答、上下文操作。

結構：

1. Left sidebar：conversation list、project、recent files。
2. Top bar：workspace title、model selector、sync status。
3. Main message stream：user / assistant / system / tool message。
4. Bottom prompt input：附件、context chips、submit/stop。
5. Right inspector：system prompt、retrieval source、token/cost、tools。

必要狀態：

- empty conversation
- streaming response
- tool running
- generation failed
- context too large
- offline reconnecting

## Prompt Playground

用途：測試 prompt、比較模型、調整參數、保存版本。

結構：

1. Header：prompt 名稱、版本、儲存狀態、環境。
2. Left editor：system prompt、user prompt、variables。
3. Right output：model response、format validation、token usage。
4. Bottom panel：logs、cost、latency、diff。
5. Side panel：model parameters、dataset examples。

必要互動：

- run
- stop
- save version
- compare output
- copy response
- export prompt

## Agent Run Detail

用途：檢視 autonomous agent 或多步驟 workflow 的執行過程。

結構：

1. Run summary：狀態、任務、模型、耗時、成本、啟動者。
2. Timeline：planning、tool call、artifact、review、final response。
3. Artifact area：檔案、diff、連結、報告。
4. Right inspector：permissions、context、environment。
5. Error panel：失敗時固定顯示原因、重試、回復方式。

必要狀態：

- queued
- running
- waiting for permission
- completed
- failed
- cancelled

## Tool Call / Log Viewer

用途：給開發者或進階使用者追蹤工具輸入輸出。

結構：

1. Filter bar：level、tool、status、time range。
2. Log list：timestamp、source、message。
3. Detail drawer：完整 input/output、headers、stack trace。
4. Action bar：copy、download、open artifact。

注意：

- 預設隱藏敏感值，以 placeholder 顯示。
- error log 需要可直接複製。
- 長 log 使用 virtualized list。

## API Playground

用途：測試 AI API、工具 API、內部 endpoint。

結構：

1. Endpoint selector。
2. Request editor：headers、body、auth hint。
3. Response viewer：status、latency、body、headers。
4. Examples / docs side panel。
5. History list：最近 request。

必要狀態：

- auth missing
- request running
- response success
- response error
- timeout

## Evaluation Dashboard

用途：比較模型、prompt、dataset 的品質與成本。

結構：

1. KPI row：pass rate、avg cost、latency、regression count。
2. Comparison chart：不同模型或版本。
3. Dataset table：case、expected、actual、score、reason。
4. Failure cluster：常見錯誤分類。
5. Export / rerun actions。

設計重點：

- 品質分數不能只用顏色，需有文字解釋。
- 失敗案例需要可直接回到 prompt 或 run detail。

## Dataset / Context Manager

用途：管理知識來源、文件、向量資料、上下文片段。

結構：

1. Source list：file、url、database、manual text。
2. Ingestion status：queued、embedding、indexed、failed。
3. Chunk preview：內容片段與 metadata。
4. Permission panel：哪些 workflow 可使用。
5. Search test：輸入 query 檢查 retrieval 結果。

## Settings / Permission Page

用途：設定工具權限、模型權限、API key 狀態、成本限制。

結構：

1. Account / workspace settings。
2. Model access matrix。
3. Tool permission list。
4. Budget and rate limit。
5. Audit log。

## AI 提示模板

```text
建立一個暗色 AI 工作台頁面。主方案使用「方案-02-暗色AI工作台」。
請先輸出資訊架構、Design token 使用、元件清單、狀態設計與 RWD 策略，再輸出程式碼。
畫面需使用深藍黑背景、cyan / purple 點綴、清楚的 message、tool call、log、artifact 與執行狀態。
必須包含 loading、streaming、failed、empty、permission required 狀態。
遵守本方案的 design-system.md、components.md 與共用規格/AI輸出契約.md。
不要做成傳統淺色管理後台，不要使用 emoji icon，不要隱藏成本、錯誤或工具呼叫細節。
```
