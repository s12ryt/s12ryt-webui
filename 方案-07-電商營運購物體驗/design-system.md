# Design System：電商營運購物體驗

## 色彩

```css
--color-bg: #FAFAF9;
--color-surface: #FFFFFF;
--color-surface-muted: #F5F5F4;
--color-border: #E7E5E4;
--color-border-strong: #D6D3D1;
--color-text: #1C1917;
--color-text-muted: #57534E;
--color-text-subtle: #78716C;
--color-primary: #EA580C;
--color-primary-hover: #C2410C;
--color-primary-soft: #FFEDD5;
--color-accent: #0F766E;
--color-accent-soft: #CCFBF1;
--color-sale: #DC2626;
--color-sale-soft: #FEE2E2;
--color-success: #16A34A;
--color-warning: #D97706;
--color-danger: #DC2626;
--color-info: #2563EB;
```

## 色彩使用

- Primary 用於加入購物車、立即購買、套用優惠。
- Sale red 只用於折扣、限時、低庫存警示，不用於一般錯誤以免混淆。
- Accent 可用於免運、環保、會員等正向提示。
- 後台可降低 primary 面積，避免長時間使用疲勞。

## 字體

- 主要字體：Inter、Noto Sans TC、system-ui。
- 價格：Inter tabular nums 或 Roboto Mono。
- 商品名稱中文可使用 Noto Sans TC，避免過細字重。

## 字級

| 用途 | 尺寸 | 行高 | 字重 | 備註 |
| --- | --- | --- | --- | --- |
| Product title | 24px | 32px | 700 | 詳情頁商品名 |
| Listing title | 15px | 22px | 600 | 商品卡名稱 |
| Price large | 28px | 36px | 700 | 詳情頁價格 |
| Price card | 18px | 26px | 700 | 商品卡價格 |
| Body | 14px | 22px | 400 | 描述與規格 |
| Caption | 12px | 18px | 500 | 庫存、運送、標籤 |

## 間距

- 前台頁面外距：桌面 32px，平板 24px，手機 16px。
- 商品 grid gap：24px 桌面，16px 手機。
- 商品卡 padding：12px 或 16px。
- 詳情頁圖片與資訊間距：32px。
- 結帳流程區塊間距：20px，避免過度分散注意力。

## 圓角與陰影

```css
--radius-sm: 6px;
--radius-md: 12px;
--radius-lg: 18px;
--radius-xl: 24px;
--shadow-card: 0 1px 2px rgba(28, 25, 23, 0.06);
--shadow-card-hover: 0 10px 28px rgba(28, 25, 23, 0.10);
--shadow-cart: 0 20px 48px rgba(28, 25, 23, 0.18);
```

## Layout

- Listing：桌面 4 欄，窄桌面 3 欄，平板 2 欄，手機 1-2 欄視商品圖片比例。
- Filter：桌面左側欄 260px，手機改 drawer。
- Product detail：桌面左圖右資訊，手機圖片在上、購買區 sticky bottom。
- Checkout：桌面左表單右摘要，手機摘要可折疊但總金額必須可見。
- Admin：後台使用 table + side drawer，商品縮圖保留 48px。

## 圖片規則

- 商品圖比例需固定，避免列表跳動。
- 圖片 loading 使用 skeleton 或低解析 placeholder。
- 缺圖使用中性 placeholder，不用 emoji。
- Hover 可切換第二張圖，但不改變卡片尺寸。

## 互動狀態

- Hover：商品卡加陰影或 border，不使用放大推擠。
- Focus：primary outline，購買流程需鍵盤可操作。
- Disabled：缺貨按鈕顯示「已售完」或「通知我」。
- Loading：加入購物車按鈕顯示「加入中」。
- Error：結帳錯誤要 inline 顯示在欄位或摘要區。

## 動效

- 商品卡 hover：180ms ease-out。
- Cart drawer：220ms ease-out。
- 加入購物車可有輕微回饋，但不要過度遊戲化。

## 禁止事項

- 不隱藏運費、稅金、限制條件到最後一步。
- 不使用會造成 layout shift 的圖片比例。
- 不讓折扣標籤與錯誤狀態共用完全相同樣式。
- 不在結帳頁放太多分散注意力的促銷 banner。
- 不使用 emoji 當商品分類 icon。
