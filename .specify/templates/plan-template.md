# 實作計畫：[功能]

**分支**：`[###-feature-name]` | **日期**：[日期] | **規格**：[連結]
**輸入**：來自 `/specs/[###-feature-name]/spec.md` 的功能規格

**注意**：此模板由 `/speckit.plan` 指令填充。請參閱 `.specify/templates/commands/plan.md` 了解執行工作流程。

## 摘要

[從功能規格中提取：主要需求 + 研究中的技術方法]

## 技術上下文

<!--
  需要操作：用專案的技術細節替換本節中的內容。
  此處呈現的結構以建議的身份指導迭代過程。
-->

**語言/版本**：[例如 Python 3.11、Swift 5.9、Rust 1.75 或需要澄清]  
**主要依賴**：[例如 FastAPI、UIKit、LLVM 或需要澄清]  
**儲存**：[如果適用，例如 PostgreSQL、CoreData、檔案或不適用]  
**測試**：[例如 pytest、XCTest、cargo test 或需要澄清]  
**目標平台**：[例如 Linux 伺服器、iOS 15+、WASM 或需要澄清]
**專案類型**：[單一/web/行動 - 決定來源結構]  
**效能目標**：[特定於領域，例如 1000 req/s、10k 行/秒、60 fps 或需要澄清]  
**約束**：[特定於領域，例如 <200ms p95、<100MB 記憶體、離線能力或需要澄清]  
**規模/範圍**：[特定於領域，例如 10k 使用者、1M LOC、50 個螢幕或需要澄清]

## 章程檢查

*門控：在階段 0 研究之前必須通過。在階段 1 設計之後重新檢查。*

[根據章程文件確定的門控]

## 專案結構

### 文件（此功能）

```
specs/[###-feature]/
├── plan.md              # 此檔案（/speckit.plan 指令輸出）
├── research.md          # 階段 0 輸出（/speckit.plan 指令）
├── data-model.md        # 階段 1 輸出（/speckit.plan 指令）
├── quickstart.md        # 階段 1 輸出（/speckit.plan 指令）
├── contracts/           # 階段 1 輸出（/speckit.plan 指令）
└── tasks.md             # 階段 2 輸出（/speckit.tasks 指令 - 不由 /speckit.plan 建立）
```

### 原始碼（儲存庫根目錄）
<!--
  需要操作：用此功能的具體佈局替換下面的佔位符樹。
  刪除未使用的選項並用實際路徑擴展所選結構（例如 apps/admin、packages/something）。
  交付的計畫不得包含選項標籤。
-->

```
# [如果未使用則刪除] 選項 1：單一專案（預設）
src/
├── models/
├── services/
├── cli/
└── lib/

tests/
├── contract/
├── integration/
└── unit/

# [如果未使用則刪除] 選項 2：Web 應用程式（當偵測到"前端"+"後端"時）
backend/
├── src/
│   ├── models/
│   ├── services/
│   └── api/
└── tests/

frontend/
├── src/
│   ├── components/
│   ├── pages/
│   └── services/
└── tests/

# [如果未使用則刪除] 選項 3：行動 + API（當偵測到"iOS/Android"時）
api/
└── [與上面的後端相同]

ios/ 或 android/
└── [平台特定結構：功能模組、UI 流程、平台測試]
```

**結構決策**：[記錄所選結構並引用上面捕獲的實際目錄]

## 複雜度追蹤

*僅當章程檢查有必須證明的違規時才填寫*

| 違規 | 為什麼需要 | 更簡單的替代方案被拒絕的原因 |
|------|----------|---------------------------|
| [例如第 4 個項目] | [目前需求] | [為什麼 3 個項目不夠] |
| [例如倉儲模式] | [具體問題] | [為什麼直接資料庫存取不夠] |
