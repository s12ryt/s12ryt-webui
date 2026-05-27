# 方案 02：暗色 AI 工作台

## 定位

適合 AI chat、agent 控制台、prompt playground、模型測試平台、開發者工具、資料處理工作流。

## 設計關鍵字

- 沉浸
- 高科技
- 專注
- 即時回饋
- 命令感

## 視覺摘要

以深色背景建立專注感，使用青色、紫色或藍色作為點綴。介面像工作台而不是傳統後台，重視輸入區、輸出區、側欄上下文與執行狀態。

## 適合頁面

- Chat / Agent 工作台
- Prompt 編輯器
- 模型參數面板
- 任務執行流程
- Log viewer
- API playground

## 不適合

- 長時間大量表格輸入的財務後台
- 高齡或低資訊熟悉度使用者
- 需要溫暖品牌感的行銷頁

## 實作優先順序

1. 建立 shell：左側專案/歷史、中央工作區、右側 context panel。
2. 建立輸入/輸出元件：message、code block、run status、streaming state。
3. 建立工作流元件：stepper、timeline、log、diff viewer。
