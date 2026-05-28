# Deep Todos

## Issue #1：項目初始需求

來源：https://github.com/s12ryt/s12ryt-webui/issues/1

### 原始需求摘錄

- `項目方向`：用於給 AI 知道 WebUI 怎麼做，避免每次風格不統一。
- `需要`：需要在倉庫根目錄給出多種方案並使用文件夾分類。

### 原始交付已完成

- [x] 確認本地工作區初始沒有檔案。
- [x] 確認 GitHub 遠端倉庫初始是 empty repository。
- [x] 在根目錄建立總入口 `README.md`。
- [x] 建立 5 個 WebUI 方向方案資料夾：
  - [x] `方案-01-沉穩企業SaaS控制台/`
  - [x] `方案-02-暗色AI工作台/`
  - [x] `方案-03-清爽工具型WebUI/`
  - [x] `方案-04-品牌行銷Landing/`
  - [x] `方案-05-資料可視化監控/`
- [x] 每個方案內建立：`README.md`、`design-system.md`、`components.md`、`pages.md`。
- [x] 建立 `agent/項目表.md` 紀錄專案結構。
- [x] 建立 `agent/memory.md` 紀錄交接資訊。
- [x] 初始化 git，建立 `main` 基準分支。
- [x] 建立 PR #2：`https://github.com/s12ryt/s12ryt-webui/pull/2`。
- [x] PR #2 已合併，Issue #1 已自動關閉。

## 2026-05-28 補強需求：更多方案並更加細化

使用者回饋：`應該要給出更多方案並且更加的細化`

### 已完成

- [x] 同步遠端 `origin/main`。
- [x] 從已合併的 main 建立補強分支：`docs/expand-webui-directions`。
- [x] 擴充根目錄 `README.md`，由 5 套方案改為 12 套方案總覽。
- [x] 新增 `共用規格/`，提供跨方案規則：
  - [x] `共用規格/方案選擇矩陣.md`
  - [x] `共用規格/細化檢查清單.md`
  - [x] `共用規格/AI輸出契約.md`
  - [x] `共用規格/方案品質門檻.md`
  - [x] `共用規格/AI實作交接卡.md`
- [x] 新增 7 個完整方案資料夾，每個都有 `README.md`、`design-system.md`、`components.md`、`pages.md`：
  - [x] `方案-06-高信任金融科技平台/`
  - [x] `方案-07-電商營運購物體驗/`
  - [x] `方案-08-社群內容與論壇平台/`
  - [x] `方案-09-知識庫文件中心/`
  - [x] `方案-10-創作者作品集媒體展示/`
  - [x] `方案-11-教育學習課程平台/`
  - [x] `方案-12-遊戲化活動互動介面/`
- [x] 細化既有 5 個方案資料夾：
  - [x] 方案 01：補典型使用者、更多頁型、狀態、權限、資料表格與設定頁規則。
  - [x] 方案 02：補 AI 工作台三欄、tool call、log、artifact、evaluation、dataset/context manager 規則。
  - [x] 方案 03：補單一工具、converter、generator、設定器、批次工具與輸入/輸出狀態規則。
  - [x] 方案 04：補 landing 轉換目標、區塊節奏、CTA、pricing、waitlist、case study 與 campaign 規則。
  - [x] 方案 05：補監控核心問題、KPI、chart、alert、incident、log analytics、refresh/stale data 規則。
- [x] 更新 `agent/項目表.md`。
- [x] 更新 `agent/memory.md`。
- [x] 依 git-master 規則拆分多個原子提交。
- [x] 推送 `docs/expand-webui-directions`。
- [x] 建立補強 PR #4 到 `main`。
- [x] PR #4 已合併。

## 2026-05-28 補強需求：AI 閱讀優化與小組件拆分

使用者回饋：`請針對ai閱讀做一些優化,還有把一些小組件拆分出來放到一個資料夾裡面`

### 已完成

- [x] 使用者合併 PR #4 後，重新從 `origin/main` 建立補強分支：`docs/ai-reading-components`。
- [x] 新增 `AI閱讀入口.md`，提供 AI 最短閱讀路徑、低上下文模式、任務判斷表與回答前自檢。
- [x] 新增 `小組件/` 資料夾，將跨方案常用元件拆成獨立文件：
  - [x] `小組件/README.md`
  - [x] `小組件/基礎元件.md`
  - [x] `小組件/資料與狀態元件.md`
  - [x] `小組件/導覽與浮層元件.md`
  - [x] `小組件/表單與操作元件.md`
  - [x] `小組件/內容展示元件.md`
- [x] 更新 `README.md`，加入 AI 閱讀入口、小組件使用方式與 AI 提示。
- [x] 更新 `共用規格/AI輸出契約.md`，要求列出小組件來源與套用方式。
- [x] 更新 `共用規格/AI實作交接卡.md`，加入小組件來源與套用方式欄位。
- [x] 更新 `agent/項目表.md`。
- [x] 更新 `agent/memory.md`。

### 待辦

- [ ] 檢查 git 差異與 Markdown 結構。
- [ ] 依 git-master 規則拆分多個原子提交。
- [ ] 推送 `docs/ai-reading-components`。
- [ ] 建立新的補強 PR 到 `main`。

## 後續建議

1. 後續真正做 WebUI 前，先在 12 套方案中指定唯一主方案。
2. 若需求跨多場景，先用 `共用規格/方案選擇矩陣.md` 決定主方案，再只借用其他方案的單一頁型或元件概念。
3. 任何實作都應依 `共用規格/AI輸出契約.md`，先輸出資訊架構、design token、小組件來源、元件清單、狀態設計與 RWD 策略，再寫程式碼。
4. 若使用 `小組件/`，只能借用結構、狀態與互動規則；色彩、圓角、陰影、字級、間距與資訊密度仍回到唯一主方案。
5. 不要用 emoji 當正式 UI icon；需使用一致 SVG icon 系統。
