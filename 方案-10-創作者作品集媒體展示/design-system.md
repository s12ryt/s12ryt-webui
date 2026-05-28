# Design System：創作者作品集媒體展示

## 色彩

```css
--color-bg: #0B0B0F;
--color-surface: #14141B;
--color-surface-muted: #1E1E27;
--color-border: #2A2A36;
--color-border-soft: rgba(255, 255, 255, 0.10);
--color-text: #FAFAFA;
--color-text-muted: #B7B7C2;
--color-text-subtle: #858596;
--color-primary: #F4C95D;
--color-primary-hover: #EAB308;
--color-primary-soft: rgba(244, 201, 93, 0.16);
--color-accent: #A78BFA;
--color-accent-soft: rgba(167, 139, 250, 0.16);
--color-success: #22C55E;
--color-warning: #F59E0B;
--color-danger: #EF4444;
--color-info: #38BDF8;
```

## 淺色替代

```css
--color-bg-light: #FAF7F2;
--color-surface-light: #FFFFFF;
--color-text-light: #171717;
--color-text-muted-light: #525252;
--color-border-light: #E7E0D6;
--color-primary-light: #9A5B00;
```

預設深色較適合攝影、影像、藝術展示；若作品本身很暗，可改淺色背景避免視覺疲勞。

## 字體

- 標題：Playfair Display、Fraunces、Noto Serif TC 或同等高辨識 serif。
- 內文：Inter、Noto Sans TC、system-ui。
- Meta：Inter uppercase 或小字重。

## 字級

| 用途 | 尺寸 | 行高 | 字重 | 備註 |
| --- | --- | --- | --- | --- |
| Hero title | 64px-96px | 1.0-1.08 | 700 | 桌面大標 |
| Page title | 44px | 52px | 700 | 一般頁標題 |
| Case title | 34px | 44px | 700 | 案例頁 |
| Section title | 24px | 34px | 650 | 區塊 |
| Body | 16px | 28px | 400 | 內文 |
| Meta | 12px | 18px | 600 | 年份、角色、分類 |

手機 Hero title 可降至 42px-52px。

## 間距

- 桌面 section spacing：96px-144px。
- 手機 section spacing：56px-80px。
- Gallery gap：16px-28px，依作品比例調整。
- Case study block 間距：64px。
- 文字與媒體間距：24px-40px。

## 圓角與陰影

```css
--radius-sm: 8px;
--radius-md: 16px;
--radius-lg: 28px;
--radius-xl: 40px;
--shadow-media: 0 24px 80px rgba(0, 0, 0, 0.35);
--shadow-overlay: 0 30px 90px rgba(0, 0, 0, 0.55);
```

## Layout

- 最大內容寬度：1200px-1440px。
- Hero 可全螢幕或 80vh，但手機不強制滿版。
- Gallery 可使用 masonry 感，但實作需避免 layout shift。
- Case study 使用交錯媒體與文字，避免每段都同版型。
- 導覽可極簡，但主要頁面入口需清楚。

## 媒體規則

- 所有圖片需設定寬高或 aspect ratio。
- 大圖使用漸進載入或 skeleton。
- 影片預設靜音，需清楚播放控制。
- Lightbox 需支援鍵盤 Esc 關閉與左右切換。
- Alt 需描述作品，不寫「作品圖片」。

## 互動狀態

- Hover：媒體可淡入 overlay 與 metadata，不改變尺寸。
- Focus：在深色背景下使用高對比 outline。
- Loading：圖片區塊保留比例。
- Disabled：CTA 降低對比但文字仍可讀。

## 動效

- 頁面 section 淡入：300ms-500ms，但需可關閉。
- 媒體 hover：180ms。
- Lightbox：220ms。
- 不使用無限循環晃動或過度 parallax。

## 禁止事項

- 不讓美術字體用在大段中文內文。
- 不因追求沉浸而隱藏導覽與聯絡入口。
- 不使用 emoji 當作品分類或 CTA icon。
- 不讓圖片未定尺寸造成跳動。
- 不讓動效阻礙作品瀏覽。
