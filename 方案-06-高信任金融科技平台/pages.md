# Pages：高信任金融科技平台

## Account Overview

結構：

1. Top bar：帳戶切換、安全狀態、通知。
2. Balance summary：總資產、可用餘額、凍結金額、幣別。
3. Quick actions：轉入、轉出、付款、換匯。
4. Risk banner：KYC、異常登入、待審核事項。
5. Cashflow chart：近期收支趨勢。
6. Recent transactions：最近 5-10 筆交易。
7. Side panel：帳戶限制、卡片、常用收款方。

狀態：

- 首次使用：引導身份驗證與新增付款方式。
- 帳戶受限：主要操作 disabled，顯示解除限制 CTA。
- loading：保留金額卡與交易列表骨架。

## Transaction History

結構：

1. Header：交易紀錄、匯出報表、日期範圍。
2. Summary strip：期間收入、支出、手續費、淨額。
3. Filter bar：搜尋、類型、狀態、金額範圍、幣別。
4. Transaction table。
5. Detail drawer：交易編號、時間線、收付款方、費用、備註。
6. Pagination。

規則：

- 預設排序最新在上。
- 匯出前顯示資料範圍與筆數。
- 空結果要提供清除篩選。

## Payment Flow

步驟：

1. 選擇收款方。
2. 輸入金額與幣別。
3. 顯示手續費、匯率、預計完成時間。
4. 確認摘要。
5. OTP / 生物識別 / 二次驗證。
6. 結果頁：成功、處理中或失敗。

結果頁必備：

- 狀態標題。
- 金額與對象。
- 交易編號。
- 完成或預計完成時間。
- 查看明細、下載收據、回首頁 CTA。

## Investment Portfolio

結構：

1. Portfolio value：總市值、今日損益、累計報酬。
2. Allocation chart：資產配置。
3. Performance chart：時間區間切換。
4. Holdings table：標的、持有量、成本、市值、損益。
5. Risk note：波動、集中度、免責聲明。

規則：

- 報酬率需顯示正負號。
- 高風險標的需要 warning badge。
- 不用會讓人誤以為保證獲利的文案。

## Billing / Invoice Center

結構：

1. Billing summary：本月應付、已付、逾期。
2. Payment method card。
3. Invoice table：發票號碼、日期、金額、狀態、下載。
4. Subscription panel：方案、下次扣款、稅務資訊。
5. Danger zone：取消訂閱或移除付款方式。

## Admin Risk Review

結構：

1. Queue metrics：待審核、逾時、已阻擋、誤報率。
2. Risk queue table：交易、風險分數、原因、使用者、時間。
3. Detail panel：規則命中、歷史交易、裝置資訊。
4. Action bar：通過、拒絕、要求補件。
5. Audit log：所有操作與操作者。

## AI 提示模板

```text
建立一個金融科技帳戶總覽頁。請使用方案-06 的高信任金融科技平台風格：淺色、克制、低噪音、清楚金額階層、風險提示與交易狀態。
頁面必須包含 BalanceCard、QuickActions、RiskBanner、CashflowChart、TransactionList。
所有金額要右對齊或使用 tabular nums，漲跌不能只靠顏色表示。
高風險操作需有確認摘要與驗證流程，不要使用霓虹、玻璃擬態、emoji icon 或賭博感動畫。
```
