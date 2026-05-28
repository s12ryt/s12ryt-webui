# Design System：沉穩企業 SaaS 控制台

## 色彩

```css
--color-bg: #F8FAFC;
--color-surface: #FFFFFF;
--color-surface-muted: #F1F5F9;
--color-surface-hover: #F8FAFC;
--color-border: #E2E8F0;
--color-border-strong: #CBD5E1;
--color-text: #0F172A;
--color-text-muted: #475569;
--color-text-subtle: #64748B;
--color-primary: #2563EB;
--color-primary-hover: #1D4ED8;
--color-primary-soft: #DBEAFE;
--color-success: #16A34A;
--color-success-soft: #DCFCE7;
--color-warning: #D97706;
--color-warning-soft: #FEF3C7;
--color-danger: #DC2626;
--color-danger-soft: #FEE2E2;
--color-info: #0891B2;
--color-info-soft: #CFFAFE;
```

## 色彩使用

- Primary：每頁唯一主要行動，例如新增、儲存、送出。
- Success：啟用、完成、正常。
- Warning：待處理、即將到期、需要注意。
- Danger：停用、刪除、失敗、風險。
- Neutral：草稿、未知、無資料。

## 字體

- 主要字體：Inter、Noto Sans TC、system-ui。
- 數字字體：Inter tabular nums 或 Roboto Mono，只用在指標、金額、代碼、ID。
- 長表格欄位避免使用過細字重。

## 字級

| 用途 | 尺寸 | 行高 | 字重 | 備註 |
| --- | --- | --- | --- | --- |
| Page title | 28px | 36px | 700 | 頁面主標 |
| Section title | 20px | 28px | 700 | 區塊標題 |
| Card title | 16px | 24px | 600 | 卡片標題 |
| Table body | 14px | 22px | 400 | 表格內容 |
| Body | 14px | 22px | 400 | 一般內容 |
| Caption | 12px | 18px | 500 | 輔助資訊 |
| Metadata | 12px | 18px | 600 | ID、時間、狀態 |

## 間距

- 頁面外距：桌面 32px，平板 24px，手機 16px。
- 卡片 padding：20px 或 24px。
- 表單欄位間距：16px。
- 區塊間距：24px-32px。
- 工具列高度：48px-56px。
- 表格列高：52px 起，密集模式可 44px。

## 圓角與陰影

```css
--radius-sm: 6px;
--radius-md: 10px;
--radius-lg: 14px;
--radius-xl: 18px;
--shadow-card: 0 1px 2px rgba(15, 23, 42, 0.06);
--shadow-popover: 0 12px 32px rgba(15, 23, 42, 0.14);
--shadow-modal: 0 24px 64px rgba(15, 23, 42, 0.20);
```

## Layout

- 側邊欄寬度：260px；可收合成 72px icon rail。
- 頂部列高度：64px。
- 內容最大寬度：通常不限制，但需保留 24px 以上 padding；表單頁可限制 960px。
- Dashboard 採 12 欄 grid；桌面 3-4 欄 KPI，平板 2 欄，手機 1 欄。
- Detail page 可使用主內容 8 欄 + metadata panel 4 欄。
- Settings 使用左側 settings nav + 右側內容。

## 互動狀態

- Hover：背景加深一階或 border 改 primary-soft。
- Active：使用 primary-soft 與 primary text。
- Focus：使用 `2px` primary outline，需清楚可見。
- Disabled：opacity 50%，cursor not-allowed，但文字仍需可讀。
- Loading：按鈕顯示 spinner，資料區顯示 skeleton。
- Selected：表格列使用 primary-soft 背景與左側標記。

## 動效

- 一般 transition：150ms ease-out。
- Dialog/Drawer：180ms-220ms ease-out。
- 表格 hover 不使用 scale。
- 尊重 `prefers-reduced-motion`。

## 可及性

- 表單欄位必須有 label。
- 表格排序狀態需可被輔助科技理解。
- Icon button 必須有 aria-label。
- 狀態不可只用顏色，需搭配文字或 icon。

## 禁止事項

- 不使用高飽和大面積漸層。
- 不用過重陰影或玻璃擬態。
- 不在資料表格內使用過多顏色。
- 不用 emoji 當狀態圖示。
- 不把主要 CTA 放在每個卡片上造成視覺噪音。
