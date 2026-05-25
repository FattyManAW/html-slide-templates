# 潤思科技 HTML 簡報素材庫

> **RunSi HTML Slide Templates Library**
> 為產品規劃組和開發組提供可直接使用的 HTML 簡報素材庫
> 從四個來源分析萃取，建立自有設計系統

## 目錄結構

```
runsi/html-slide-templates/
├── README.md                    ← 本文件：總索引
├── catalog/                     ← 宏觀層（Dana）：use case 分類索引
├── patterns/                    ← 視覺層（Smart）：CSS tokens · 配色 · 字體 · 佈局
├── workflow/                    ← 行為層（Kai）：5-step 挑選工作流
├── analysis/                    ← 補強層（Technus）：多維度分類 · SPA 判定
├── sources/                     ← 各來源原始分析
└── reusable-components/         ← 可直接引用的 HTML/CSS 元件
```

## 快速開始

### 幫我建立一份簡報

```bash
# 1. Clone 本素材庫
git clone https://github.com/FattyManAW/html-slide-templates.git

# 2. 閱讀工作流
cat workflow/workflow.md

# 3. 挑選模板（依場合+氛圍）
# 來源：beautiful-html-templates（34 模板，MIT license）
```

### 直接使用設計系統

```css
/* 10 套配色，任選一套 */
@import url('patterns/color-systems.css');

/* 6 套字體配對 */
@import url('patterns/font-pairings.css');

/* 10 種佈局模式 */
@import url('patterns/layout-patterns.css');
```

## 四層設計系統

| 層級 | 負責人 | 內容 | 產出 |
|------|--------|------|------|
| **宏觀層** | Dana | 12 use case 類別索引 · 4 macro 配色系統 | `catalog/` |
| **行為層** | Kai | 5-step 挑選工作流 · 場景對照表 · 裝飾詞彙庫 · 素材庫架構 | `workflow/` |
| **視覺層** | Smart | 10 CSS 配色系統 · 10 字體配對 · 10 佈局模式（含 HTML 骨架） | `patterns/` |
| **補強層** | Technus | 34 模板六維度分類 · nicepage 平台分析 · slides.com 判定 | `analysis/` |

## 34 模板速覽（Source 1: beautiful-html-templates）

### 📰 Editorial 雜誌風（14 模板）
Biennale Yellow · Bold Poster · Broadside · Cartesian · Cobalt Grid · Editorial Forest · Editorial Tri-Tone · Emerald Editorial · Grove · Monochrome · Neo-Grid Bold · Pin & Paper · Soft Editorial · Vellum

### 📢 Bold & Punchy 大膽宣言（7 模板）
8-Bit Orbit · BlockFrame · Coral · Creative Mode · People's Platform · Raw Grid · Studio

### 💼 Professional 專業商務（4 模板）
Blue Professional · Capsule · Long Table · Signal

### 🎮 Playful 活潑遊戲（3 模板）
Daisy Days · Retro Windows · Sakura Chroma

### 🎨 Creative 創意（2 模板）
Scatterbrain · Stencil & Tablet

### 🤲 Warm & Crafted 溫暖手作（3 模板）
Mat · Playful · Retro Zine

### 🌙 Dark & Moody 黑暗氛圍（1 模板）
Pink Script — After Hours

> 完整分析見 [`sources/source-1-analysis.md`](sources/source-1-analysis.md)

## 潤思常見場景 → 推薦模板

| 場景 | 推薦模板 |
|------|---------|
| 用友簡報（企業級） | Signal · Blue Professional · Emerald Editorial |
| 產品發表 | Neo-Grid Bold · BlockFrame · Raw Grid |
| 數據報告 | Monochrome · Neo-Grid Bold · Cobalt Grid |
| 品牌故事 | Soft Editorial · Pin & Paper · Grove |
| 創意 Pitch | Creative Mode · Studio · Bold Poster |
| 技術分享 | Cobalt Grid · 8-Bit Orbit · Vellum |
| 內部回顧 | Editorial Forest · Scatterbrain · Playful |

## 10 套配色系統

| # | 名稱 | 類型 | 關鍵色 |
|---|------|------|--------|
| 1 | 暖紙+單色點綴 | Editorial | 奶油 #faf6f0 + 鈷藍/酒紅/翡翠 |
| 2 | Navy+Gold | Institutional | #0d1b2a + #c9a84c |
| 3 | Black+Electric Yellow | Studio | #0a0a0a + #ffe600 |
| 4 | Cream+Multi-Accent | Creative | #faf8f3 + RGBY |
| 5 | Forest+Dusty Pink | Organic | #2d4a3e + #d4a5a5 |
| 6 | White+Electric Blue | Professional | #ffffff + #2563eb |
| 7 | Dark Neon | Cyberpunk | #0a0a1a + #00ff88 |
| 8 | Pastel Capsule | Y2K | #fafafa + 馬卡龍方塊 |
| 9 | Tri-Tone Editorial | Fashion | #6b2737 + #d4a5a5 + cream |
| 10 | Graph Paper+Cobalt | Design Research | 鈷藍網格 + 奶油紙 |

> 完整 CSS variables 見 `patterns/color-systems.md`

## 6 套字體配對

1. **襯線體標題+無襯線內文** — Cormorant Garamond + Inter
2. **展示體封面+襯線體內文** — Archivo Black + Lora
3. **全無襯線體** — Inter (w700/w400)
4. **手寫體+無襯線體** — Caveat + DM Sans
5. **古典襯線體** — EB Garamond
6. **粗體無襯線+輕量無襯線** — Space Grotesk + DM Sans

> 完整 Google Fonts @import 見 `patterns/font-pairings.md`

## 四來源評估

| # | 來源 | 推薦度 | 定位 |
|---|------|:--:|------|
| 1 | beautiful-html-templates (GitHub) | ⭐⭐⭐ | 核心素材庫（34 模板，MIT） |
| 2 | nicepage.com | ⭐⭐ | 設計靈感補充（HTML Block 元件） |
| 3 | slides.com/templates | ⭐ | Reveal.js 生態參考（slides.com 不可達，已改用 Reveal.js 開源文檔） |
| 4 | slides.com/explore | ⭐ | 社群作品（slides.com 不可達，雙重確認） |

> 完整四來源分析見 [`sources/source-analysis.md`](sources/source-analysis.md)

## 設計系統關鍵原則

- ✅ **複製內容**（標題、內文、數字、圖片）→ 替換
- ❌ **保留不變**（字體、色板、網格、裝飾、導航）
- 🎨 **模板有品味，沒有行業** — 使用者品味優先
- 🔧 **設計缺失 layout** — 用同一設計系統自行設計，不換模板

## 貢獻者

| Agent | 角色 | 貢獻 |
|-------|------|------|
| Kai | Knowledge Manager | 行為層：工作流 · 場景對照 · 裝飾詞彙 · 素材庫架構 |
| Dana | DevOps | 宏觀層：use case 分類 · repo 架構 |
| Smart | Developer | 視覺層：CSS tokens · 配色 · 字體 · 佈局 |
| Technus | Developer | 補強層：六維度分類 · SPA 分析 |
| Commander-D | Lead | Source 1-2 分析 |
| Vesper | QA | 來源稽核 |
| Ray | Release | index.json · design tokens |

## License

上游模板（beautiful-html-templates）：MIT
自有分析文檔：MIT