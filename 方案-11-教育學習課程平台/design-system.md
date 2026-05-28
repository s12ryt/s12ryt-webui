# Design System：教育學習課程平台

## 色彩

```css
--color-bg: #F8FAFC;
--color-surface: #FFFFFF;
--color-surface-muted: #F1F5F9;
--color-border: #E2E8F0;
--color-border-strong: #CBD5E1;
--color-text: #102033;
--color-text-muted: #526173;
--color-text-subtle: #718096;
--color-primary: #4F46E5;
--color-primary-hover: #4338CA;
--color-primary-soft: #E0E7FF;
--color-accent: #0EA5E9;
--color-accent-soft: #E0F2FE;
--color-progress: #10B981;
--color-progress-soft: #D1FAE5;
--color-success: #16A34A;
--color-warning: #D97706;
--color-danger: #DC2626;
--color-info: #2563EB;
```

## 字體

- 主要字體：Inter、Noto Sans TC、system-ui。
- 閱讀內容：Noto Sans TC，行高較寬。
- 程式課程 code：JetBrains Mono、Roboto Mono。

## 字級

| 用途 | 尺寸 | 行高 | 字重 | 備註 |
| --- | --- | --- | --- | --- |
| Course title | 32px | 42px | 750 | 課程詳情 |
| Lesson title | 24px | 34px | 700 | 學習頁 |
| Section title | 18px | 28px | 700 | 區塊 |
| Body | 15px | 26px | 400 | 說明文字 |
| Learning content | 16px | 30px | 400 | 閱讀教材 |
| Caption | 12px | 18px | 500 | 進度、時間 |

## 間距

- 課程卡 padding：18px-22px。
- 學習頁主內容與側欄 gap：24px。
- 章節列表列高：56px-72px。
- 測驗題目間距：24px。
- 完成狀態與回饋間距：16px。

## 圓角與陰影

```css
--radius-sm: 8px;
--radius-md: 14px;
--radius-lg: 20px;
--radius-xl: 28px;
--shadow-card: 0 1px 2px rgba(16, 32, 51, 0.06), 0 10px 28px rgba(16, 32, 51, 0.06);
--shadow-player: 0 20px 60px rgba(16, 32, 51, 0.12);
```

## Layout

- Course dashboard：主內容 8 欄 + 側邊進度 4 欄。
- Learning player：影片/內容為主，章節側欄 320px。
- Mobile：章節列表改 bottom sheet 或獨立頁，避免壓縮播放器。
- Quiz：題目置中，最大寬度 760px。
- Admin：table + analytics cards。

## 進度與狀態

- 未開始：neutral。
- 進行中：primary 或 accent。
- 已完成：progress/success。
- 逾期：warning。
- 未通過：danger。

進度不可只用顏色，需顯示百分比、完成數或文字。

## 互動狀態

- Hover：課程卡邊框或陰影變化。
- Focus：primary outline。
- Disabled：未解鎖課程顯示鎖定原因。
- Loading：課程列表與播放器 skeleton。
- Completion：完成課程可顯示溫和回饋，不用過度爆炸動畫。

## 動效

- 進度條變化：250ms ease-out。
- 答題回饋：180ms。
- 章節切換：150ms。
- 尊重 `prefers-reduced-motion`。

## 禁止事項

- 不讓促銷 banner 干擾學習頁。
- 不只用顏色表示答題正確/錯誤。
- 不用 emoji 當課程狀態 icon。
- 不把所有成就做成強烈遊戲化特效。
- 不在影片播放器周圍放過多雜訊。
