# Design System：清爽工具型 WebUI

## 設計目標

清爽工具型 WebUI 必須讓使用者快速完成單一任務。設計的優先順序是清楚、可操作、可驗證、可複製，而不是品牌敘事或資料展示。

## 色彩 Token

```css
--color-bg: #FFFFFF;
--color-bg-subtle: #F8FAFC;
--color-bg-muted: #F1F5F9;
--color-surface: #FFFFFF;
--color-surface-hover: #F8FAFC;
--color-border: #E5E7EB;
--color-border-strong: #CBD5E1;
--color-text: #111827;
--color-text-muted: #6B7280;
--color-text-subtle: #94A3B8;
--color-primary: #0EA5E9;
--color-primary-hover: #0284C7;
--color-primary-soft: #E0F2FE;
--color-success: #10B981;
--color-success-soft: #D1FAE5;
--color-warning: #F59E0B;
--color-warning-soft: #FEF3C7;
--color-danger: #EF4444;
--color-danger-soft: #FEE2E2;
--color-code-bg: #0F172A;
--color-code-text: #E2E8F0;
```

## 色彩使用規則

- 主背景白色，工具卡片使用白底或極淡灰底。
- Primary 只用於主操作，例如轉換、產生、查詢。
- Danger 用於清空、刪除、無法復原或驗證失敗。
- Success 用於可複製結果、完成轉換、下載完成。
- Warning 用於輸入不完整、格式可疑、可能遺失資訊。

## 字體

- 主要字體：Inter、Noto Sans TC、system-ui。
- 技術輸入輸出：JetBrains Mono、Roboto Mono、ui-monospace。
- 不建議使用太有個性的 display font，以免降低工具可信度。

## 字級

| 用途 | 尺寸 | 行高 | 字重 | 備註 |
| --- | --- | --- | --- | --- |
| Page title | 34px | 42px | 750 | 單頁工具主標題 |
| Tool title | 22px | 30px | 700 | 工具卡片標題 |
| Section title | 16px | 24px | 650 | 區塊標題 |
| Label | 14px | 20px | 600 | 欄位標籤 |
| Body | 14px | 24px | 400 | 一般說明 |
| Helper | 13px | 20px | 400 | 補充文字 |
| Code / output | 13px | 22px | 400 | 結果區 |

## Layout

### 單頁工具

- Page container：max-width 960px 或 1120px。
- Page top spacing：48px-72px。
- Tool card：單欄或左右雙欄。
- Intro：一句價值主張 + 一句具體說明，不要長篇文案。
- Footer：版本、隱私、回饋連結即可。

### 左右雙欄工具

- 左欄輸入：45%-50%。
- 右欄輸出：50%-55%。
- 中間 gap：20px-28px。
- 低於 768px 全部改單欄，輸出在輸入下方。

### 設定型工具

- 分組使用 card section。
- Sticky action bar 可放在底部或表單右上。
- 進階選項使用 accordion，不預設展開。

## 間距與尺寸

```css
--radius-sm: 8px;
--radius-md: 12px;
--radius-lg: 20px;
--radius-xl: 28px;
--shadow-soft: 0 8px 24px rgba(15, 23, 42, 0.06);
--shadow-focus: 0 0 0 4px rgba(14, 165, 233, 0.16);
```

- Tool card padding：桌面 24px-32px，手機 18px-20px。
- Textarea 最小高度：160px-240px。
- Output 最小高度：160px，避免結果區跳動。
- 表單欄位垂直間距：14px-18px。

## 表單規則

- label 必須可見，不只依賴 placeholder。
- placeholder 使用真實範例。
- 錯誤訊息靠近欄位，不只用 toast。
- 必填與選填要明確標示。
- 長輸入應提供清空、貼上、載入範例。

## 狀態規則

| 狀態 | 視覺 | 說明 |
| --- | --- | --- |
| empty | 淡灰提示區 | 告知輸入後會產生什麼 |
| typing | focus ring | 使用者正在輸入 |
| validating | 小型 spinner | 驗證格式或檔案 |
| processing | button loading + output skeleton | 正在轉換或產生 |
| success | success inline feedback | 可複製或下載 |
| warning | warning helper | 結果可用但需注意 |
| error | danger inline message | 指出問題與修正方式 |
| disabled | 降低透明度但仍可讀 | 說明不可操作原因 |

## 互動

- 主要 CTA 清楚但不刺眼。
- Copy 成功需有短暫 toast 或 inline feedback。
- Reset / Clear 使用 secondary 或 danger ghost，避免誤按。
- Download、Copy、Share 放在輸出區右上。
- 進階設定變更後應立即反映，或清楚標示需重新執行。

## 動效

- Hover 使用顏色、border、陰影微調，不使用會造成 layout shift 的 scale。
- Loading skeleton 保持穩定，不閃爍。
- Toast 200ms 內淡入淡出。
- 尊重 `prefers-reduced-motion`。

## 禁止事項

- 不要塞滿整頁資訊。
- 不要一開始就顯示太多進階設定。
- 不要使用厚重側邊欄。
- 不要把結果藏在頁面很下方。
- 不要只用 placeholder 取代 label。
- 不要把錯誤訊息只放在頁面頂部。
- 不要用 emoji 當正式 UI icon。
