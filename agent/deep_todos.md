# Deep Todos

## Issue #1：項目初始需求

來源：https://github.com/s12ryt/s12ryt-webui/issues/1

### 需求摘錄

- `項目方向`：用於給 AI 知道 WebUI 怎麼做，避免每次風格不統一。
- `需要`：需要在倉庫根目錄給出多種方案並使用文件夾分類。

### 已完成

- [x] 確認本地工作區初始沒有檔案。
- [x] 確認 GitHub 遠端倉庫目前是 empty repository。
- [x] 在根目錄建立總入口 `README.md`。
- [x] 建立 5 個 WebUI 方向方案資料夾：
  - [x] `方案-01-沉穩企業SaaS控制台/`
  - [x] `方案-02-暗色AI工作台/`
  - [x] `方案-03-清爽工具型WebUI/`
  - [x] `方案-04-品牌行銷Landing/`
  - [x] `方案-05-資料可視化監控/`
- [x] 每個方案內建立：
  - [x] `README.md`
  - [x] `design-system.md`
  - [x] `components.md`
  - [x] `pages.md`
- [x] 建立 `agent/項目表.md` 紀錄專案結構。
- [x] 建立 `agent/memory.md` 紀錄交接資訊。

### 待辦

- [ ] 若使用者要上傳到 GitHub：初始化 git、commit、push 到遠端預設分支。
- [ ] 可選：依選定方案建立實際 Web App scaffold。
- [ ] 可選：為選定方案補一份可視化範例頁面或 screenshot。
- [ ] 可選：關閉 GitHub issue #1，並附上完成摘要。

## 後續建議

1. 先讓使用者挑選主要方案。
2. 再決定技術棧與是否要建立實際可執行 WebUI。
3. 若進入實作階段，將 design token 轉成程式碼中的 theme 設定。
