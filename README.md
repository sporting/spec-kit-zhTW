# Spec-Kit 繁體中文版 🇹🇼

> GitHub Spec-Kit 的完整繁體中文化版本 | 規格驅動開發工具包

[![GitHub](https://img.shields.io/badge/GitHub-spec--kit-blue)](https://github.com/github/spec-kit)
[![語言](https://img.shields.io/badge/語言-繁體中文-red)](README.md)
[![狀態](httpss://img.shields.io/badge/狀態-穩定-green)](README.md)

---

## 📖 簡介

**Spec-Kit** 是 GitHub 開源的規格驅動開發工具包，與 Cursor 等 AI 編碼工具深度整合，幫助開發者從需求到實作的全流程開發。

**本專案特點**：
- 🇹🇼 **完整中文化** - 所有指令和範本已中文化
- 📋 **開頭一句話** - 每個指令都有簡潔的用途說明
- 🚀 **開箱即用** - 複製即可使用
- 📚 **文件完善** - 詳細的中文使用指南

---

## ✨ 核心功能

### 🎯 四階段核心工作流程

| 階段 | 指令 | 用途 |
|------|------|------|
| 1️⃣ | `/speckit.specify` | 將功能需求轉化為清晰的規格文件 |
| 2️⃣ | `/speckit.plan` | 制定功能的技術實作方案 |
| 3️⃣ | `/speckit.tasks` | 將技術方案分解為可執行的任務清單 |
| 4️⃣ | `/speckit.implement` | 按任務清單逐步實作功能程式碼 |

### 🔧 輔助指令

| 指令 | 用途 | 使用時機 |
|------|------|---------|
| `/speckit.constitution` | 定義專案的核心原則和開發規範 | 專案開始時（可選） |
| `/speckit.clarify` | 解決規格中的模糊和歧義問題 | 規格化後（可選） |
| `/speckit.analyze` | 檢查規格、計畫、任務的一致性 | 實作前（可選） |
| `/speckit.checklist` | 產生需求品質驗證清單 | 任何階段 |

---

## 🚀 快速開始

### 方式一：使用此範本建立新專案

```bash
# 1. 在 GitHub 上點擊 "Use this template" 建立新倉庫

# 2. 複製您的新倉庫
git clone https://github.com/your-username/your-project.git
cd your-project

# 3. 開始使用（在 Cursor 中）
/speckit.specify
開發一個使用者註冊功能...
```

### 方式二：在現有專案中使用

```bash
# 1. 確保已安裝 Spec-Kit CLI
uv tool install specify-cli --from git+https://github.com/github/spec-kit.git

# 2. 在專案中初始化
cd your-existing-project
specify init --here --ai cursor --force

# 3. 複製中文化檔案
# 從本範本複製 .cursor/commands/ 和 .specify/templates/ 到您的專案
```

---

## 📚 使用範例

### 完整開發流程

```bash
# 步驟 1：建立功能規格
/speckit.specify
開發一個待辦事項管理功能。使用者可以建立、查看、標記完成、刪除待辦事項。

# 步驟 2：制定技術方案
/speckit.plan

# 步驟 3：分解任務
/speckit.tasks

# 步驟 4：開始實作
/speckit.implement
```

### 最小工作流程（4步）

```
指定 → 規劃 → 任務 → 實作
```

### 完整工作流程（含品質檢查）

```
原則 → 指定 → 澄清 → 規劃 → 任務 → 分析 → 實作
```

---

## 📁 專案結構

```
.
├── .cursor/
│   └── commands/          # 8個中文化的指令檔案
│       ├── speckit.constitution.md
│       ├── speckit.specify.md
│       ├── speckit.clarify.md
│       ├── speckit.plan.md
│       ├── speckit.tasks.md
│       ├── speckit.implement.md
│       ├── speckit.analyze.md
│       └── speckit.checklist.md
│
├── .specify/
│   ├── memory/
│   │   └── constitution.md    # 專案章程範本
│   ├── scripts/               # 自動化腳本
│   └── templates/             # 5個中文化的檔案範本
│
├── README.md                  # 本文件
└── 指令快速參考.md             # 指令速查表
```

---

## 🎯 中文化說明

本專案遵循以下中文化原則：

✅ **已中文化**
- 所有指令的 `description` 和執行說明
- 所有範本的章節標題和註釋
- 每個指令開頭的"指令用途"說明

✅ **保持英文**
- 指令檔案名稱（如 `speckit.specify.md`）
- 指令觸發詞（如 `/speckit.specify`）
- 技術標識符（變數名稱、路徑等）

**原因**：確保工具穩定運行的同時提供最佳中文體驗

---

## 💡 核心優勢

| 對比項 | 傳統開發 | Spec-Kit |
|--------|---------|----------|
| 需求管理 | 口頭溝通，易誤解 | 結構化文件，清晰明確 |
| 開發流程 | 直接編碼，後期問題多 | 先規範後實作，減少重工 |
| 測試覆蓋 | 後期補充，覆蓋率低 | 強制 TDD，測試先行 |
| 文件維護 | 文件與程式碼脫節 | 規格與實作同步 |
| 團隊協作 | 依賴個人理解 | 基於統一規範 |

---

## 🌟 特色功能

### 1. 開頭一句話用途說明
每個指令文件都以簡潔的方式告訴您它的用途：

```markdown
## 📋 指令用途

**將功能需求轉化為清晰的規格文件**
```

### 2. 快速參考表
查看 [指令快速參考.md](./指令快速參考.md) 獲取：
- 所有指令總覽
- 使用時機說明
- 完整工作流程範例
- 使用技巧

---

## 📋 系統要求

- **Python**: 3.11+
- **套件管理器**: uv
- **AI 工具**: Cursor（推薦）或其他相容工具
- **Git**: 版本控制

---

## 🤝 貢獻

歡迎提交 Issue 和 Pull Request！

如果您發現翻譯不準確或有改進建議，請：
1. Fork 本倉庫
2. 建立您的特性分支
3. 提交變更
4. 發起 Pull Request

---

## 📄 授權條款

本專案基於原 [github/spec-kit](https://github.com/github/spec-kit) 專案。

中文化工作遵循原專案的授權條款。

---

## 🔗 相關連結

- [Spec-Kit 原專案](https://github.com/github/spec-kit)
- [Cursor 官網](https://cursor.sh)
- [uv 套件管理器](https://github.com/astral-sh/uv)

---

## ⭐ 如果有幫助，請給個 Star！

如果這個中文化版本對您有幫助，請點擊右上角的 ⭐ Star 支持我們！

---

**開始使用 Spec-Kit 繁體中文版，體驗規格驅動開發的強大威力！** 🚀