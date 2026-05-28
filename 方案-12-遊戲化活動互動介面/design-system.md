# Design System：遊戲化活動互動介面

## 色彩

```css
--color-bg: #17122B;
--color-surface: #241A42;
--color-surface-muted: #302255;
--color-border: rgba(255, 255, 255, 0.14);
--color-border-strong: rgba(255, 255, 255, 0.24);
--color-text: #FFFFFF;
--color-text-muted: #D7D0F4;
--color-text-subtle: #A99FD0;
--color-primary: #F97316;
--color-primary-hover: #EA580C;
--color-primary-soft: rgba(249, 115, 22, 0.18);
--color-accent: #A3E635;
--color-accent-soft: rgba(163, 230, 53, 0.18);
--color-reward: #FACC15;
--color-reward-soft: rgba(250, 204, 21, 0.18);
--color-success: #22C55E;
--color-warning: #F59E0B;
--color-danger: #F43F5E;
--color-info: #38BDF8;
```

## 淺色活動替代

```css
--color-bg-light: #FFF7ED;
--color-surface-light: #FFFFFF;
--color-text-light: #1F2937;
--color-primary-light: #EA580C;
--color-accent-light: #65A30D;
--color-reward-light: #CA8A04;
```

深色適合大型活動與沉浸任務；淺色適合一般會員中心或教育型挑戰。

## 字體

- 標題：Inter、Noto Sans TC，字重 800；可搭配圓潤 display font，但中文需可讀。
- 內文：Inter、Noto Sans TC、system-ui。
- 數字/積分：Inter tabular nums 或 Roboto Mono。

## 字級

| 用途 | 尺寸 | 行高 | 字重 | 備註 |
| --- | --- | --- | --- | --- |
| Event title | 48px-72px | 1.05 | 800 | 活動主標 |
| Mission title | 18px | 26px | 750 | 任務卡 |
| Reward number | 32px | 40px | 800 | 積分、獎勵 |
| Body | 14px | 22px | 500 | 說明 |
| Rule text | 13px | 21px | 500 | 規則 |
| Caption | 12px | 18px | 600 | 倒數、限制 |

## 間距

- Event hero padding：桌面 72px-96px，手機 40px-56px。
- Mission grid gap：16px-24px。
- Reward card padding：20px-24px。
- 排行榜列高：56px-72px。
- 規則區塊需有足夠留白，避免像小字附註。

## 圓角與陰影

```css
--radius-sm: 10px;
--radius-md: 18px;
--radius-lg: 28px;
--radius-xl: 36px;
--radius-pill: 999px;
--shadow-glow: 0 0 40px rgba(249, 115, 22, 0.24);
--shadow-card: 0 18px 44px rgba(0, 0, 0, 0.28);
--shadow-reward: 0 20px 60px rgba(250, 204, 21, 0.24);
```

## Layout

- 活動首頁：Hero → 任務進度 → 任務列表 → 獎勵 → 排行榜 → 規則。
- 任務中心：左側分類 + 任務 grid；手機改 tabs。
- Leaderboard：前三名可突出，但列表其餘項目仍可讀。
- 後台：使用較克制的表格與設定表單，不套用全部活動特效。

## 互動狀態

- Hover：卡片可增加 glow 或 border，但不位移過大。
- Focus：高對比 outline，不被 glow 淹沒。
- Disabled：任務未解鎖需顯示條件。
- Completed：顯示完成文字、時間、可領取狀態。
- Claiming：領取中 disabled，避免重複領取。

## 動效

- 任務完成：短暫 scale/fade，可關閉。
- 進度條：300ms ease-out。
- 獎勵 reveal：250ms-400ms。
- 倒數更新不應每秒造成整頁 reflow。
- 尊重 `prefers-reduced-motion`。

## 禁止事項

- 不使用誤導性抽獎或賭博感文案。
- 不隱藏中獎機率、資格或限制。
- 不讓動畫阻擋使用者操作。
- 不用 emoji 作為正式任務 icon。
- 不只用色彩表示任務完成，需文字與 icon。
