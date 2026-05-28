# Design System：知識庫文件中心

## 色彩

```css
--color-bg: #FFFFFF;
--color-surface: #FFFFFF;
--color-surface-muted: #F8FAFC;
--color-surface-code: #0F172A;
--color-border: #E2E8F0;
--color-border-strong: #CBD5E1;
--color-text: #0F172A;
--color-text-muted: #475569;
--color-text-subtle: #64748B;
--color-primary: #2563EB;
--color-primary-hover: #1D4ED8;
--color-primary-soft: #DBEAFE;
--color-success: #16A34A;
--color-warning: #D97706;
--color-danger: #DC2626;
--color-info: #0891B2;
--color-callout-note: #EFF6FF;
--color-callout-warning: #FFFBEB;
--color-callout-danger: #FEF2F2;
```

## 字體

- 主要字體：Inter、Noto Sans TC、system-ui。
- 文章內文：Noto Sans TC，保持高可讀性。
- 程式碼：JetBrains Mono、Roboto Mono、Consolas。

## 字級

| 用途 | 尺寸 | 行高 | 字重 | 備註 |
| --- | --- | --- | --- | --- |
| Article H1 | 36px | 46px | 750 | 文章標題 |
| Article H2 | 26px | 36px | 700 | 主章節 |
| Article H3 | 20px | 30px | 700 | 子章節 |
| Body | 16px | 30px | 400 | 長文閱讀 |
| UI text | 14px | 22px | 500 | 導航與搜尋 |
| Code | 13px | 22px | 400 | 程式碼 |
| Caption | 12px | 18px | 500 | 版本、更新時間 |

## 間距

- Article max width：720px-820px。
- 文件 shell gap：32px。
- 段落間距：16px。
- H2 上方間距：40px，下方 16px。
- Code block padding：16px-20px。
- Callout padding：16px。

## 圓角與陰影

```css
--radius-sm: 6px;
--radius-md: 10px;
--radius-lg: 14px;
--shadow-search: 0 18px 48px rgba(15, 23, 42, 0.18);
--shadow-card: 0 1px 2px rgba(15, 23, 42, 0.05);
```

文章主體不使用大量陰影，讓閱讀保持安靜。

## Layout

- Top bar：64px，含 logo、搜尋、版本、主要連結。
- Left sidebar：280px，顯示文件樹。
- Article：720px-820px。
- Right TOC：220px，顯示本頁章節。
- 1200px 以下可隱藏右 TOC；768px 以下左側目錄改 drawer。
- 搜尋 modal 可覆蓋中央，支援鍵盤。

## 文章排版

- H2/H3 需有錨點連結。
- 列表縮排一致。
- Table 可水平捲動，但頁面不整體水平捲動。
- Code block 有語言標籤與 copy button。
- Callout 分 note、tip、warning、danger。

## 互動狀態

- 搜尋 focus 明顯，支援 `Ctrl/Cmd + K`。
- Sidebar active item 使用 primary 左邊框或背景。
- TOC active item 跟隨捲動。
- Copy code 成功顯示短文字，不只 icon 變化。
- Broken link 或無權限內容需 inline 說明。

## 動效

- 搜尋 modal：160ms fade/scale。
- Sidebar 展開：150ms。
- Anchor scroll 可 smooth，但尊重 reduced motion。

## 禁止事項

- 不讓文章寬度超過 900px 導致難讀。
- 不在長文中使用過多彩色卡片。
- 不用 emoji 作為 callout icon。
- 不只顯示 icon，不提供文字標籤。
- 不把版本警告藏在頁尾。
