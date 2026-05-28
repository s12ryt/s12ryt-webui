# Design System：社群內容與論壇平台

## 色彩

```css
--color-bg: #F7F8FB;
--color-surface: #FFFFFF;
--color-surface-muted: #F1F5F9;
--color-surface-hover: #EEF2F7;
--color-border: #E2E8F0;
--color-border-strong: #CBD5E1;
--color-text: #0F172A;
--color-text-muted: #475569;
--color-text-subtle: #64748B;
--color-primary: #7C3AED;
--color-primary-hover: #6D28D9;
--color-primary-soft: #EDE9FE;
--color-accent: #0891B2;
--color-accent-soft: #CFFAFE;
--color-success: #16A34A;
--color-warning: #D97706;
--color-danger: #DC2626;
--color-info: #2563EB;
--color-reaction: #F59E0B;
```

## 字體

- 主要字體：Inter、Noto Sans TC、system-ui。
- 長文內容：Noto Sans TC 或思源黑體，行高需較寬。
- 代碼討論可使用 JetBrains Mono 或 Roboto Mono。

## 字級

| 用途 | 尺寸 | 行高 | 字重 | 備註 |
| --- | --- | --- | --- | --- |
| Feed title | 20px | 30px | 700 | 貼文標題 |
| Thread title | 28px | 38px | 700 | 討論串詳情 |
| Body | 15px | 26px | 400 | 貼文內容 |
| Comment body | 14px | 23px | 400 | 留言 |
| Meta | 12px | 18px | 500 | 作者、時間、社群 |
| Count | 13px | 18px | 600 | 互動數 |

## 間距

- Feed 容器寬度：640px-760px，避免長文過寬。
- 右側趨勢欄：320px，可在平板以下隱藏。
- Feed item padding：18px-22px。
- 留言縮排：16px-24px，不超過 3 層視覺縮排。
- 內容段落間距：12px-16px。

## 圓角與陰影

```css
--radius-sm: 8px;
--radius-md: 14px;
--radius-lg: 20px;
--radius-pill: 999px;
--shadow-card: 0 1px 2px rgba(15, 23, 42, 0.05);
--shadow-composer: 0 12px 32px rgba(15, 23, 42, 0.12);
```

## Layout

- Desktop：左 nav 240px，中間 feed 680px，右側 trends 320px。
- Tablet：左 nav 收合成 icon rail，中間 feed 佔主要寬度。
- Mobile：底部導覽或頂部 tabs，composer 可 sticky bottom。
- 討論串詳情：主內容 + 右側目錄/相關討論，可在小螢幕收合。

## 內容樣式

- 貼文內連結使用 primary，hover underline。
- 引用區塊使用左邊框與 muted background。
- code inline 使用 muted surface，不用高彩背景。
- 圖片與媒體需有固定最大高度與圓角。

## 互動狀態

- Reaction hover：背景 primary-soft 或 reaction-soft，不放大推擠。
- Active reaction：顯示實心 icon 與數字強調。
- Focus：清楚 outline，composer toolbar 可鍵盤操作。
- Loading：Feed 使用 skeleton card。
- Muted/Blocked：內容降低對比並顯示原因。

## 動效

- Reaction 切換：120ms color/background transition。
- Composer 展開：180ms ease-out。
- 新通知 badge：淡入，不使用持續跳動。
- 尊重 `prefers-reduced-motion`。

## 禁止事項

- 不使用 emoji 取代正式 reaction icon；若產品允許 emoji reaction，需作為內容功能而非 UI icon。
- 不讓互動數字比內容標題更顯眼。
- 不在每則貼文使用過重陰影。
- 不讓多層留言無限縮排導致手機不可讀。
- 不只用顏色標示檢舉/封鎖狀態。
