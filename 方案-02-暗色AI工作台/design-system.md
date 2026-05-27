# Design System：暗色 AI 工作台

## 色彩

```css
--color-bg: #050816;
--color-bg-elevated: #0B1020;
--color-surface: #111827;
--color-surface-soft: #172033;
--color-border: #263244;
--color-text: #E5E7EB;
--color-text-muted: #94A3B8;
--color-primary: #22D3EE;
--color-primary-hover: #06B6D4;
--color-secondary: #A78BFA;
--color-accent: #38BDF8;
--color-success: #34D399;
--color-warning: #FBBF24;
--color-danger: #F87171;
```

## 背景

- 主背景使用深藍黑，不使用純黑。
- 可加入非常淡的 radial gradient 作氣氛，但不可影響文字可讀性。
- 卡片透明度不可過低，至少確保文字對比清楚。

## 字體

- UI：Inter、Noto Sans TC、system-ui。
- Code / prompt：JetBrains Mono、Fira Code、ui-monospace。

## 字級

| 用途 | 尺寸 | 行高 | 字重 |
| --- | --- | --- | --- |
| Workspace title | 24px | 32px | 700 |
| Panel title | 14px | 20px | 600 |
| Message body | 14px | 24px | 400 |
| Code | 13px | 22px | 400 |
| Meta | 12px | 18px | 500 |

## 間距與尺寸

- 左側 sidebar：280px。
- 右側 panel：320px-380px。
- 輸入框最小高度：112px。
- message 最大寬度：900px。
- panel padding：16px。

## 圓角與效果

```css
--radius-sm: 8px;
--radius-md: 12px;
--radius-lg: 18px;
--shadow-glow: 0 0 28px rgba(34, 211, 238, 0.14);
--shadow-panel: 0 18px 48px rgba(0, 0, 0, 0.28);
```

## 動效

- Streaming：文字或狀態可漸進出現。
- Running：使用 subtle pulse，不要大幅閃爍。
- Hover：border 或背景亮一階。
- 尊重 `prefers-reduced-motion`。

## 禁止事項

- 不使用過多霓虹外光，避免廉價感。
- 不使用低對比灰字。
- 不讓側欄、面板、主工作區全部同一個色階。
- 不用 emoji 當模型、工具、狀態 icon。
