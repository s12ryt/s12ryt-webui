# Design System：品牌行銷 Landing

## 色彩

```css
--color-bg: #FAFAFF;
--color-surface: #FFFFFF;
--color-text: #111827;
--color-text-muted: #4B5563;
--color-primary: #7C3AED;
--color-primary-hover: #6D28D9;
--color-secondary: #06B6D4;
--color-accent: #F97316;
--color-border: #E5E7EB;
--gradient-hero: linear-gradient(135deg, #7C3AED 0%, #06B6D4 55%, #F97316 100%);
```

## 字體

- 標題：Plus Jakarta Sans、Inter、Noto Sans TC。
- 內文：Inter、Noto Sans TC、system-ui。

## 字級

| 用途 | 尺寸 | 行高 | 字重 |
| --- | --- | --- | --- |
| Hero title | 56px | 64px | 800 |
| Hero title mobile | 36px | 44px | 800 |
| Section title | 40px | 48px | 750 |
| Card title | 20px | 28px | 700 |
| Body large | 18px | 30px | 400 |
| Body | 16px | 26px | 400 |

## Layout

- Container：max-width 1200px。
- Section padding：桌面 96px，手機 56px。
- Hero 高度：至少 680px 或首屏 80vh。
- Navbar：可使用 floating pill 或簡潔 top nav。

## 圓角與陰影

```css
--radius-md: 14px;
--radius-lg: 24px;
--radius-xl: 32px;
--shadow-feature: 0 20px 60px rgba(17, 24, 39, 0.12);
--shadow-cta: 0 16px 40px rgba(124, 58, 237, 0.24);
```

## 視覺元素

- 可使用漸層 blob、產品截圖、抽象線條。
- 每個大區塊需要一個視覺焦點。
- CTA 顏色需在頁面中一致。

## 禁止事項

- 不要每個區塊都使用不同漸層。
- 不要讓 hero 標題超過兩行半。
- 不要用模糊空泛文案，例如「最佳解決方案」但沒有具體說明。
- 不要為了炫技犧牲載入速度與可讀性。
