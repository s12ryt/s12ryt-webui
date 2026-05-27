# 方案 05：資料可視化監控

## 定位

適合 NOC、營運儀表板、監控中心、分析平台、即時狀態看板、風險監控。

## 設計關鍵字

- 即時
- 精準
- 狀態清楚
- 高密度
- 監控感

## 視覺摘要

以資料優先，強調圖表、告警、趨勢與異常。可以是深色也可以是淺色，但狀態色與資訊層級必須非常明確。

## 適合頁面

- Global overview
- Metrics dashboard
- Alerts center
- Incident timeline
- Service health
- Report view

## 不適合

- 以故事為主的品牌頁
- 只有單一輸入輸出的簡單工具
- 過度依賴大圖形裝飾的展示頁

## 實作優先順序

1. 先定義指標卡與圖表 grid。
2. 再建立告警、趨勢、比較、時間軸。
3. 最後補 drill-down、filters、export、refresh 狀態。
