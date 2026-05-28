# Design System：高信任金融科技平台

## 色彩

```css
--color-bg: #F6F8FB;
--color-surface: #FFFFFF;
--color-surface-muted: #EEF3F8;
--color-surface-strong: #E6EDF5;
--color-border: #D8E1EC;
--color-border-strong: #AEBFD1;
--color-text: #0B1220;
--color-text-muted: #526173;
--color-text-subtle: #7A8797;
--color-primary: #1455D9;
--color-primary-hover: #0F46B8;
--color-primary-soft: #DCE8FF;
--color-trust: #0F766E;
--color-trust-soft: #CCFBF1;
--color-profit: #15803D;
--color-loss: #B91C1C;
--color-warning: #B7791F;
--color-warning-soft: #FEF3C7;
--color-danger: #B42318;
--color-danger-soft: #FEE4E2;
--color-info: #0369A1;
```

## 深色模式可選 token

```css
--color-bg-dark: #07111F;
--color-surface-dark: #0D1B2D;
--color-surface-muted-dark: #13243A;
--color-border-dark: #23405E;
--color-text-dark: #F8FAFC;
--color-text-muted-dark: #A8B3C2;
--color-primary-dark: #6EA8FF;
```

深色模式僅適合專業交易台或風險監控，消費者錢包預設仍建議淺色。

## 字體

- 主要字體：Inter、Noto Sans TC、system-ui。
- 金額與數字：Roboto Mono、JetBrains Mono、Inter tabular nums。
- 中文數字旁的單位需保持一致，例如 `NT$ 12,340.00`。

## 字級

| 用途 | 尺寸 | 行高 | 字重 | 備註 |
| --- | --- | --- | --- | --- |
| Account balance | 36px | 44px | 700 | 只用於核心餘額 |
| Page title | 28px | 36px | 700 | 頁面標題 |
| Section title | 18px | 28px | 700 | 區塊標題 |
| Body | 14px | 22px | 400 | 主要內容 |
| Financial caption | 12px | 18px | 600 | 幣別、手續費、時間 |
| Risk note | 13px | 20px | 500 | 風險提示 |

## 間距

- 頁面外距：桌面 32px，平板 24px，手機 16px。
- 卡片 padding：24px；金額卡可用 28px。
- 交易列高度：64px 起，需容納名稱、時間、金額、狀態。
- 表單欄位間距：18px；付款流程步驟間距 24px。
- 風險提示與確認區塊上下至少 16px。

## 圓角與陰影

```css
--radius-sm: 6px;
--radius-md: 10px;
--radius-lg: 16px;
--radius-xl: 22px;
--shadow-card: 0 1px 2px rgba(11, 18, 32, 0.06), 0 8px 24px rgba(11, 18, 32, 0.05);
--shadow-confirmation: 0 20px 50px rgba(11, 18, 32, 0.18);
```

## Layout

- 頂部列高度：72px，放帳戶切換、通知、安全狀態。
- 內容最大寬度：1200px；交易台可放寬至 1440px。
- 桌面採 12 欄 grid：左 8 欄主要金額/交易，右 4 欄風險/摘要。
- 手機順序：帳戶狀態 → 餘額 → 主要操作 → 近期交易 → 風險提示。
- 高風險流程使用 stepper，不使用單頁長表單讓使用者迷失。

## 狀態與語意

- 成功：付款完成、驗證通過、收益正向。
- 警告：待審核、即將到期、匯率變動、手續費提醒。
- 危險：交易失敗、風險阻擋、帳戶受限、刪除付款方式。
- 資訊：處理中、入帳時間、系統公告。

## 互動狀態

- Hover：卡片只加深邊框或背景，不使用放大。
- Focus：`2px` primary outline，外加 2px offset。
- Disabled：透明度 55%，但金額仍需可讀。
- Loading：金額顯示 skeleton，交易列表保留列高度。
- Confirmation：高風險操作需顯示摘要、費用、收款方、完成後不可逆說明。

## 動效

- 一般 transition：150ms ease-out。
- Dialog/Drawer：200ms ease-out。
- 金額變化可用淡入，不使用跳動或賭博感動畫。
- 尊重 `prefers-reduced-motion`。

## 禁止事項

- 不用紅綠作為唯一漲跌訊號，必須搭配 `+`、`-`、箭頭或文字。
- 不用大面積霓虹、玻璃擬態、賭場感金色特效。
- 不在付款確認前隱藏手續費與匯率。
- 不讓危險操作只靠 toast 告知，需 inline 顯示。
- 不使用 emoji 表示金錢、風險或安全。
