# Typography Scale · 字級階層分析

- **來源**: beautiful-html-templates（34 模板）
- **提取日期**: 2026-05-25
- **提取者**: Technus (Beta Squad)

## 字級階層系統總覽

beautiful-html-templates 使用 **vw-based 流體字級**（fluid typography），配合 `clamp()` 確保最小/最大字級。這是現代投影片的最佳實踐 — 投影片尺寸 = 螢幕尺寸，vw 直接對應視覺比例。

### 標準八級階層（從 monochrome 模板提取）

| 層級 | CSS Variable | 典型值 | 用途 |
|:--:|------|------|------|
| Display | `--sz-display` | 8.5vw | 封面大標 · Hero statement |
| H1 | `--sz-h1` | 5vw | 章節標題 · Chapter title |
| H2 | `--sz-h2` | 3.2vw | 投影片標題 · Slide headline |
| H3 | `--sz-h3` | 2vw | 副標題 · Sub-headline |
| Lead | `--sz-lead` | 1.5vw | 導言 · 摘要段落 |
| Body | `--sz-body` | 1.1vw | 內文 · 段落文字 |
| Caption | `--sz-caption` | 0.85vw | 圖說 · 註腳 |
| Label | `--sz-label` | 0.72vw | 標籤 · 側欄文字 |

### 實用 clamp() 轉換

```
display: clamp(48px, 8.5vw, 120px)
h1:      clamp(32px, 5vw, 72px)
h2:      clamp(24px, 3.2vw, 48px)
h3:      clamp(18px, 2vw, 32px)
body:    clamp(14px, 1.1vw, 18px)
caption: clamp(11px, 0.85vw, 14px)
```

## 字體家族生態

### 拉丁字體（Display · Heading · Body）

| 角色 | 字體 | 出現次數 | 範本 |
|------|------|:--:|------|
| **Serif Display** | Playfair Display | 4 | cartesian, soft-editorial, grove, vellum |
| | Cormorant Garamond | 3 | soft-editorial, vellum, biennale-yellow |
| | Instrument Serif | 3 | pink-script, editorial-tri-tone, editorial-forest |
| | Lora | 3 | monochrome, editorial-forest, grove |
| | Libre Baskerville | 2 | bold-poster, mat |
| **Sans Display** | Archivo Black | 3 | creative-mode, signal, block-frame |
| | Bebas Neue | 2 | coral, retro-zine |
| | Shrikhand | 2 | bold-poster, scatterbrain |
| | Syne | 2 | playful, daisy-days |
| | Alfa Slab One | 1 | peoples-platform |
| **Body Sans** | Inter | 5 | blue-professional, cartesian, signal, vellum, stencil-tablet |
| | Space Grotesk | 4 | bold-poster, neo-grid-bold, raw-grid, mat |
| | Jost | 3 | monochrome, capsule, cobalt-grid |
| **Mono** | JetBrains Mono | 8 | 全模板使用（labels/chrome/meta） |
| | DM Mono | 2 | 8-bit-orbit, retro-windows |

### 中文字體配對（from chinese-font-guide.html）

| 拉丁字體 | 中文配對 | 適用場景 |
|------|------|------|
| Playfair Display / Cormorant | **Noto Serif SC** 700/900 | 正式簡報 · 品牌故事 |
| Inter / Space Grotesk | **Noto Sans SC** 400/500/700 | 企業簡報 · 產品發表 |
| Instrument Serif / Lora | **LXGW WenKai TC** | 文學/文化類 · 柔和氛圍 |
| Archivo Black / Shrikhand | **ZCOOL KuaiLe** | 活潑/創意提案 |
| Bebas Neue | **Smiley Sans Oblique** | 現代/科技感 |
| 手寫風格 (Caveat) | **Ma Shan Zheng** / **Long Cang** | 工作坊 · 非正式場合 |

## 字級配對模式

### 模式 A：Serif Display + Sans Body（正式/經典）
```
Display: Playfair Display 900 @ 8.5vw
H1:     Playfair Display 700 @ 5vw
Body:   Inter 400 @ 1.1vw
Caption: Inter 400 @ 0.85vw
```
> 適用: cartesian, soft-editorial, vellum, grove

### 模式 B：Sans Display + Sans Body（現代/簡潔）
```
Display: Archivo Black @ 8.5vw
H1:     Space Grotesk 700 @ 5vw
Body:   Space Grotesk 400 @ 1.1vw
Caption: Space Grotesk 400 @ 0.85vw
```
> 適用: blue-professional, signal, creative-mode

### 模式 C：Mixed Serif/Sans（對比/編輯感）
```
Display: Instrument Serif italic @ 8.5vw
H1:     Bricolage Grotesque 700 @ 5vw
Body:   Inter 400 @ 1.1vw
```
> 適用: editorial-tri-tone, emerald-editorial, editorial-forest

### 模式 D：Display Heavy（海報/宣言）
```
Display: Shrikhand @ 12vw
H2:     Space Grotesk 700 @ 3.2vw
Body:   Libre Baskerville 400 @ 1.3vw
```
> 適用: bold-poster, peoples-platform, studio

## 對我們簡報的建議

### P0 用友（企業級）
- **Display**: Noto Serif SC 900
- **Heading**: Noto Sans SC 700
- **Body**: Noto Sans SC 400
- **字級**: 模式 A（Serif Display + Sans Body）
- **模板參考**: blue-professional, signal

### P3 APS/CRIS（科技/產品）
- **Display**: Noto Sans SC 900
- **Heading**: Noto Sans SC 700
- **Body**: Noto Sans SC 400
- **字級**: 模式 B（Sans Display + Sans Body）
- **模板參考**: neo-grid-bold, creative-mode

### 關鍵規則
1. ⚠️ **vw 字級在 1920px 螢幕才正確** — 小螢幕需 `clamp()` 下限
2. ⚠️ **CJK 字體行高需 +0.1-0.2** — 中文字元高度大於拉丁字元
3. ✅ **只需一個 display 字重 + 兩個 body 字重** — 過多字重破壞層次
4. ✅ **永遠配對 mono 字體給標籤/數字** — JetBrains Mono 是標配