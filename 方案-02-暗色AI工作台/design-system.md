# Design System：暗色 AI 工作台

## 設計目標

暗色 AI 工作台不是一般深色主題後台，而是用於長時間對話、執行任務、觀察模型輸出、檢查工具呼叫與調整參數的專業工作環境。設計重點是降低疲勞、讓執行狀態透明、讓錯誤與成本可追蹤。

## 色彩 Token

```css
--color-bg: #050816;
--color-bg-deep: #030712;
--color-bg-gradient-start: rgba(34, 211, 238, 0.12);
--color-bg-gradient-end: rgba(167, 139, 250, 0.10);
--color-surface: #0B1020;
--color-surface-raised: #111827;
--color-surface-soft: #172033;
--color-surface-hover: #1E293B;
--color-border: #263244;
--color-border-strong: #334155;
--color-text: #E5E7EB;
--color-text-muted: #94A3B8;
--color-text-subtle: #64748B;
--color-primary: #22D3EE;
--color-primary-hover: #06B6D4;
--color-primary-soft: rgba(34, 211, 238, 0.12);
--color-secondary: #A78BFA;
--color-secondary-soft: rgba(167, 139, 250, 0.12);
--color-success: #34D399;
--color-success-soft: rgba(52, 211, 153, 0.12);
--color-warning: #FBBF24;
--color-warning-soft: rgba(251, 191, 36, 0.14);
--color-danger: #F87171;
--color-danger-soft: rgba(248, 113, 113, 0.14);
--color-info: #38BDF8;
--color-info-soft: rgba(56, 189, 248, 0.12);
```

## 色彩使用規則

- 主背景使用深藍黑，不使用純黑，避免長時間觀看疲勞。
- 主 CTA 與執行中狀態使用 cyan；AI 智慧、建議、模型相關點綴可使用 purple。
- 錯誤、取消、危險工具呼叫使用 danger；警告與成本超量使用 warning。
- Tool call、log、system message 必須與一般 assistant message 有明確色階差異。
- 背景可使用極淡 radial gradient，但不可壓低文字對比。

## 字體

- UI：Inter、Noto Sans TC、system-ui。
- Code、prompt、log：JetBrains Mono、Fira Code、ui-monospace。
- 數字、token、cost、latency：可使用 monospace 以便對齊。

## 字級

| 用途 | 尺寸 | 行高 | 字重 | 備註 |
| --- | --- | --- | --- | --- |
| Workspace title | 24px | 32px | 700 | 頁面或任務標題 |
| Conversation title | 18px | 28px | 700 | 對話、run detail |
| Panel title | 14px | 20px | 650 | 右側參數與工具面板 |
| Message body | 14px | 24px | 400 | 主要對話內容 |
| Code / log | 13px | 22px | 400 | 需要可讀且可掃描 |
| Meta / timestamp | 12px | 18px | 500 | 成本、時間、模型名稱 |
| Badge | 11px | 16px | 650 | 狀態標籤 |

## Layout

### 桌面三欄工作台

- Left sidebar：260px-300px，放 conversation、project、dataset、history。
- Main workspace：彈性寬度，放 message stream、editor、preview、artifact。
- Right inspector：320px-400px，放 model settings、context、tools、run metadata。
- Bottom prompt input：可固定在主區底部，最小高度 112px，展開後不超過視窗 45%。

### 中尺寸螢幕

- 左欄可收合為 icon rail。
- 右欄改為 drawer 或 tab panel。
- 中央 message 最大寬度維持 900px，避免文字過長。

### 手機版

- 預設只顯示主要對話或任務流程。
- conversation list、settings、tools 進入 bottom sheet。
- prompt input 固定底部時必須避開系統安全區。

## 間距與尺寸

```css
--space-panel: 16px;
--space-section: 20px;
--space-message: 18px;
--height-topbar: 56px;
--height-input-min: 112px;
--width-sidebar: 280px;
--width-inspector: 360px;
```

- Message 之間至少 16px，tool log 可更緊湊但不可低於 8px。
- Panel 內部使用 12px 或 16px spacing，避免暗色畫面過度壓迫。
- Code block padding 14px-16px。

## 圓角與陰影

```css
--radius-sm: 8px;
--radius-md: 12px;
--radius-lg: 18px;
--radius-xl: 24px;
--shadow-glow: 0 0 28px rgba(34, 211, 238, 0.14);
--shadow-panel: 0 18px 48px rgba(0, 0, 0, 0.28);
--shadow-danger: 0 0 24px rgba(248, 113, 113, 0.12);
```

- glow 只用於 focus、active run、selected artifact，不可到處使用。
- 大面板用深陰影區分層級，小元件以 border 區分即可。

## 狀態規則

| 狀態 | 視覺規則 | 必備文字 |
| --- | --- | --- |
| idle | muted text、空狀態提示 | 下一步操作 |
| pending | spinner 或 subtle pulse | 等待原因 |
| streaming | caret 或逐步內容 | 可停止或暫停 |
| running tool | cyan dot、log 展開入口 | 工具名稱與耗時 |
| success | success badge | 完成結果摘要 |
| warning | warning banner | 影響與建議 |
| failed | danger panel | 錯誤原因、重試方式、可複製細節 |
| cancelled | neutral badge | 取消時間與已完成步驟 |

## 互動與鍵盤

- Prompt input 必須清楚標示 Enter / Shift+Enter 行為。
- 所有可點擊工具、artifact、message action 必須有 `cursor-pointer` 與 focus ring。
- 支援常用快捷鍵時要提供 command menu 或 help overlay。
- Stop generation 必須比其他次要按鈕更容易找到。
- 危險工具呼叫、外部寫入、刪除資料、花費大量 token 的行為需二次確認。

## 動效

- Streaming 可漸進出現，但不要讓整段文字跳動。
- Running 使用 subtle pulse，頻率不超過每秒一次。
- Panel / drawer 開合 160ms-220ms。
- 對 `prefers-reduced-motion` 使用者停用閃爍、粒子、長距離位移。

## 可及性

- 深色模式下 body text 對比需達 WCAG AA。
- 狀態不可只用顏色，必須搭配文字或 SVG icon。
- Code block 的 copy button 要有 aria-label。
- Log viewer 需要可鍵盤捲動與搜尋。

## 禁止事項

- 不使用過多霓虹外光，避免廉價科技感。
- 不使用低對比灰字承載重要資訊。
- 不讓側欄、面板、主工作區全部同一色階。
- 不用 emoji 當模型、工具、狀態 icon。
- 不把成本、token、錯誤訊息藏在不可見角落。
- 不用純聊天介面承載需要審查的工具呼叫流程。
