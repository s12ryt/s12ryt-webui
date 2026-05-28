# Pages：遊戲化活動互動介面

## Event Landing

結構：

1. Event hero：標題、副標、倒數、CTA。
2. Progress summary：目前完成度、可領獎勵。
3. Featured missions。
4. Reward showcase。
5. Leaderboard preview。
6. Rules panel。
7. FAQ。

規則：

- 首屏說清楚活動價值與下一步。
- 規則與限制不可難找。
- CTA 根據資格顯示不同狀態。

## Mission Center

結構：

1. Header：總進度、剩餘時間。
2. Mission category tabs。
3. Mission grid/list。
4. Reward summary。
5. Activity log。

狀態：

- 未登入：提示登入參加。
- 無資格：說明原因。
- 任務完成：提供領取 CTA。
- 活動結束：顯示結算結果。

## Reward Wallet

結構：

1. Points balance。
2. Available rewards。
3. Claimed rewards。
4. Expiring soon。
5. Reward detail modal。

規則：

- 即將到期要明確。
- 已使用、已過期、可使用狀態分明。

## Leaderboard Page

結構：

1. Leaderboard header。
2. My rank card。
3. Top 3 highlight。
4. Ranking table。
5. Rules / tie-breaker。
6. Time range switcher。

規則：

- 不公開敏感個資。
- 排名更新時間要顯示。
- 分數規則需可查。

## Sign-in / Streak Page

結構：

1. Streak summary。
2. Calendar grid。
3. Daily reward。
4. Missed day explanation。
5. Claim action。

## Lottery / Draw Page

結構：

1. Eligibility summary。
2. Chances count。
3. Draw action。
4. Reward result。
5. Prize list and probability/rules。
6. History。

規則：

- 機率與限制需清楚。
- 動畫不可讓使用者誤解結果可操控。
- 結果需可追蹤。

## Admin Activity Dashboard

結構：

1. KPI：參與人數、完成率、發獎數、轉換率。
2. Mission performance。
3. Reward inventory。
4. Leaderboard moderation。
5. Fraud/risk alerts。

## Admin Mission Editor

結構：

1. Basic info。
2. Eligibility。
3. Mission condition builder。
4. Reward settings。
5. Schedule。
6. Preview。
7. Publish confirmation。

## AI 提示模板

```text
建立一個遊戲化活動任務中心。請使用方案-12 的遊戲化活動互動介面風格：深色活動背景、橘色 primary、明確任務卡、進度、獎勵與倒數。
頁面需包含 event header、progress summary、mission tabs、mission card grid、reward summary、activity log、rules link、loading/empty/error 狀態。
任務完成不可只靠顏色表示；不要用 emoji 當正式 icon；活動規則與資格限制必須可見；動效需尊重 prefers-reduced-motion。
```
