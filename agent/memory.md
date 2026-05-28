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

## 2026-05-28：方案擴充與治理規格

### 使用者追加回饋

使用者指出：「應該要給出更多方案並且更加的細化」。

### 處理方向

在已合併的 PR #2 基礎上，建立補強分支 `docs/expand-webui-directions`，將 WebUI 方向資料庫從 5 套方案擴充為 12 套方案，並新增跨方案共用規格、品質門檻與 AI 實作交接規則。

### 已新增共用規格

- `共用規格/方案選擇矩陣.md`：提供快速決策樹、維度比較、混用規則與選定方案後的必填欄位。
- `共用規格/細化檢查清單.md`：要求每個方案與頁面補齊定位、token、layout、元件、狀態、RWD、a11y、交付檢查。
- `共用規格/AI輸出契約.md`：規範 AI 必須先輸出方案確認、資訊架構、Design token、元件清單、狀態設計、RWD、可及性，再輸出實作內容。
- `共用規格/方案品質門檻.md`：補上方案最低合格門檻、20 分評分表、PR review 必問問題與不合格修正順序。
- `共用規格/AI實作交接卡.md`：補上交給 AI 或開發者前的交接模板，要求明確填寫主方案、頁面範圍、主要任務、狀態、RWD、禁用風格與驗收條件。

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

### GitHub 狀態

- PR #4：`https://github.com/s12ryt/s12ryt-webui/pull/4` 已建立並由使用者合併。
- `main` 已包含 12 套方案與 5 個共用規格。

## 2026-05-28：AI 閱讀與小組件拆分

### 使用者追加回饋

使用者要求：「請針對ai閱讀做一些優化,還有把一些小組件拆分出來放到一個資料夾裡面」。使用者合併 PR #4 後，又要求重開新的 PR。

### 處理方向

從已包含 PR #4 的 `origin/main` 建立新分支 `docs/ai-reading-components`。本次不改 12 套方案本體，而是補 AI 閱讀路徑、低上下文模式與跨方案小組件資料夾，降低 AI 閱讀成本並避免把所有方案塞入上下文造成風格混用。

### 已新增 AI 閱讀入口

- `AI閱讀入口.md`：
  - 說明本 repo 是 WebUI 方向資料庫，不是實際 Web App。
  - 定義快速了解專案、實作頁面、新增/大改方案、審查 PR 的閱讀順序。
  - 定義低上下文模式：只讀必要文件，不讀所有 `方案-*`。
  - 要求 AI 先確認唯一主方案，再輸出資訊架構、design token、元件清單、狀態、RWD、可及性，最後才輸出程式碼。
  - 要求使用小組件時先取 `小組件/` 的共用結構，再套用主方案 token。

### 已新增小組件資料夾

- `小組件/README.md`：小組件使用原則、分類索引、AI 使用範本、共用狀態、命名建議與禁止事項。
- `小組件/基礎元件.md`：Button、TextInput、Select、Checkbox、Radio、Switch、Card、Badge、Avatar、Divider、Tooltip。
- `小組件/資料與狀態元件.md`：Table、List、MetricCard、ChartPanel、EmptyState、Skeleton、ErrorState、PermissionNotice、Toast/InlineAlert。
- `小組件/導覽與浮層元件.md`：AppHeader、SideNav、Breadcrumbs、TabsNav、Dialog、Drawer、PopoverMenu、Tooltip。
- `小組件/表單與操作元件.md`：FormField、FieldGroup、SearchInput、FilterBar、ActionBar/BulkActionBar、Pagination、Stepper、Confirm pattern。
- `小組件/內容展示元件.md`：HeroSection、FeatureGrid、PricingCard、MediaCard、ArticleCard、Timeline、Callout/Highlight、QuoteBlock/Testimonial。

### 已串接索引與契約

- `README.md`：新增 `AI閱讀入口.md` 的使用方式，說明需要具體元件時讀 `小組件/`，並在 AI 實作提示中要求列出小組件來源與回套主方案 token。
- `共用規格/AI輸出契約.md`：新增小組件來源欄位、AI 回答中的小組件套用方式，以及禁止把 `小組件/` 當成另一套視覺方案。
- `共用規格/AI實作交接卡.md`：新增小組件來源、來源文件與套用方式欄位。
- `agent/項目表.md`：新增 AI 閱讀入口與小組件資料夾索引。
- `agent/deep_todos.md`：新增本次需求與待辦狀態。

### 注意事項

- 後續實作 WebUI 必須先指定唯一主方案。
- 若需要混合方案，只能借用單一元件或頁型概念，不可混用主色、狀態色、圓角、陰影與資訊密度。
- `小組件/` 只定義結構、狀態與互動規則，不決定品牌色、圓角、陰影、字級、間距與資訊密度。
- 若小組件文件與主方案文件衝突，以主方案 `design-system.md` 與 `components.md` 為準。
- 不要把 emoji 當正式 UI icon。
- 目前仍是文件型專案，尚未建立實際 app scaffold。
