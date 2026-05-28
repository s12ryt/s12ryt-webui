# 方案 02：暗色 AI 工作台

## 定位

適合 AI chat、agent 控制台、prompt playground、模型測試平台、開發者工具、資料處理工作流、向量資料檢索、工具呼叫觀察與自動化任務執行介面。

## 設計關鍵字

- 沉浸
- 高科技
- 專注
- 即時回饋
- 命令感
- 可觀測
- 可調試

## 視覺摘要

以深色背景建立專注感，使用青色、紫色或藍色作為點綴。介面像工作台而不是傳統後台，重視輸入區、輸出區、側欄上下文、執行狀態、工具呼叫與 log 可讀性。

## 典型使用者

- 使用 AI 對話、生成、分析或自動化任務的一般使用者。
- 調整 prompt、模型參數、評估輸出的開發者或 prompt engineer。
- 監控 agent run、工具呼叫、成本、錯誤與 artifacts 的技術人員。

## 適合頁面

- Chat / Agent 工作台
- Prompt 編輯器
- 模型參數面板
- 任務執行流程
- Tool call / Log viewer
- API playground
- Evaluation dashboard
- Dataset / context manager

## 不適合

- 長時間大量表格輸入的財務後台。
- 高齡或低資訊熟悉度使用者為主的公共服務。
- 需要溫暖品牌感的行銷頁。
- 高信任付款確認或法遵審核流程。

## 資訊密度

中。主工作區要讓輸入與輸出保持清楚，側欄可承載模型、工具、上下文與參數；log 區可高密度但必須可收合。

## 實作優先順序

1. 建立 shell：左側專案/歷史、中央工作區、右側 context panel、底部 prompt input。
2. 建立輸入/輸出元件：message、prompt input、code block、artifact card、streaming state。
3. 建立工作流元件：run status、stepper、timeline、tool call、log、diff viewer。
4. 建立調試功能：token/cost、model selector、temperature、evaluation、retry。
5. 補錯誤與取消：failed、cancelled、timeout、rate limit、empty context。

## 風格邊界

- 可以使用細緻 glow，但不使用廉價霓虹滿版。
- 可以深色沉浸，但文字對比必須足夠。
- 可以有技術感，但不能犧牲可讀性與操作可預期性。
