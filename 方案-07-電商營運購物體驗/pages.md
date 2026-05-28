# Pages：電商營運購物體驗

## Product Listing Page

結構：

1. Header：分類名稱、描述、商品數。
2. Promo strip：可選，顯示活動但不遮擋列表。
3. Toolbar：排序、顯示模式、篩選入口。
4. Filter sidebar / mobile drawer。
5. Product grid。
6. Pagination 或 infinite scroll。
7. Empty state。

規則：

- 已套用篩選顯示 chip。
- 商品卡圖片比例一致。
- 手機版篩選與排序要易操作。

## Product Detail Page

結構：

1. Breadcrumb。
2. Product gallery。
3. Product info：名稱、評分、價格、優惠、規格。
4. Purchase panel：數量、庫存、加入購物車、立即購買。
5. Delivery info：運送、退貨、付款方式。
6. Detail tabs：描述、規格、評價、問答。
7. Related products。

狀態：

- 缺貨：購買 CTA 改通知。
- 規格未選：提示選擇規格。
- 加入中：按鈕 loading。

## Cart Page / Drawer

結構：

1. Cart item list。
2. Quantity controls。
3. Coupon input。
4. Shipping estimator。
5. Order summary。
6. Checkout CTA。

規則：

- 移除商品要可復原。
- 庫存不足需 inline 顯示。
- 免運門檻可以顯示進度，但不要過度遊戲化。

## Checkout Page

結構：

1. Stepper。
2. Contact form。
3. Shipping method。
4. Payment method。
5. Order summary sticky panel。
6. Trust notes：安全付款、退貨政策。

規則：

- 每一步只要求必要資訊。
- 錯誤欄位需聚焦。
- 付款送出後防止重複提交。
- 最後確認前顯示完整費用。

## Order Detail Page

結構：

1. Order status header。
2. Timeline：已下單、已付款、出貨、配送、完成。
3. Items list。
4. Payment summary。
5. Shipping address。
6. Actions：取消、退貨、聯絡客服。

## Admin Sales Dashboard

結構：

1. KPI：營收、訂單數、轉換率、客單價。
2. Sales chart。
3. Top products。
4. Low stock alerts。
5. Recent orders。
6. Promotion performance。

## Admin Product Management

結構：

1. Header：新增商品、匯入、匯出。
2. Filter bar：搜尋、分類、狀態、庫存。
3. Product table。
4. Bulk action bar。
5. Edit drawer。

## AI 提示模板

```text
建立一個電商商品列表頁。請使用方案-07 的電商營運購物體驗風格：白底、商品圖片優先、橘色 primary CTA、清楚價格、折扣、庫存與篩選。
頁面必須包含分類 header、toolbar、filter sidebar、product grid、product card、empty/loading/error 狀態。
商品圖片比例固定，hover 不可造成 layout shift；不可使用 emoji icon；結帳或購買 CTA 文案要明確。
```
