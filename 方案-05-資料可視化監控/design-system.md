# Design System：資料可視化監控

## 色彩

```css
--color-bg: #0F172A;
--color-surface: #111C33;
--color-surface-soft: #16213A;
--color-border: #24314D;
--color-text: #E2E8F0;
--color-text-muted: #94A3B8;
--color-primary: #38BDF8;
--color-success: #22C55E;
--color-warning: #F59E0B;
--color-danger: #EF4444;
--color-info: #8B5CF6;
```

## 原則

- 顏色用於狀態與比較，不做純裝飾。
- 圖表色盤需固定，避免每頁改變造成認知負擔。
- 深色背景上文字對比要足夠。

## 字體

- UI：Inter、Noto Sans TC、system-ui。
- 數字與時間：Inter、Roboto Mono、ui-monospace。

## 字級

| 用途 | 尺寸 | 行高 | 字重 |
| --- | --- | --- | --- |
| Dashboard title | 28px | 36px | 700 |
| Metric value | 32px | 40px | 800 |
| Metric label | 12px | 18px | 600 |
| Table body | 13px | 20px | 400 |
| Chart annotation | 12px | 16px | 500 |

## Layout

- Dashboard grid：12 欄。
- KPI：4 欄或 3 欄。
- Chart：6 欄或 8 欄。
- Alert panel：3 欄或 4 欄。
- Mobile：先顯示 KPI + 核心告警，再降級圖表。

## 圖表規則

- 一張圖只回答一個問題。
- 線圖、長條圖、堆疊圖、熱力圖分工明確。
- 避免在同一圖中放太多維度。
- Tooltip 需顯示完整數值與時間範圍。

## 禁止事項

- 不要把所有資訊都變成紅黃綠。
- 不要用純裝飾動畫干擾讀數。
- 不要過度依賴圓餅圖。
- 不要讓圖表圖例太小或對比不足。
