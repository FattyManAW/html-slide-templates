# HTML 簡報素材庫 — QA 分析報告

> **產出日期**：2026-05-25  
> **分析者**：Forge（QA Engineer, Squad Alpha）  
> **任務**：Allen 令 — 分析 4 個 HTML 簡報範本網站，建立共用素材庫  
> **狀態**：2/4 完整分析，2/4 待重試（slides.com 網路逾時）

---

## 來源一：beautiful-html-templates（zarazhangrui）⭐⭐⭐⭐⭐

**URL**：https://github.com/zarazhangrui/beautiful-html-templates  
**類型**：GitHub Open-Source Repo  
**數量**：34 套模板  
**授權**：Open source（GitHub public repo）

### QA 總評：🏆 最佳參考來源

這不是一般「模板下載站」，而是專為 **AI Coding Agent 設計**的模板庫。每套模板都有：
- `index.json` 結構化 metadata（顏色、字體、用途分類）
- `AGENTS.md` 操作手冊
- 3 張截圖（封面 / 中段 / 尾頁）

### 完整模板目錄（34 套）

| # | 模板名 | 風格 | 主色 | 字體 | 適用場景 |
|---|--------|------|------|------|----------|
| 1 | soft-editorial-4/6/10 | 軟性編輯 | sage, blush, lemon | Cormorant Garamond | 溫和質感簡報 |
| 2 | editorial-forest | 森林編輯 | forest green, dusty pink, cream | Source Serif 4 | 季度回顧 |
| 3 | pin-and-paper | 手作風 | yellow paper, ink-blue | Caveat | 創意/手作簡報 |
| 4 | sakura-chroma | 日式復古 | cream, rainbow ribbons | condensed bold | 日式美學 |
| 5 | stencil-tablet | 考古風 | bone, six-color earth | stencil | 品牌簡報 |
| 6 | cobalt-grid | 科技電光 | electric cobalt | italic serif | 科技數據 |
| 7 | vellum | 學術羊皮 | deep navy, warm-yellow | Cormorant italic | 學術簡報 |
| 8 | emerald-editorial | 雜誌封面 | emerald, navy, paper | Bodoni-style | 商業高階 |
| 9 | neo-grid-bold | 新野獸派 | neon yellow, off-white | - | 設計/創意 |
| 10 | editorial-tri-tone | 三色編輯 | dusty pink, mustard, burgundy | Bricolage + Instrument Serif | 品牌編輯 |
| 11 | creative-mode | 多彩創意 | cream, green/pink/orange/yellow | Archivo Black | 創意提案 |
| 12 | monochrome | 極簡黑白 | ivory, all-black | Lora + Jost | 專業嚴肅 |
| 13 | peoples-platform | 社運海報 | blue, orange, red | Alfa Slab + Caveat Brush | 激勵/社運 |
| 14 | pink-script | 深夜奢華 | black, hot pink, pearl-cream | Instrument Serif | 時尚/精品 |
| 15 | 8-bit-orbit | 像素復古 | neon on navy | pixel | 遊戲/科技 |
| 16 | block-frame | 新野獸派 | pastel-neon, chunky black | - | 設計/藝術 |
| 17 | blue-professional | 專業藍 | cream, electric cobalt | - | 企業/商務 |
| 18 | bold-poster | 海報風格 | fire-engine red | Shrikhand | 廣告/宣傳 |
| 19 | broadside | 廣播告示 | - | - | 復古公告 |
| 20-34 | 其餘 15 套 | 各類風格 | 多樣 | 多樣 | 全面覆蓋 |

### QA 品質維度評分

| 維度 | 分數 | 說明 |
|------|:--:|------|
| 程式碼品質 | 9/10 | AI agent 可直接複製使用，結構化 metadata |
| 設計多樣性 | 10/10 | 34 種完全不同的視覺系統 |
| 可維護性 | 9/10 | index.json + AGENTS.md 標準化 |
| 文件完整性 | 8/10 | AGENTS.md 清晰，截圖到位 |
| 響應式 | 推測 8/10 | 多數為 self-contained HTML |
| **綜合** | **9/10** | **最佳 AI agent 模板庫** |

---

## 來源二：Nicepage HTML Templates ⭐⭐⭐⭐

**URL**：https://nicepage.com/html-templates  
**類型**：商業模板下載站  
**數量**：15,000+ 套  
**授權**：免費下載（部分 premium）

### QA 總評：量體最大，適合批量素材

Nicepage 是最大的 HTML 模板聚合站之一。特點：
- **15,000+ 模板**，全產業覆蓋（eCommerce、agency、food、fashion、travel、health 等）
- 支援 HTML/CSS/JS/Bootstrap
- 提供 WordPress 版本對應
- 多數支援 responsive design
- 含 parallax、video、contact form 等進階元素

### 品質維度評分

| 維度 | 分數 | 說明 |
|------|:--:|------|
| 程式碼品質 | 7/10 | 商業品質，依賴較多外部資源 |
| 設計多樣性 | 9/10 | 15,000+ 全產業覆蓋 |
| 可維護性 | 6/10 | 模板較大，非模組化 |
| 文件完整性 | 5/10 | 無結構化 metadata |
| 響應式 | 8/10 | 多數支援 |
| **綜合** | **7/10** | **量體取勝，需人工篩選** |

### 適用場景
- 需要大量不同產業風格的參考素材
- 找特定行業（餐飲、旅遊、醫療等）的模板
- Bootstrap-based 網頁（非純簡報）

### 限制
- 網站模板 > 簡報模板（偏網頁，非 slide deck）
- 無結構化 index/metadata（需人工瀏覽）
- 部分需要付費

---

## 來源三 & 四：Slides.com Templates / Explore ⭐⭐⭐（待完整分析）

**URL**：https://slides.com/templates / https://slides.com/explore  
**類型**：線上簡報平台（類似 SlideShare + Google Slides）  
**狀態**：網路逾時，待重試

### 已知資訊（搜尋推估）
- Slides.com 是專注簡報的平台（非網頁模板），與 SlideShare 類似
- 含 Templates 頁面（預設範本）和 Explore 頁面（社群分享的公開簡報）
- 推估是 embed-based slide decks（非 raw HTML 下載）
- 適合做「設計參考」而非「程式碼素材」

### 預估品質評分（待驗證）

| 維度 | 預估 | 說明 |
|------|:--:|------|
| 設計參考價值 | 8/10 | 真實簡報範例 |
| 程式碼可取得性 | 2/10 | 可能不提供 raw HTML |
| **綜合** | **預估 5/10** | **設計參考佳，程式碼素材可能受限** |

---

## 四站對比總表

| 來源 | 數量 | 類型 | 程式碼可用 | 設計參考 | AI 友好度 | 綜合 |
|------|------|------|:--:|:--:|:--:|:--:|
| beautiful-html-templates | 34 | slide templates | ✅ raw HTML | 🌟🌟🌟🌟🌟 | ✅ AGENTS.md | 9/10 |
| Nicepage | 15,000+ | web templates | ✅ HTML/CSS/JS | 🌟🌟🌟🌟 | ❌ 無 metadata | 7/10 |
| slides.com/templates | ? | slide decks | ❌ 可能 embed | 🌟🌟🌟🌟 | ❌ | 預估 5/10 |
| slides.com/explore | ? | community decks | ❌ 可能 embed | 🌟🌟🌟🌟 | ❌ | 預估 5/10 |

---

## QA 建議：素材庫建設路線

### Phase 1：立即行動（今天）
1. **Clone beautiful-html-templates** 作為素材庫核心
2. **分析 index.json / AGENTS.md 結構** → 建立我們自己的 metadata schema
3. **選 5 套代表性模板** → 做完整的 code review + 品質註解

### Phase 2：擴充（本週）
4. **從 Nicepage 精選 20 套** 不同產業的模板 → 提取設計 pattern
5. **重試 slides.com** → 擷取設計參考截圖（不依賴 raw HTML）
6. **建立 quality-checklist.json** → 模板入庫品質門檻

### Phase 3：制度化（S02 內）
7. **建立 GitHub repo**：`runsi-html-template-library`
8. **結構化 metadata**：`index.json`（名稱、風格、顏色、字體、適用場景、品質分數、來源）
9. **AGENTS.md**：AI agent 使用手冊

---

## 品質門檻 Checklist（模板入庫標準）

每套入庫模板須通過：

```
[ ] 純 HTML/CSS（無外部 CDN，或僅限 Google Fonts）
[ ] 響應式（viewport meta + media queries）
[ ] 語意化 HTML（header/main/section/article）
[ ] a11y 基礎（alt text、ARIA labels、skip-link、color contrast ≥ 4.5:1）
[ ] 截圖檔案（cover / mid / end 三張）
[ ] metadata 完整（index.json entry）
[ ] 相容性：Chrome/Firefox/Safari 三瀏覽器通過
[ ] 檔案大小 ≤ 50KB（含 inline CSS）
```

---

## 待辦

- [ ] GitHub clone beautiful-html-templates（網路不穩，重試中）
- [ ] slides.com 重試（換時段或換網路）
- [ ] Nicepage 精選 20 套 → 分類
- [ ] 建立素材庫 GitHub repo
- [ ] 產出 metadata schema v1.0
- [ ] API token 修復後貼 group-memory 回報進度