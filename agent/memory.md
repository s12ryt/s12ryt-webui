# Memory

## 2026-05-27

### 使用者需求

使用者提供 GitHub issue：https://github.com/s12ryt/s12ryt-webui/issues/1

Issue 標題：`項目初始需求`

Issue 內容要求建立 WebUI 專案方向文件，讓 AI 後續知道介面要怎麼做，避免風格不統一；並要求在倉庫根目錄給出多種方案、用資料夾分類。

### 探查結果

- 本地工作目錄：`D:\00\cloudflare\github\s12ryt-webui`
- 初始 `agent/*` 不存在。
- 初始工作區沒有檔案。
- 本地不是 git repository。
- GitHub repository `s12ryt/s12ryt-webui` 是 empty repository。
- 本機沒有可用 `python` 指令，因此 ui-ux-pro-max skill 的搜尋腳本沒有執行，只採用其通用 UI/UX 原則人工整理。

### 已建立內容

- 根目錄 `README.md`：總覽、方案選擇速查、共通 WebUI 原則、AI 提示。
- 五個方案資料夾，每個資料夾都有：
  - `README.md`
  - `design-system.md`
  - `components.md`
  - `pages.md`
- `agent/項目表.md`
- `agent/deep_todos.md`
- `agent/memory.md`

### 方案摘要

1. `方案-01-沉穩企業SaaS控制台`：淺色、藍灰、B2B 後台。
2. `方案-02-暗色AI工作台`：深色、青紫點綴、AI/agent/prompt 工作台。
3. `方案-03-清爽工具型WebUI`：白底、大留白、單一任務工具。
4. `方案-04-品牌行銷Landing`：強 hero、漸層、CTA、社會證明。
5. `方案-05-資料可視化監控`：KPI、圖表、告警、即時監控。

### 注意事項

- 若要提交到 GitHub，需要先 `git init`，設定 remote，再 commit/push；目前尚未做，因為使用者沒有明確要求提交。
- 如果後續要做實際 UI，必須先指定主方案，避免混風格。
- 不要把 emoji 當正式 UI icon。
