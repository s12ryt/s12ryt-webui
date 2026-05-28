# Design System：品牌行銷 Landing

## 設計目標

品牌行銷 Landing 的設計目標是建立第一印象、傳達價值、累積信任並推動轉換。視覺可以更有張力，但所有裝飾都必須服務於訊息與 CTA。

## 色彩 Token

```css
--color-bg: #FAFAFF;
--color-bg-soft: #F5F3FF;
--color-surface: #FFFFFF;
--color-surface-tinted: #F8FAFC;
--color-text: #111827;
--color-text-muted: #4B5563;
--color-text-subtle: #6B7280;
--color-primary: #7C3AED;
--color-primary-hover: #6D28D9;
--color-primary-soft: #EDE9FE;
--color-secondary: #06B6D4;
--color-secondary-soft: #CFFAFE;
--color-accent: #F97316;
--color-accent-soft: #FFEDD5;
--color-success: #10B981;
--color-warning: #F59E0B;
--color-danger: #EF4444;
--color-border: #E5E7EB;
--gradient-hero: linear-gradient(135deg, #7C3AED 0%, #06B6D4 55%, #F97316 100%);
--gradient-soft: radial-gradient(circle at top left, rgba(124, 58, 237, 0.16), transparent 34%), radial-gradient(circle at top right, rgba(6, 182, 212, 0.14), transparent 32%);
```

## 色彩使用規則

- Primary CTA 全站一致，不可每區換色。
- Secondary 可用於輔助 CTA、連結、產品截圖 highlight。
- Accent 只用於重點標籤、活動亮點、價格促銷，不可濫用。
- 漸層只作為 hero 或 CTA 區背景，不要每個卡片都套漸層。
- 文字對比永遠優先於炫目背景。

## 字體

- 標題：Plus Jakarta Sans、Inter、Noto Sans TC。
- 內文：Inter、Noto Sans TC、system-ui。
- 若品牌需要更強個性，可使用 display font，但中文長文仍以 Noto Sans TC 為主。

## 字級

| 用途 | 桌面尺寸 | 行高 | 手機尺寸 | 字重 |
| --- | --- | --- | --- | --- |
| Hero title | 56px-72px | 1.08 | 36px-44px | 800 |
| Hero subtitle | 20px | 32px | 17px | 400 |
| Section title | 40px-48px | 1.15 | 30px-34px | 750 |
| Section subtitle | 18px | 30px | 16px | 400 |
| Card title | 20px | 28px | 18px | 700 |
| Body | 16px | 26px | 15px | 400 |
| Eyebrow | 13px | 18px | 12px | 700 |

## Layout

- Container：max-width 1120px-1240px。
- Section padding：桌面 88px-120px，手機 56px-72px。
- Hero：至少 680px 或首屏 80vh；短 Landing 可降低到 560px。
- Navbar：可使用 floating pill 或簡潔 top nav。
- Section 之間要有節奏變化：純文字、圖文、卡片、數據、CTA 交替。

## Hero 規則

- 主標題不超過兩行半。
- 副標必須說明「給誰、解決什麼、得到什麼」。
- Primary CTA + Secondary CTA 最多兩個。
- Hero visual 可以是產品截圖、抽象圖、流程圖或影片預覽。
- 首屏需出現信任訊號，例如使用者數、客戶 logo、安全標章或低風險文案。

## 圓角與陰影

```css
--radius-sm: 10px;
--radius-md: 14px;
--radius-lg: 24px;
--radius-xl: 32px;
--radius-pill: 999px;
--shadow-feature: 0 20px 60px rgba(17, 24, 39, 0.12);
--shadow-cta: 0 16px 40px rgba(124, 58, 237, 0.24);
--shadow-card-hover: 0 18px 48px rgba(17, 24, 39, 0.10);
```

## 視覺元素

- 可使用漸層 blob、產品截圖、抽象線條、裝飾 grid。
- 每個大區塊需要一個視覺焦點。
- 圖示必須使用一致 SVG icon set。
- 產品截圖需放在 browser frame 或 device frame 中，避免漂浮無上下文。

## 互動

- CTA hover 使用顏色與陰影，不使用劇烈 scale。
- Anchor navigation 需 smooth scroll，但尊重 reduced motion。
- Pricing toggle、FAQ accordion、feature tabs 需保留鍵盤操作。
- 表單送出需有 loading、success、error、privacy note。

## RWD

- Mobile hero CTA 必須在首屏可見。
- Logo wall 在手機可改水平捲動或 2 欄 grid。
- Feature card 從 3 欄降到 1 欄。
- Pricing card 手機按推薦方案優先排序。

## 禁止事項

- 不要每個區塊都使用不同漸層。
- 不要讓 hero 標題超過兩行半。
- 不要用模糊空泛文案，例如「最佳解決方案」但沒有具體說明。
- 不要為了炫技犧牲載入速度與可讀性。
- 不要讓 CTA 文案不一致。
- 不要使用 emoji 作為正式 icon。
