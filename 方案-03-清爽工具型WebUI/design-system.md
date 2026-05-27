# Design System：清爽工具型 WebUI

## 色彩

```css
--color-bg: #FFFFFF;
--color-bg-subtle: #F8FAFC;
--color-surface: #FFFFFF;
--color-border: #E5E7EB;
--color-text: #111827;
--color-text-muted: #6B7280;
--color-primary: #0EA5E9;
--color-primary-hover: #0284C7;
--color-primary-soft: #E0F2FE;
--color-success: #10B981;
--color-warning: #F59E0B;
--color-danger: #EF4444;
```

## 字體

- 主要字體：Inter、Noto Sans TC、system-ui。
- 單行輸出或技術內容：JetBrains Mono、ui-monospace。

## 字級

| 用途 | 尺寸 | 行高 | 字重 |
| --- | --- | --- | --- |
| Hero title | 32px | 40px | 750 |
| Tool title | 22px | 30px | 700 |
| Label | 14px | 20px | 600 |
| Body | 14px | 24px | 400 |
| Helper | 13px | 20px | 400 |

## Layout

- 最大寬度：960px 或 1120px。
- 頁面上方留白：48px-72px。
- 工具主卡片：單欄或左右雙欄。
- mobile：所有輸入輸出改單欄。

## 圓角與陰影

```css
--radius-sm: 8px;
--radius-md: 12px;
--radius-lg: 20px;
--shadow-soft: 0 8px 24px rgba(15, 23, 42, 0.06);
```

## 互動

- 主要 CTA 清楚但不刺眼。
- Copy 成功要有短暫 toast 或 inline feedback。
- Reset / Clear 需避免誤按，可使用 secondary 樣式。
- 錯誤訊息靠近欄位，不要只用 toast。

## 禁止事項

- 不要塞滿整頁資訊。
- 不要一開始就顯示太多進階設定。
- 不要使用厚重側邊欄。
- 不要把結果藏在頁面很下方。
