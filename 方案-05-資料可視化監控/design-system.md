# Design System：資料可視化監控

## 設計目標

資料可視化監控的核心是快速判斷狀態、理解趨勢、定位異常並採取行動。設計上必須控制資訊密度、圖表語意、狀態色與時間範圍一致性。

## 色彩 Token

```css
--color-bg: #0F172A;
--color-bg-deep: #020617;
--color-surface: #111C33;
--color-surface-soft: #16213A;
--color-surface-hover: #1E293B;
--color-border: #24314D;
--color-border-strong: #334155;
--color-text: #E2E8F0;
--color-text-muted: #94A3B8;
--color-text-subtle: #64748B;
--color-primary: #38BDF8;
--color-primary-soft: rgba(56, 189, 248, 0.12);
--color-success: #22C55E;
--color-success-soft: rgba(34, 197, 94, 0.12);
--color-warning: #F59E0B;
--color-warning-soft: rgba(245, 158, 11, 0.14);
--color-danger: #EF4444;
--color-danger-soft: rgba(239, 68, 68, 0.14);
--color-critical: #DC2626;
--color-info: #8B5CF6;
--color-info-soft: rgba(139, 92, 246, 0.12);
```

## 可選淺色模式

```css
--color-bg-light: #F8FAFC;
--color-surface-light: #FFFFFF;
--color-border-light: #E2E8F0;
--color-text-light: #0F172A;
--color-text-muted-light: #475569;
```

淺色模式適合報表與管理層簡報；深色模式適合長時間監控與 NOC。

## 圖表色盤

```css
--chart-blue: #38BDF8;
--chart-purple: #A78BFA;
--chart-green: #34D399;
--chart-yellow: #FBBF24;
--chart-orange: #FB923C;
--chart-red: #F87171;
--chart-slate: #94A3B8;
```

規則：

- 同一指標在不同頁面必須使用同一顏色。
- 成功、警告、危險色優先保留給狀態，不用於一般分類。
- 圖例、tooltip、axis label 對比要足夠。

## 字體

- UI：Inter、Noto Sans TC、system-ui。
- 數字與時間：Inter、Roboto Mono、ui-monospace。
- Log：JetBrains Mono、ui-monospace。

## 字級

| 用途 | 尺寸 | 行高 | 字重 | 備註 |
| --- | --- | --- | --- | --- |
| Dashboard title | 28px | 36px | 700 | 頁面標題 |
| Metric value | 32px-40px | 1.1 | 800 | KPI 數值 |
| Metric label | 12px | 18px | 650 | 指標名稱 |
| Delta | 12px | 18px | 700 | 變化量 |
| Table body | 13px | 20px | 400 | 高密度列表 |
| Chart annotation | 12px | 16px | 500 | 圖表標註 |
| Timestamp | 12px | 18px | 500 | 時間、last updated |

## Layout

- Dashboard grid：12 欄。
- KPI：4 欄或 3 欄，手機改 1-2 欄。
- Chart：6 欄或 8 欄。
- Alert panel：3 欄或 4 欄。
- Timeline / table：通常全寬或 8 欄。
- Mobile：先顯示 KPI + 核心告警，再降級圖表。

## 圖表規則

- 一張圖只回答一個問題。
- 線圖用於趨勢。
- 長條圖用於比較。
- 堆疊圖用於組成與總量變化。
- 熱力圖用於時間 x 維度密度。
- 散點圖用於關聯與異常值。
- 圓餅圖只用於少量分類且不需精準比較。
- Tooltip 需顯示完整數值、單位、時間範圍。

## 狀態規則

| 狀態 | 顏色 | 規則 |
| --- | --- | --- |
| healthy | success | 明確標示正常與最新更新時間 |
| degraded | warning | 顯示影響範圍與建議觀察 |
| incident | danger | 顯示嚴重度、開始時間、處理入口 |
| critical | critical | 最高層級，不可被其他裝飾稀釋 |
| unknown | muted | 說明資料缺失或尚未回報 |
| stale | warning soft | 顯示資料過期時間 |

狀態不可只用顏色，需搭配文字、icon、badge 或形狀。

## Refresh / Time Range

- 全頁時間範圍需清楚可見。
- 自動刷新與手動刷新都要顯示。
- Last updated 必須出現在 dashboard header 或 chart footer。
- 資料陳舊時使用 stale banner。
- 不同圖表若時間範圍不同，需明確標示。

## 互動

- Hover chart data point 顯示 tooltip。
- 點擊 KPI 可 drill-down 到相關頁。
- Filter 改變後需要 loading 或 skeleton。
- Export 前需說明範圍與格式。
- 高危告警操作需確認。

## 禁止事項

- 不要把所有資訊都變成紅黃綠。
- 不要用純裝飾動畫干擾讀數。
- 不要過度依賴圓餅圖。
- 不要讓圖表圖例太小或對比不足。
- 不要隱藏時間範圍與資料來源。
- 不要使用 emoji 作為告警 icon。
