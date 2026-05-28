# 小組件

本資料夾把跨方案常用的小組件從各方案敘述中抽出，作為 AI 實作時的共用元件索引。這裡定義的是元件責任、狀態、互動與內容規則，不直接決定視覺風格。

## 使用原則

1. 小組件只提供結構與行為，不提供獨立主視覺。
2. 色彩、圓角、陰影、字級、間距必須回到主方案的 `design-system.md`。
3. 元件文案語氣必須回到主方案的 `README.md` 與 `components.md`。
4. 若小組件規則與主方案衝突，以主方案為準。
5. 不可因為共用小組件而混用其他方案的視覺語言。

## 文件分類

| 文件 | 內容 | 常見使用時機 |
| --- | --- | --- |
| `基礎元件.md` | Button、Input、Select、Checkbox、Card、Badge 等 | 幾乎所有頁面 |
| `資料與狀態元件.md` | Table、List、Metric、Chart、Empty、Skeleton、Error 等 | 後台、監控、電商、文件列表 |
| `導覽與浮層元件.md` | Header、Sidebar、Tabs、Breadcrumb、Dialog、Drawer、Popover 等 | 多頁產品、設定頁、詳情頁 |
| `表單與操作元件.md` | Form、Validation、Confirm、Bulk action、Search、Filter 等 | 建立/編輯流程、管理後台 |
| `內容展示元件.md` | Hero、Feature、Pricing、Media card、Article、Timeline 等 | Landing、作品集、知識庫、活動頁 |

## AI 使用方式

當使用者要求實作頁面時，AI 應先決定主方案，再依需求挑小組件：

```text
主方案：方案-XX
頁面類型：列表 / 詳情 / 表單 / 儀表板 / Landing / 文件 / 活動
需要小組件：
- 基礎元件：Button、Card
- 資料與狀態元件：Table、EmptyState、Skeleton
- 導覽與浮層元件：Breadcrumb、Dialog
套用規則：所有 token 來自主方案 design-system.md
```

## 共用狀態要求

每個可互動或承載資料的小組件至少要考慮：

- default
- hover
- focus
- active
- disabled
- loading
- empty
- error
- success
- permission denied 或 readonly

## 命名建議

實作時可以採用下列抽象命名，再由不同框架轉換：

| 類型 | 命名範例 |
| --- | --- |
| 基礎元件 | `Button`、`TextInput`、`SelectField`、`Card` |
| 資料元件 | `DataTable`、`MetricCard`、`StatusBadge`、`ChartPanel` |
| 狀態元件 | `EmptyState`、`ErrorState`、`LoadingSkeleton`、`PermissionNotice` |
| 導覽元件 | `AppHeader`、`SideNav`、`Breadcrumbs`、`TabsNav` |
| 浮層元件 | `Dialog`、`Drawer`、`PopoverMenu`、`Tooltip` |
| 表單元件 | `FormField`、`ValidationMessage`、`SearchInput`、`FilterBar` |
| 內容元件 | `HeroSection`、`FeatureGrid`、`PricingCard`、`MediaCard` |

## 不要做

- 不要在小組件內指定某套方案的品牌色。
- 不要用 emoji 當 icon。
- 不要只定義 happy path。
- 不要讓 hover 或 focus 造成 layout shift。
- 不要把頁面區塊命名成只適用單一方案的名稱，除非放在方案資料夾內。
