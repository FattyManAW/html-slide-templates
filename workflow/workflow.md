# 模板挑選工作流（5-Step）

> 取自 beautiful-html-templates AGENTS.md，Kai 萃取整理
> 適用範圍：任何 coding agent 透過本素材庫建立 HTML 簡報

## Step 1: 問使用者（不可跳過）

每次建立簡報前，先問使用者兩個問題：

1. **場合**（occasion）：創始人 pitch、研究整理、品牌宣言、課程開場等
2. **情緒/氛圍**（mood/vibe）：自信有力、安靜文學、溫暖活潑、黑暗氛圍

即使簡報需求看起來很清楚，也要問——使用者的品味常常在意想不到的地方。

> ❌ 不要問「這是金融還是科技領域的？」
> ✅ 要問「應該感覺精緻有權威感，還是溫暖有設計感？」

## Step 2: 匹配模板（3 個候選）

讀取 index.json，將使用者的場合 + mood 對應到每個模板的以下欄位：

| 欄位 | 用途 |
|------|------|
| `mood` | 情緒形容詞，對應使用者的感覺關鍵詞 |
| `tone` | 聲音/個性 |
| `best_for` | 最適合感覺 + 範例場景 |
| `avoid_for` | 色調衝突 — 軟警示，非硬規則 |
| `formality` | 正式程度（low → high） |
| `density` | 每頁可容納內容量 |
| `scheme` | light / dark / mixed |

挑選 3 個**真正不同**的模板：
- 如果使用者的簡報是 editorial 風格 → 挑一個 editorial、一個更溫暖的替代、一個重新詮釋需求的 wildcard
- 不要挑三個 editorial 模板！

## Step 3: 預覽（Title Slide Only）

對每個 3 個候選：
1. 讀 template.html 的視覺系統
2. **只取第一頁**（封面/標題頁）
3. 把預留內容換成使用者的真實內容
4. 存為獨立 HTML（previews/01-<template>.html）
5. 開啟瀏覽器預覽

## Step 4: 讓使用者挑選

不要用文字解釋取捨——直接給三個預覽路徑。

## Step 5: Clone + 自適應

使用者挑選後：
- Clone 完整模板到專案資料夾
- **保留不替換**：字體、色板、網格、裝飾、導航、CSS class
- **替換**：標題、內文、數字、名稱、圖片
- **擴展**：內容超過 → duplicate 既有 layout；不夠 → drop 底部 slide
- **設計缺失 layout**：用同一設計系統自行設計（同字體、同色板、同裝飾詞彙、同間距節奏）

## 關鍵原則

### 保留（Preserve）— 永遠不變
- 字體（Google Fonts @import / font-family）
- 色板（CSS variables）
- 佈局網格（grid / flex）
- 裝飾元素（corner brackets, paper grain, shapes, SVGs）
- 導航系統（deck-stage.js / keyboard / scroll-snap）
- Slide-level CSS classes

### 替換（Replace）— 換成真實內容
- 標題（h1, h2, h3）
- 內文（p, li, caption）
- 數字/統計（47%, 2.4M, +142%）
- 名稱/日期/屬性
- 區塊標籤（[Topic], [Year], [Studio]）
- 圖片預留（Image Placeholder → 真實圖片，同尺寸）

### 品味優先
模板有「色調」，不是「行業」。使用者品味高於一切。
- Confident editorial deck 可以承載 tech talk
- Playful pastel deck 可以承載 finance review
- 只要使用者想要那個感覺，它就適用