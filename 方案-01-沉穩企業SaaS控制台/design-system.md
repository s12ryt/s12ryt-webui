# Design System：沉穩企業 SaaS 控制台

## 色彩

```css
--color-bg: #F8FAFC;
--color-surface: #FFFFFF;
--color-surface-muted: #F1F5F9;
--color-border: #E2E8F0;
--color-text: #0F172A;
--color-text-muted: #475569;
--color-primary: #2563EB;
--color-primary-hover: #1D4ED8;
--color-primary-soft: #DBEAFE;
--color-success: #16A34A;
--color-warning: #D97706;
--color-danger: #DC2626;
--color-info: #0891B2;
```

## 字體

- 主要字體：Inter、Noto Sans TC、system-ui。
- 數字字體：Inter 或 Roboto Mono，只用在指標、金額、代碼。

## 字級

| 用途 | 尺寸 | 行高 | 字重 |
| --- | --- | --- | --- |
| Page title | 28px | 36px | 700 |
| Section title | 20px | 28px | 700 |
| Card title | 16px | 24px | 600 |
| Body | 14px | 22px | 400 |
| Caption | 12px | 18px | 500 |

## 間距

- 頁面外距：24px / 32px。
- 卡片 padding：20px 或 24px。
- 表單欄位間距：16px。
- 區塊間距：24px。

## 圓角與陰影

```css
--radius-sm: 6px;
--radius-md: 10px;
--radius-lg: 14px;
--shadow-card: 0 1px 2px rgba(15, 23, 42, 0.06);
--shadow-popover: 0 12px 32px rgba(15, 23, 42, 0.14);
```

## Layout

- 側邊欄寬度：260px。
- 頂部列高度：64px。
- 內容最大寬度：視資料密度決定，通常不限制，但需有 24px 以上 padding。
- 卡片採 12 欄 grid；桌面 3-4 欄 KPI，平板 2 欄，手機 1 欄。

## 互動狀態

- Hover：背景加深一階或 border 改 primary-soft。
- Focus：使用 `2px` primary outline，需清楚可見。
- Disabled：opacity 50%，cursor not-allowed。
- Loading：按鈕顯示 spinner，資料區顯示 skeleton。

## 禁止事項

- 不使用高飽和大面積漸層。
- 不用過重陰影或玻璃擬態。
- 不在資料表格內使用過多顏色。
- 不用 emoji 當狀態圖示。
