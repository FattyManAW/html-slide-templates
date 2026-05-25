# 設計 Tokens 萃取 — HTML 簡報素材庫

> 來源: beautiful-html-templates (34 templates)
> Token 來源: 上游 `template.json` + `design.md`（GitHub API）
> 萃取: Ray (G7 Release Gate), 2026-05-25

## 設計 Token 概念

每個模板的 `template.json` 和 `design.md` 包含結構化的設計變數，可作為產品規劃組和開發組建立「我們自己的簡報」時的參考基礎。

## 範例 Token 萃取（5 個代表性模板）

### 1. Soft Editorial（編輯風 · 低密度 · 高正式度）

```yaml
palette:
  paper: "#F2EEDF"       # 暖紙底
  ink: "#2A241B"          # 深墨色
  accent-pink: "#E1A4C2"
  accent-lemon: "#D6DD63"
  accent-blush: "#E8C9B6"
  accent-sage: "#B7C7A8"
  card-fill: "rgba(255,255,255,0.55)"
  rule-soft: "rgba(42,36,27,0.18)"

display-font: "Cormorant Garamond"   # 高對比 garalde 襯線
body-font: "Work Sans"               # 乾淨人文無襯線
headline-weight: 500
card-radius: 24-36px

best_for: [editorial-feature, longform-brand-story, gallery-museum, literary-pitch]
scheme: light
slide_count: 12
```

### 2. Emerald Editorial（商務雜誌 · 翡翠綠+海軍藍）

> 適用: 產品發表簡報、商業提案、品牌識別
> 配色: 翡翠綠 + 海軍藍 + 紙白
> 字型: Bodoni 風格粗襯線（雙線條刊頭裝飾）
> Token 關鍵字: `masthead ornaments`, `double-rule`, `magazine-cover weight`

### 3. Bold Poster（海報風 · 大字 · 單色重點）

```yaml
palette:
  bg: "#FFFFFF"
  dark: "#1C1410"
  red: "#D8000F"         # 唯一顏色: 消防車紅
  light: "#F5F2EF"

display-font: "Shrikhand"            # 巨大海報字體
serif-font: "Libre Baskerville"      # 編輯襯線
body-font: "Space Grotesk"           # 怪誕無襯線
typographic-contrast: "very-high"

best_for: [brand-manifesto, creative-pitch, magazine-editorial, founder-vision]
scheme: light
slide_count: 10
```

### 4. Retro Windows（懷舊 · 像素 · Win95）

```yaml
palette:
  bg-gray: "#C0C0C0"     # Win95 底色
  title-navy: "#000080"  # 標題列深藍
  accent-blue: "#1084D0" # Win95 藍
  white: "#FFFFFF"
  black: "#000000"

display-font: "Press Start 2P"       # 8-bit 像素字
body-font: "MS Sans Serif"           # 微軟系統字
mono-font: "VT323"                   # DOS 終端字
border-style: "3D inset/outset, no anti-aliasing"

best_for: [retro-gaming, Y2K-brand, tech-history, developer-tools]
scheme: light
slide_count: 10
```

### 5. Blue Professional（現代專業 · 單色藍 · 乾淨）

```yaml
palette:
  bg: "#FDFAE7"          # 暖奶油紙
  primary: "#1E2BFA"     # 唯一重點色: 電鈷藍
  text: "#111111"
  text-muted: "#6B6B6B"

display-font: "Space Grotesk"
body-font: "Inter"
style: "modern sans-only, no decorative flourishes"

best_for: [B2B-SaaS-pitch, consulting-deliverable, advisory-pitch, investor-update]
scheme: light
slide_count: 10
```

### 6. Daisy Days（友善 · 手繪 · 全粉彩）

```yaml
palette:
  cream: "#F5F0E6"
  turquoise: "#7ECDC0"
  soft-pink: "#F7C8D4"
  butter: "#FDE68A"
  mint: "#A8E6CF"
  lavender: "#D4A5E8"
  peach: "#FFCBA4"
  coral: "#F8635F"
  outline: "3px solid #2D2D2D"
  shadow: "6px offset"

display-font: "Fredoka One"   # 圓角無襯線
body-font: "Quicksand"        # 友善幾何無襯線
ink-color: "#2D2D2D"          # 墨黑

best_for: [education, kids-brand, wellness, community-workshop, team-kickoff]
scheme: light
slide_count: 10
```

### 7. Signal（機構級 · 雙語 · 沉穩）

```yaml
palette:
  bg: "#1c2644"          # 深藍畫布
  alt: "#232f55"
  fg: "#e2dcd0"          # 骨白紙
  accent: "#c8a870"      # 啞金（唯一強調色）
  light: "#f0ece3"

display-font: "Source Serif 4"
body-font: "DM Sans"
mono-font: "IBM Plex Mono"
chinese-serif: "Noto Serif SC"      # 中文襯線
chinese-sans: "Noto Sans SC"        # 中文無襯線

best_for: [investor-deck, board-presentation, legal-brief, bilingual-deck]
scheme: mixed
slide_count: 18
```

## 跨模板 Design Token 模式

### 配色策略（依型式）

| 配色策略 | 模板 | 特色 |
|---------|------|------|
| **單色+紙底** | Blue Professional, Signal, Bold Poster | 1-2 accent 色 + 暖紙底 |
| **全彩粉彩** | Daisy Days, Creative Mode, Capsule | 6-9 彩度 + 墨線 |
| **暗底+高對比** | Pink Script, Studio, 8-bit-orbit, Vellum | 黑/深藍底 + 1-2 亮色 |
| **自然/大地** | Grove, Mat, Editorial Forest, Stencil Tablet | 森林綠 + 鏽 + 奶油 |
| **雙色編輯** | Emerald Editorial, Editorial Tri-tone | 主色+輔色+紙 | 
| **復古系統** | Retro Windows, Retro Zine, Sakura Chroma | 時代特有調色板 |

### 字型配對策略

| 配對模式 | 模板 | 場景 |
|---------|------|------|
| **高對比襯線+無襯線** | Soft Editorial, Bold Poster | 編輯/海報 |
| **單一無襯線家族** | Blue Professional, Neo Grid Bold | 現代專業 |
| **像素+系統字** | Retro Windows, 8-bit-orbit | 復古/遊戲 |
| **圓角友好** | Daisy Days, Playful, Scatterbrain | 教育/友善 |
| **中英雙語** | Signal (Noto Serif/Sans SC), Broadside | 國際化/雙語 |

### 排版密度 × 正式度矩陣

```
         formal ────────────────────────── informal
           │                                  │
high       │  Signal              BlockFrame  │
density    │  Emerald Editorial    Raw Grid   │
           │                                  │
           │  Soft Editorial      Scatterbrain│
medium     │  Blue Professional   Capsule     │
           │  Bold Poster         Playful     │
           │                                  │
           │  Cartesian           Daisy Days  │
low        │  Vellum              8-bit-orbit │
density    │                      Retro Zine  │
           │                                  │
```

## 給開發組的建議

1. **建立 CSS 變數系統** — 每個模板的 color/typography tokens 可以直接轉換成 CSS custom properties
2. **可重用元件庫** — Hero section, card grid, timeline, data display, team section 每個模板都有獨特版本
3. **主題切換機制** — 34 模板的 token 差異主要來自 palette + typography，可建立「主題變數」系統一鍵切換
4. **中文字型對應** — 目前僅 Signal 有 CJK 字型堆疊，需要為每個模板建立中文字型後備方案