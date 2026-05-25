# 設計模式萃取 — 跨來源通用 HTML 簡報設計系統

> 從 Source 1（beautiful-html-templates 34模板）+ Source 2（nicepage.com 15,000+網站）+ Source 3-4（slides.com）萃取
> Owner: Kai
> 用途：潤思自有素材庫的設計語言基礎

## 10 套通用配色系統

從 S1 的 34 模板中萃取的 10 種配色策略，按使用場景分組。

### 1. 暖紙 + 單色點綴（Editorial/Literary）
```
背景: #faf6f0 (暖奶油) / #f5f0e8 (紙)
主色: 單一強色（鈷藍 #1a3a5c / 酒紅 #6b2737 / 翡翠綠 #2d5a3e）
輔色: 同色系 +20% lightness
文字: #1a1a1a (標題) / #4a4a4a (內文)
```
**適用**: 正式簡報、文學、季度報告、品牌介紹

### 2. Navy + Gold（Institutional/Weighty）
```
背景: #0d1b2a (深海軍)
點綴: #c9a84c (金) / #f0d78c (淡金)
文字: #ffffff (標題) / #b8c5d6 (內文)
```
**適用**: 投資人簡報、董事會報告、顧問交付物

### 3. Black + Electric Yellow（Studio/Creative）
```
背景: #0a0a0a (黑)
點綴: #ffe600 (電光黃)
內文: #ffffff / #a0a0a0
```
**適用**: 設計工作室 credentials、創意 pitch、品牌展示

### 4. Cream + Multi-Accent（Creative/Playful）
```
背景: #faf8f3 (奶油)
點綴: #2ecc71 (綠) / #e74c3c (紅) / #f39c12 (橙) / #3498db (藍)
文字: #1a1a1a
```
**適用**: 腦力激盪、設計 thinking 工作坊、非正式簡報

### 5. Forest + Dusty Pink（Organic/Warm）
```
背景: #f7f4f0 (暖紙) / #2d4a3e (森林暗區)
主色: #2d4a3e (森林綠)
輔色: #d4a5a5 (灰粉)
文字: #1a1a1a / #ffffff (暗區)
```
**適用**: 永續品牌、自然主題、CSR 報告

### 6. White + Electric Blue（Professional/Clean）
```
背景: #faf8f3 (奶油) / #ffffff
主色: #2563eb (電光藍)
輔色: #1e40af (深藍文字/線條)
文字: #1a1a1a / #4a5568
```
**適用**: B2B SaaS pitch、顧問報告、科技簡報

### 7. Dark Neon（Cyberpunk/Retro）
```
背景: #0a0a1a (深黑藍)
主色: #00ff88 (霓虹綠) / #ff00ff (霓虹紫) / #00ffff (霓虹青)
文字: #e0e0e0 / #80ff80
```
**適用**: 遊戲、web3、駭客松 demo、科幻主題

### 8. Pastel Capsule（Y2K/Modular）
```
背景: #fafafa
色塊: #e8f4f8 (淡藍) / #fce4ec (淡粉) / #e8f5e9 (淡綠) / #fff3e0 (淡橙)
邊框: #333333 (粗黑)
文字: #1a1a1a
```
**適用**: 生活品牌、創作者作品集、DTC 品牌

### 9. Tri-Tone Editorial（Fashion/Magazine）
```
背景: #faf6f0 (奶油) / #fdf2f4 (淡粉區塊)
主色: #6b2737 (深酒紅)
輔色: #d4a5a5 (灰粉)
文字: #1a1a1a / #6b2737 (強調)
```
**適用**: 時尚品牌、生活媒體、編輯簡報

### 10. Graph Paper + Cobalt（Design Research/Studio）
```
背景: #faf8f3 (網格紙紋理)
主色: #1a3a5c (鈷藍)
線條: rgba(26,58,92,0.12) (淡網格線)
文字: #1a3a5c (標題) / #4a5a6a (內文)
```
**適用**: 設計研究公報、工作室年鑑、學術報告

## 6 套標準字體配對

### 1. 襯線體標題 + 無襯線體內文（Classic Editorial）
```
標題: Cormorant Garamond / Playfair Display / Source Serif 4
內文: Inter / Jost / Work Sans
數字: Tabular lining (monospace)
```

### 2. 展示體封面 + 襯線體內容（Bold Magazine）
```
封面: Archivo Black / Bebas Neue / Shrikhand / Alfa Slab
標題: Instrument Serif / Lora
內文: Inter / Noto Sans TC
```

### 3. 全無襯線體（Modern Tech）
```
標題: Inter (w700-w900) / DM Sans / Satoshi
內文: Inter (w400-w500)
數字: JetBrains Mono / Fira Code (data)
```

### 4. 手寫體 + 無襯線體（Warm/Crafted）
```
裝飾/引用: Caveat / Caveat Brush / Kalam
標題: Jost / DM Sans
內文: Inter / Noto Sans TC
```

### 5. 古典襯線體（Scholarly/Institutional）
```
全體: Cormorant Garamond / EB Garamond / Source Serif 4
強調: Italic
內文: Regular / Book
```

### 6. 粗體無襯線 + 輕量無襯線（Neo-Brutalist）
```
標題: Archivo Black / Space Grotesk (w700)
內文: Space Grotesk (w400) / DM Sans
線條: 粗黑 border
```

## 5 種標準佈局模式

### 1. Hero Cover（封面頁）
```
結構: 垂直置中 + 大標題 + 副標 + 作者/日期
CSS: display:flex; flex-direction:column; justify-content:center; min-height:100vh
色調: 背景色 + 文字對比（light bg = dark text, dark bg = light text）
裝飾: corner brackets / rules / underlines
```

### 2. Grid Cards（卡片網格）
```
結構: 2-4 欄 grid
CSS: display:grid; grid-template-columns: repeat(3, 1fr); gap: 24px
內容: 圖片/圖標 + 標題 + 簡短描述
適合作: 功能介紹、案例展示、團隊介紹
```

### 3. Stat Grid（數據網格）
```
結構: 大數字 + 標籤 + 描述 + mono 註腳
CSS: 同 Grid Cards + 大字體數字
格式: 47% / 2.4M / +142% → 加粗大號 + 單位小號
```

### 4. Timeline / Process（流程時間線）
```
結構: 垂直線 + 節點 + 卡片
CSS: border-left + padding-left + position relative for dots
適合作: 發展歷程、專案階段、方法論
```

### 5. Quote / Statement（引言頁）
```
結構: 大字 quote + 來源
CSS: 大 font-size (2-3rem) + 居中 + 襯線體 + 前後引號裝飾
適合作: 品牌宣言、客戶證言、核心價值
```

## S1 裝飾詞彙庫

從 beautiful-html-templates 萃取的 8 種裝飾模式：

| 模式 | 說明 | CSS 實現 |
|------|------|----------|
| Corner brackets | 四角 L 型 brackets | `::before` `::after` + `border` |
| Paper grain | 紙張紋理疊層 | `background-image: url(grain.png)` + `opacity: 0.03` |
| Double rules | 雙線刊頭裝飾 | `border-top: 2px double` |
| Hand-drawn doodles | 手繪 SVG 插畫 | inline `<svg>` |
| Geometric shapes | 圓形/矩形色塊 | `border-radius: 50%` + accent color |
| Grid overlay | 網格覆層 | repeating linear-gradient |
| Stencil cutouts | 模板切割字體 | `-webkit-text-stroke` + transparent fill |
| Offset shadows | 偏移陰影 | `box-shadow: 8px 8px 0` + 野獸派風格 |

## nicepage.com 可複用 Block 元件

從 S2 萃取的簡報可直接使用的 HTML Block：

| Block | 簡報用途 | 結構 |
|-------|----------|------|
| Testimonials | 客戶證言 | 引用 + 頭像 + 姓名 + 職位 |
| Team | 團隊介紹 | 頭像 + 姓名 + 職位 + 社交連結 |
| Pricing Table | 方案對比 | 3 欄卡片 + 價格 + 功能列表 + CTA |
| FAQ Accordion | 常見問答 | dt/dd + JS toggle |
| Hero w/ Video | 影片封面 | background video + overlay + 文字 |
| Stats Counter | 數據展示 | 大數字 + 標籤 + 動畫計數 |
| Timeline | 時間線 | 垂直線 + dot + 卡片 |
| Before/After | 前後對比 | 雙圖 slider |
| Contact Form | 聯絡表單 | input + textarea + button |
| Footer CTA | 行動呼籲 | 大標題 + button |

## 跨來源合成：潤思自有素材庫架構建議

```
html-slides-library/
├── README.md              ← 總索引
├── design-system/
│   ├── colors.css         ← 10 套配色 CSS variables
│   ├── fonts.css          ← 6 套字體 @import + fallback
│   └── decorations.css    ← 8 種裝飾模式 CSS
├── templates/
│   ├── editorial/         ← 雜誌/編輯風模板
│   ├── professional/      ← 專業商務模板
│   ├── creative/          ← 創意/設計導向模板
│   └── playful/           ← 活潑/非正式模板
├── components/
│   ├── hero-cover.html    ← 封面區塊
│   ├── grid-cards.html    ← 卡片網格
│   ├── stat-grid.html     ← 數據網格
│   ├── timeline.html      ← 時間線
│   ├── quote.html         ← 引言
│   ├── testimonials.html  ← 證言
│   ├── team.html          ← 團隊
│   └── pricing.html       ← 方案對比
└── patterns/
    ├── color-systems.md   ← 配色系統（待 Smart 合流）
    ├── font-pairings.md   ← 字體配對（待 Smart 合流）
    └── layout-patterns.md ← 佈局模式（待 Smart 合流）
```