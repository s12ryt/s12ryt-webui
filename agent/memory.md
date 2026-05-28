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
- GitHub repository `s12ryt/s12ryt-webui` 初始是 empty repository。
- 本機沒有可用 `python` 指令，因此 ui-ux-pro-max skill 的搜尋腳本沒有執行，只採用其通用 UI/UX 原則人工整理。

### 初始建立內容

- 根目錄 `README.md`：總覽、方案選擇速查、共通 WebUI 原則、AI 提示。
- 五個方案資料夾，每個資料夾都有：`README.md`、`design-system.md`、`components.md`、`pages.md`。
- `agent/項目表.md`
- `agent/deep_todos.md`
- `agent/memory.md`

### 初始方案摘要

1. `方案-01-沉穩企業SaaS控制台`：淺色、藍灰、B2B 後台。
2. `方案-02-暗色AI工作台`：深色、青紫點綴、AI/agent/prompt 工作台。
3. `方案-03-清爽工具型WebUI`：白底、大留白、單一任務工具。
4. `方案-04-品牌行銷Landing`：強 hero、漸層、CTA、社會證明。
5. `方案-05-資料可視化監控`：KPI、圖表、告警、即時監控。

### GitHub 狀態

- 已初始化 git。
- 已建立 main 基準分支與 feature branch。
- 已建立 PR #2：`https://github.com/s12ryt/s12ryt-webui/pull/2`。
- PR #2 已合併到 main。
- Issue #1 已自動關閉。

## 2026-05-28

### 使用者追加回饋

使用者指出：「應該要給出更多方案並且更加的細化」。

### 本次處理方向

在已合併的 PR #2 基礎上，建立補強分支 `docs/expand-webui-directions`，將 WebUI 方向資料庫從 5 套方案擴充為 12 套方案，並新增跨方案共用規格與 AI 輸出契約。

### 已新增共用規格

- `共用規格/方案選擇矩陣.md`：提供快速決策樹、維度比較、混用規則與選定方案後的必填欄位。
- `共用規格/細化檢查清單.md`：要求每個方案與頁面補齊定位、token、layout、元件、狀態、RWD、a11y、交付檢查。
- `共用規格/AI輸出契約.md`：規範 AI 必須先輸出方案確認、資訊架構、Design token、元件清單、狀態設計、RWD、可及性，再輸出實作內容。

### 已新增方案

6. `方案-06-高信任金融科技平台`：FinTech、錢包、投資、支付、帳務、風險控管。
7. `方案-07-電商營運購物體驗`：商品列表、商品詳情、購物車、結帳、訂單、促銷、商家營運。
8. `方案-08-社群內容與論壇平台`：Feed、討論串、留言、通知、會員互動、版主管理。
9. `方案-09-知識庫文件中心`：產品文件、Help Center、FAQ、API reference、Changelog、文件搜尋。
10. `方案-10-創作者作品集媒體展示`：作品集、攝影集、案例展示、媒體品牌、創作者首頁。
11. `方案-11-教育學習課程平台`：課程、章節、學習進度、播放器、測驗、作業、教師後台。
12. `方案-12-遊戲化活動互動介面`：活動頁、任務中心、簽到、積分、徽章、排行榜、抽獎。

### 已細化既有方案

- 方案 01：補 B2B SaaS 的典型使用者、資料表格、篩選器、批次操作、權限、設定頁、audit log 與狀態規則。
- 方案 02：補 AI 工作台的三欄 layout、message、prompt input、model selector、tool call、run timeline、artifact、log viewer、evaluation、dataset/context manager。
- 方案 03：補清爽工具型 UI 的單一主流程、converter、generator、settings tool、batch tool、copy/download/reset、advanced options、input/output 狀態。
- 方案 04：補品牌 Landing 的轉換目標、hero、CTA、feature、social proof、pricing、waitlist、launch、case study、campaign 與表單狀態。
- 方案 05：補資料監控的核心問題、KPI、chart、alert、incident timeline、filters、log analytics、refresh/stale data、partial failure 與 report view。

### 注意事項

- 後續實作 WebUI 必須先指定唯一主方案。
- 若需要混合方案，只能借用單一元件或頁型概念，不可混用主色、狀態色、圓角、陰影與資訊密度。
- 不要把 emoji 當正式 UI icon。
- 目前仍是文件型專案，尚未建立實際 app scaffold。
