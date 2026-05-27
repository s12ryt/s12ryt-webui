# Components：暗色 AI 工作台

## Workspace Shell

- 左側：歷史紀錄、專案、資料來源。
- 中央：主要對話或任務執行區。
- 右側：參數、上下文、工具狀態。
- 底部：輸入框或 command bar。

## Message

角色：

- User：右側或全寬卡片，背景較亮。
- Assistant：左側或全寬內容，支援 markdown/code。
- System / Tool：使用 compact log 樣式，不與對話混淆。

必要狀態：

- pending
- streaming
- completed
- failed
- cancelled

## Prompt Input

- 支援多行。
- 右下放 submit button。
- 可放 attachment、model selector、temperature 等控制。
- Enter / Shift+Enter 行為需清楚。

## Code Block

- 深色區塊比主背景再亮一階。
- 顯示語言標籤。
- 提供 copy button。
- 長內容可水平捲動，不破版。

## Run Status

- Running：青色 pulse dot。
- Success：綠色 check icon。
- Warning：黃色 alert icon。
- Failed：紅色 x icon。

## Tool Call / Log

- 使用 monospace。
- 時間戳置左或置右但需一致。
- 支援展開/收合。
- 錯誤訊息需可複製。

## Tabs / Segmented Control

用於：Preview、JSON、Logs、Diff、Settings。

- active 狀態使用 primary underline 或 soft background。
- inactive 狀態不能低於可讀對比。
