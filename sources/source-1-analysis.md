# Source 1: beautiful-html-templates — 完整分析

> Source: https://github.com/zarazhangrui/beautiful-html-templates
> Analyzed: 2026-05-25 by Kai
> 34 模板全量解析 + 5-step 工作流

## 概覽

| 項目 | 值 |
|------|-----|
| 模板總數 | 34 |
| 設計目標 | 專為 coding agent 設計的 HTML 簡報模板庫 |
| 入門文件 | AGENTS.md（5-step 工作流） |
| 索引文件 | index.json（結構化 mood/tone/formality/density/scheme 欄位） |
| 授權 | Open Source (GitHub) |
| 每模板 | cover · mid-deck · later 三截圖 + HTML/CSS + 裝飾資產 |

## 8 大風格分類

### 1. 📰 Editorial（雜誌/編輯風 — 14 模板）

正式、有份量、設計感強的編輯美學。最適合企業簡報、季度報告、品牌介紹。

| Template | Formality | Scheme | 頁數 | 核心特徵 |
|----------|:---------:|:------:|:--:|----------|
| Biennale Yellow | high | light | 8 | 藝術雙年展海報感，荷蘭編輯風，單色黃簽名 |
| Bold Poster | medium | light | 10 | 雜誌封面感，極簡文字，大字宣言 |
| Broadside | medium-high | dark | 20 | 報紙頭版感，雙語 EN/CN，火橘單點綴 |
| Cartesian | high | light | 10 | 安靜克制，適合投資論文、白皮書 |
| Cobalt Grid | high | light | 8 | 設計研究公報風，鈷藍+奶油+網格 |
| Editorial Forest | medium | mixed | 8 | 溫暖不急促的編輯風，適合季度回顧 |
| Editorial Tri-Tone | medium-high | mixed | 8 | 時尚雜誌跨頁感，酒紅/粉/奶油三色 |
| Emerald Editorial | medium-high | mixed | 8 | 雜誌封面感，雙線刊頭裝飾 |
| Grove | medium-high | mixed | 12 | 有機自然/永續品牌，森綠+古典襯線 |
| Monochrome | high | light | 18 | 手工排版帳本風，純黑白，使用者研究 |
| Neo-Grid Bold | medium | light | 13 | 編輯新野獸主義，霓虹黃單點綴 |
| Pin & Paper | medium | light | 11 | 手工溫度，迴紋針插畫，Caveat 手寫字 |
| Soft Editorial | high | light | 12 | 文學優雅，暖紙+Cormorant Garamond |
| Vellum | high | dark | 9 | 學術沉靜，海軍藍+暖黃 Cormorant |

### 2. 📢 Bold & Punchy（大膽宣言 — 7 模板）

自信、有力、視覺衝擊。適合品牌宣言、創意 pitch、新創 Demo。

| Template | Formality | Scheme | 頁數 | 核心特徵 |
|----------|:---------:|:------:|:--:|----------|
| 8-Bit Orbit | low | dark | 10 | CRT 螢幕像素風，霓虹賽博朋克 |
| BlockFrame | medium-low | light | 10 | 新野獸派，馬卡龍霓虹色塊+粗黑邊框 |
| Coral | medium | mixed | 10 | 暖圖像編輯風，珊瑚色+Bebas Neue |
| Creative Mode | medium | light | 8 | 多色設計導向，Archivo Black 展示體 |
| People's Platform | medium-low | light | 10 | 抗議海報能量，藍橙紅 Alfa Slab+Caveat |
| Raw Grid | medium-low | light | 10 | 直接圖像自信，野獸派邊框+偏移陰影 |
| Studio | medium | dark | 12 | 全庫最大聲，黑底+電光黃 |

### 3. 💼 Professional（專業商務 — 4 模板）

乾淨、可信、不張揚。適合 B2B pitch、顧問報告、投資人簡報。

| Template | Formality | Scheme | 頁數 | 核心特徵 |
|----------|:---------:|:------:|:--:|----------|
| Blue Professional | medium-high | light | 10 | 電光鈷藍+奶油紙，現代專業 |
| Capsule | medium-low | light | 10 | 模組化 Y2K，膠囊形狀+馬卡龍點綴 |
| Long Table | medium | light | 8 | 款待/社群品牌，暖鏽紅+粗襯線混搭 |
| Signal | high | mixed | 18 | 重量級機構風，海軍藍+金，18 頁高密度 |

### 4. 🎮 Playful（活潑遊戲 — 3 模板）

好玩、懷舊、不按牌理出牌。適合教育、社群活動、非正式場合。

| Template | Formality | Scheme | 頁數 | 核心特徵 |
|----------|:---------:|:------:|:--:|----------|
| Daisy Days | low | light | 10 | 手繪雛菊 SVG，溫暖軟萌 |
| Retro Windows | low | light | 10 | Win95 懷舊風，Y2K 品牌 |
| Sakura Chroma | low | light | 8 | 80s 日式卡帶目錄風，彩虹絲帶+粗體 |

### 5. 🎨 Creative（創意 — 2 模板）

設計導向、非傳統佈局。適合設計工作室、腦力激盪。

| Template | Formality | Scheme | 頁數 | 核心特徵 |
|----------|:---------:|:------:|:--:|----------|
| Scatterbrain | low | light | 10 | 設計師白板風，便利貼+手繪線條 |
| Stencil & Tablet | medium-high | light | 11 | 考古/檔案感，模板切割標題+六色大地 |

### 6. 🤲 Warm & Crafted（溫暖手作 — 3 模板）

溫暖、親密、有人味。適合獨立品牌、創作者作品集、手工藝。

| Template | Formality | Scheme | 頁數 | 核心特徵 |
|----------|:---------:|:------:|:--:|----------|
| Mat | medium | mixed | 9 | 中世紀現代主義，鼠尾草+焦橙 |
| Playful | low | light | 10 | 獨立品牌暖色，桃子色調 |
| Retro Zine | medium-low | light | 10 | 印刷/低保真/地下雜誌風，Riso 印刷質感 |

### 7. 🌙 Dark & Moody（黑暗氛圍 — 1 模板）

| Template | Formality | Scheme | 頁數 | 核心特徵 |
|----------|:---------:|:------:|:--:|----------|
| Pink Script — After Hours | medium-high | dark | 9 | 午夜雜誌，黑底+熱粉紅+Instrument Serif |

## 設計系統通用模式

從 34 模板中萃取的通用設計原則：

### 色彩
- 67% 使用 `light` scheme（奶油/暖紙底）
- 21% `mixed`（暗底+亮色區域交替）
- 12% `dark`（全黑/全海軍藍底）
- 90%+ 使用 CSS variables（`:root` 定義）
- 典型配色：1 主色 + 1-2 輔色 + 奶油/紙底

### 字體
- 襯線體主導（Cormorant Garamond, Source Serif 4, Instrument Serif, Playfair Display, Lora）
- 展示體用於封面大標（Archivo Black, Bebas Neue, Shrikhand, Alfa Slab）
- 手寫/特殊體用於個性化（Caveat, Caveat Brush）
- 全部 Google Fonts @import

### 佈局
- Grid-based 多欄佈局最常見
- Flexbox 用於卡片/元件排列
- 裝飾元素（corner brackets, rules, shapes, SVGs）是視覺系統核心
- 導航：deck-stage.js / inline keyboard / scroll-snap

### 適用場景快速對照

| 潤思使用場景 | 推薦模板 |
|-------------|---------|
| 用友簡報（企業級） | Signal, Blue Professional, Emerald Editorial |
| 產品發表 | Neo-Grid Bold, BlockFrame, Raw Grid |
| 數據報告 | Monochrome, Neo-Grid Bold, Raw Grid |
| 品牌故事 | Soft Editorial, Pin & Paper, Grove |
| 創意 Pitch | Creative Mode, Studio, Bold Poster |
| 技術分享 | Cobalt Grid, 8-Bit Orbit, Vellum |
| 內部回顧 | Editorial Forest, Scatterbrain, Playful |