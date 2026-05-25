# Chart Styles · 圖表風格分析

- **來源**: beautiful-html-templates（34 模板）
- **提取日期**: 2026-05-25
- **提取者**: Technus (Beta Squad)

## 總覽

beautiful-html-templates 模板**不含 JavaScript 圖表庫**（沒有 Chart.js/D3.js 引用）。所有數據呈現依賴純 CSS：大數字、統計卡、進度條、對比網格。這對我們是優勢 — 投影片簡報不需要互動式圖表，CSS 驅動的靜態數據展示更快、更可控、更易中文化。

## 數據呈現模式（從 34 模板提取）

### 模式 1：Hero Metric（封面大數字）

**適用**: 封面 · 章節頁 · 宣言頁

```css
.metric-hero {
  font-family: "JetBrains Mono", monospace;
  font-size: clamp(64px, 12vw, 180px);
  font-weight: 700;
  letter-spacing: -0.03em;
  line-height: 0.95;
}
.metric-label {
  font-family: "Space Grotesk", sans-serif;
  font-size: clamp(14px, 0.9vw, 18px);
  text-transform: uppercase;
  letter-spacing: 0.12em;
  opacity: 0.6;
}
```

**範本**: signal, neo-grid-bold, blue-professional, studio

**使用範例**:
```html
<div class="metric-hero">47%</div>
<div class="metric-label">Year-over-Year Revenue Growth</div>
```

### 模式 2：Stat Card Grid（統計卡片網格）

**適用**: 數據儀表板 · KPI 摘要 · 季度回顧

```css
.stat-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2vw;
}
.stat-card {
  background: var(--card-bg);
  border: 2px solid var(--border);
  padding: 3vw;
  border-radius: 0; /* 投影片不用圓角 — 保持乾淨 */
}
.stat-card .number {
  font-family: "JetBrains Mono", monospace;
  font-size: 3.5vw;
  font-weight: 700;
  color: var(--accent);
  line-height: 1;
}
.stat-card .label {
  font-size: 0.9vw;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  margin-top: 0.8vw;
  opacity: 0.6;
}
.stat-card .delta {
  font-size: 0.85vw;
  margin-top: 0.4vw;
}
.stat-card .delta.up { color: #16a34a; }
.stat-card .delta.down { color: #dc2626; }
```

**範本**: monochrome（18 頁統計密集）, signal, block-frame

### 模式 3：Comparison Bar（水平對比條）

**適用**: 競品對比 · 前後對照 · 方案比較

```css
.compare-bar {
  display: flex;
  align-items: center;
  gap: 1.5vw;
  margin-bottom: 1.5vw;
}
.compare-bar .label {
  width: 18vw;
  font-size: 1vw;
  text-align: right;
}
.compare-bar .track {
  flex: 1;
  height: 2.2vw;
  background: var(--card-bg);
  position: relative;
}
.compare-bar .fill {
  height: 100%;
  background: var(--accent);
  transition: width 1.2s cubic-bezier(0.22, 1, 0.36, 1);
}
.compare-bar .value {
  font-family: "JetBrains Mono", monospace;
  font-size: 1vw;
  width: 6vw;
}
```

**範本**: neo-grid-bold, raw-grid, block-frame

### 模式 4：Timeline（時間軸 / 里程碑）

**適用**: 專案時程 · 產品路線圖 · 公司里程碑

```css
.timeline {
  display: flex;
  flex-direction: column;
  gap: 0;
  padding-left: 3vw;
  border-left: 3px solid var(--accent);
}
.timeline-item {
  position: relative;
  padding: 2vw 0 2vw 3vw;
}
.timeline-item::before {
  content: '';
  position: absolute;
  left: calc(-3vw - 8px);
  top: 2.4vw;
  width: 13px;
  height: 13px;
  border-radius: 50%;
  background: var(--accent);
}
.timeline-item .year {
  font-family: "JetBrains Mono", monospace;
  font-size: 1.4vw;
  font-weight: 700;
  color: var(--accent);
}
.timeline-item .title {
  font-size: 1.6vw;
  font-weight: 700;
  margin-top: 0.3vw;
}
.timeline-item .desc {
  font-size: 0.95vw;
  opacity: 0.7;
  margin-top: 0.4vw;
}
```

**範本**: broadside (20 頁含 timeline), stencil-tablet, signal

### 模式 5：Progress Ring（環形進度）

**適用**: 專案完成度 · 目標達成率 · 技能/能力圖

```css
.progress-ring {
  width: 12vw;
  height: 12vw;
  border-radius: 50%;
  border: 0.6vw solid var(--card-bg);
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}
.progress-ring .pct {
  font-family: "JetBrains Mono", monospace;
  font-size: 2.5vw;
  font-weight: 700;
}
.progress-ring .ring-label {
  position: absolute;
  bottom: -2.5vw;
  font-size: 0.8vw;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  opacity: 0.6;
}
```

**範本**: capsule, creative-mode

### 模式 6：Table / Matrix（數據表 / 矩陣）

**適用**: 功能對比 · 定價表 · 規格矩陣

```css
.data-table {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.95vw;
}
.data-table th {
  font-family: "JetBrains Mono", monospace;
  font-size: 0.75vw;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  text-align: left;
  padding: 1vw 1.5vw;
  border-bottom: 2px solid var(--ink);
  opacity: 0.6;
}
.data-table td {
  padding: 1vw 1.5vw;
  border-bottom: 1px solid var(--border-light);
}
.data-table tr.highlight {
  background: var(--highlight-bg);
}
.data-table .check { color: #16a34a; font-weight: 700; }
.data-table .cross { color: #dc2626; }
```

**範本**: signal（18 頁含多張表）, monochrome, emerald-editorial

## 配色策略 for 數據

### 數字強調色

| 模板 | 數字色 | 用途 |
|------|------|------|
| signal | `--c-accent` (muted-gold) | 所有大數字 |
| neo-grid-bold | `#FFE600` (neon-yellow) | KPI 數字 |
| studio | `#FFE600` (electric-yellow) | 封面數字 |
| blue-professional | `#1E5FBB` (cobalt) | 統計數字 |
| monochrome | `#1A1A16` (black) | 無彩色，純排版 |

### 增長/下降色

```css
:root {
  --delta-up:   #16a34a; /* 增長綠 */
  --delta-down: #dc2626; /* 下降紅 */
  --delta-flat: #8a8a80; /* 持平灰 */
}
```

### 圖表輔助色序列

從 34 模板中提取最常用的 CSS 數據色序列：

```css
--chart-1: #1E5FBB; /* 鈷藍 */
--chart-2: #C8442A; /* 磚紅 */
--chart-3: #B8860B; /* 暗金 */
--chart-4: #2D5A27; /* 森林綠 */
--chart-5: #8B5CF6; /* 紫羅蘭 */
--chart-6: #D97706; /* 琥珀 */
--chart-7: #5B8C5A; /* 鼠尾草 */
--chart-8: #BE185D; /* 深粉 */
```

## 8-Bit Orbit 的特殊圖表（像素風）

唯一包含圖形化 chart 元素的模板 — SVG pixel art：

```css
/* 像素柱狀圖 */
.pixel-bar {
  display: flex;
  align-items: flex-end;
  gap: 4px;
  height: 200px;
}
.pixel-bar .col {
  width: 32px;
  background: var(--neon-green);
  image-rendering: pixelated;
  box-shadow: 0 0 12px var(--neon-green);
}
```

## 對我們簡報的建議

### P0 用友（企業數據報告）
- **主模式**: Stat Card Grid + Data Table
- **配色**: blue-professional 風格（cream + cobalt）
- **數字字體**: Noto Sans SC 700（CJK 數字比 JetBrains Mono 更適合中文環境）

### P3 APS/CRIS（科技產品）
- **主模式**: Hero Metric + Comparison Bar
- **配色**: neo-grid-bold 或 creative-mode（大膽對比）
- **數字字體**: JetBrains Mono（科技感）

### 核心規則
1. ✅ **數字永遠用 mono 字體** — 這是 beautiful-html-templates 34 模板的統一規則
2. ✅ **不使用 JavaScript 圖表庫** — 靜態 CSS 足以應付投影片簡報
3. ✅ **每頁最多 3 個大數字** — 超過會分散注意力
4. ✅ **增長/下降必須有方向色** — 綠漲紅跌是跨語言通用慣例
5. ⚠️ **CJK 數字環境下 JetBrains Mono 可能顯示過窄** — 中文字型數字優先