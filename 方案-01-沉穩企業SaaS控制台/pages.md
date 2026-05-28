# Pages：沉穩企業 SaaS 控制台

## Dashboard

結構：

1. Page header：標題、說明、主要 CTA、日期或環境切換。
2. KPI cards：3-4 張，包含數字、趨勢、輔助文字。
3. 主要圖表：營收、使用量、活躍度或處理量。
4. 次要列表：最近活動、待辦、告警。
5. Quick actions：常用操作。

規則：

- KPI 需有比較基準，例如「較上週」。
- 圖表不應超過 2-3 個，避免變監控中心。
- 待辦與異常要比裝飾性內容更明顯。

## List Page

結構：

1. 標題列與新增按鈕。
2. 篩選器列：搜尋、狀態、日期、更多篩選。
3. 已套用篩選 chip。
4. Data table。
5. Pagination。
6. Empty / loading / error state。

規則：

- 批次選取後顯示 bulk action bar。
- 列操作固定在最右側。
- 點擊列可進入 detail 或開 drawer，但行為需一致。

## Detail Page

結構：

1. Breadcrumb。
2. Header：名稱、狀態、主要操作。
3. Summary cards。
4. Tabs：概覽、設定、成員、紀錄。
5. 右側 metadata panel（可選）。
6. Audit log 或 recent activity。

規則：

- 危險操作不要放在 header 主要 CTA。
- 狀態變更要有確認與紀錄。
- Metadata panel 不應塞入主要操作。

## Create / Edit Form Page

結構：

1. Page header。
2. Form sections。
3. Sidebar help 或 summary（可選）。
4. Sticky action bar：取消、儲存草稿、送出。
5. Validation summary。

規則：

- 長表單分區。
- 儲存中防止重複送出。
- 離開前提示未儲存變更。

## Settings Page

結構：

1. 左側 settings nav。
2. 右側表單內容。
3. 每個設定區塊用 card 分隔。
4. Audit note。
5. Danger Zone 固定放在最下方。

## Permission / Role Management

結構：

1. Role list。
2. Permission matrix。
3. Member assignment。
4. Change summary。
5. Confirmation dialog。

規則：

- 權限變更需顯示影響範圍。
- 高權限角色需 warning。
- 儲存後顯示稽核紀錄入口。

## Notification Center

結構：

1. Tabs：全部、未讀、系統、工作。
2. Notification list。
3. Batch mark as read。
4. Preferences link。

## AI 提示模板

```text
建立一個企業 SaaS 後台頁面。請使用方案-01 的沉穩企業 SaaS 控制台風格：淺色、藍灰配色、白底卡片、清楚表格、中高資料密度、可預期操作。
頁面必須包含 page header、filter bar、data table、pagination、empty/loading/error 狀態，以及必要的 dialog 或 drawer。
遵守本方案的 design-system.md 與 components.md，不要加入霓虹、玻璃擬態、大面積漸層或 emoji icon。
```
