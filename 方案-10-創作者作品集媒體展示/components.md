# Components：創作者作品集媒體展示

## Button / Link CTA

- Primary：聯絡合作、查看作品、預約諮詢。
- Secondary：下載作品集、查看案例。
- Text link：閱讀故事、下一個作品。
- Ghost：深色背景上的低干擾導覽。

規則：

- CTA 可更具品牌感，但 hover 不推擠版面。
- 深色背景需確保對比。
- 外部連結需有清楚標示。

## Media Hero

結構：

1. 大標題。
2. 短 tagline。
3. 背景圖/影片。
4. 主要 CTA。
5. Metadata：年份、地點、角色。

規則：

- 背景媒體加 overlay 確保文字可讀。
- 手機上避免文字覆蓋重要主體。
- 影片需提供替代 poster。

## Gallery Card

結構：

1. 圖片或影片縮圖。
2. Overlay title。
3. Category / year。
4. Hover CTA。

狀態：

- loading：保留比例 skeleton。
- error：顯示中性 fallback。
- featured：可加大尺寸。

## Masonry / Gallery Grid

- 支援不同作品比例。
- 需避免 CLS，預先定義 aspect ratio。
- 手機改單欄或雙欄。
- 可用 filter chips 切換分類。

## Case Study Header

必備：

- 案例標題。
- 客戶或專案名稱。
- 年份。
- 角色。
- 服務項目。
- 成果摘要。

## Case Study Block

類型：

- Problem / Challenge。
- Process。
- Visual exploration。
- Result。
- Testimonial。
- Next project。

每個 block 應有清楚標題與媒體支撐，不只堆圖片。

## Lightbox

功能：

- 開啟大圖。
- 左右切換。
- Esc 關閉。
- 顯示作品標題與描述。
- 支援觸控滑動。

可及性：

- 開啟時 focus trap。
- 關閉後 focus 回到原卡片。

## Profile / About Card

- 頭像或工作照。
- 簡介。
- 技能/服務。
- 客戶或合作標誌。
- 社群連結。

不要使用過多 logo 導致雜亂。

## Testimonial

- 引言。
- 姓名。
- 身份/公司。
- 頭像可選。
- 相關案例連結。

## Contact CTA

結構：

1. 合作邀請文案。
2. 服務類型選項。
3. Email / form CTA。
4. 回覆時間預期。

## Media Article Card

- 封面。
- 標題。
- 摘要。
- 日期。
- 閱讀時間。

## Empty State

- 篩選無作品：提供清除篩選。
- 圖片載入失敗：提供重試或替代描述。
