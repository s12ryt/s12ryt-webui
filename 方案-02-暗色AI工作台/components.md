# Components：暗色 AI 工作台

## Workspace Shell

用途：承載 AI 對話、任務執行、模型調參、工具呼叫、artifact 檢視。

結構：

1. Left sidebar：conversation、project、dataset、history、saved prompt。
2. Top bar：目前 workspace、模型、同步狀態、全域 search。
3. Main area：message stream、editor、preview 或 run timeline。
4. Right inspector：context、tools、parameters、cost、metadata。
5. Bottom prompt input 或 command bar。

狀態：

- sidebar collapsed / expanded
- inspector pinned / drawer
- workspace syncing
- offline / reconnecting

## Message

### 角色

- User：清楚標示使用者輸入，可放在右側或全寬卡片。
- Assistant：支援 markdown、code、table、artifact link。
- System：使用 compact system notice，不與一般回覆混淆。
- Tool：使用 log/event 樣式，預設可收合。
- Error：使用 danger panel，提供可複製錯誤。

### 必備狀態

- queued
- streaming
- completed
- failed
- cancelled
- regenerated

### 必備操作

- copy
- retry / regenerate
- branch from here
- view raw
- report issue 或 feedback

## Prompt Input

組成：

- 多行 textarea。
- Submit / Stop button。
- Model selector。
- Attachment button。
- Context source chips。
- Advanced controls 入口。

規則：

- Enter / Shift+Enter 行為需在 helper text 或 tooltip 中說明。
- 送出後若仍可編輯，必須明確顯示是否會影響目前 run。
- 空輸入時 primary button disabled。
- 附件上傳需顯示進度、大小、失敗原因。

## Model Selector

顯示內容：

- model name
- provider
- context window
- speed / cost hint
- capability badge，例如 vision、tool use、reasoning

互動規則：

- 切換模型時保留 prompt，不要清空使用者內容。
- 若模型不支援工具或附件，要顯示限制原因。

## Parameter Panel

常見欄位：

- temperature
- max tokens
- system prompt
- response format
- tool permissions
- memory / retrieval mode

規則：

- 進階參數預設收合。
- 每個參數提供簡短說明與合理範圍。
- 改動後要顯示 unsaved / applied 狀態。

## Code Block

- 深色區塊比主背景亮一階。
- 顯示語言標籤、copy button、wrap toggle。
- 長行允許水平捲動，不破壞整頁 layout。
- 多檔案輸出要用 file tabs 或 artifact list，不要堆在單一訊息中。

## Tool Call Card

必備資訊：

- 工具名稱。
- 狀態：queued、running、success、failed、skipped。
- input 摘要。
- output 摘要。
- 耗時、成本或 token。
- 展開後顯示完整 JSON / log。

高風險工具：

- 使用 warning / danger 樣式。
- 顯示會改動的資源。
- 需要確認或 permission badge。

## Run Timeline

用途：呈現 agent 或 workflow 的步驟。

每個 step 包含：

- step name
- status
- timestamp / duration
- model / tool
- artifact link
- error detail

規則：

- 目前步驟自動展開。
- 已完成步驟可收合。
- 失敗步驟需固定顯示 retry 與 copy error。

## Artifact Panel

支援類型：

- Markdown
- code file
- diff
- JSON
- image preview
- table
- link

規則：

- artifact 必須可從 message 或 timeline 回溯來源。
- Diff view 要明確標示新增、刪除與檔案路徑。
- 大型 artifact 預設摘要，使用者再展開。

## Log Viewer

- 使用 monospace。
- 支援 level filter：info、warn、error、debug。
- 支援搜尋、copy、download。
- 時間戳格式需一致。
- 錯誤 stack trace 不應被截斷到不可理解。

## Tabs / Segmented Control

適用於：Preview、JSON、Logs、Diff、Settings、Context。

- Active 使用 primary underline 或 soft background。
- Inactive 文字不可低於可讀對比。
- 切換 tab 不應重置使用者已輸入內容。

## Empty State

應依場景提供下一步：

- 尚無對話：提供 prompt 範例與建立專案。
- 尚無工具：引導設定 tool permission。
- 尚無資料來源：引導上傳、連接或貼上內容。
- 尚無 evaluation：引導建立 dataset。

## Toast / Inline Alert

- 成功複製、儲存設定可用 toast。
- 工具失敗、權限不足、成本超量必須用 inline alert 或 panel，不只用 toast。
- Alert 需提供修復方式或查看詳細資料。
