# HTML Template Quality Checklist

> Forge QA Gate Standard | v1.0 | 2026-05-25

每套入庫 HTML 簡報模板必須通過以下品質門檻。不合格者標記 `qaStatus: needs-review` 並附註原因。

## Tier 1 — 必備（全部通過才可入庫）

```
[ ] T1.1  純 HTML/CSS，無外部 runtime CDN 依賴（Google Fonts 除外）
[ ] T1.2  <meta name="viewport"> 存在且正確
[ ] T1.3  檔案總大小 ≤ 200KB（含 inline CSS/JS）
[ ] T1.4  無 console errors（Chrome DevTools 驗證）
[ ] T1.5  至少 3 張截圖（封面 / 中段 / 尾頁）
[ ] T1.6  語意化 HTML（header / main / section 結構）
[ ] T1.7  <title> 標籤存在且有意義
```

## Tier 2 — 建議（至少通過 5/8）

```
[ ] T2.1  響應式：≥ 2 breakpoints（mobile < 768px + desktop ≥ 1024px）
[ ] T2.2  色彩對比度 ≥ WCAG AA（文字 4.5:1 / 大文字 3:1）
[ ] T2.3  alt 屬性存在於所有 <img>
[ ] T2.4  skip-link 或 ARIA landmark roles
[ ] T2.5  列印樣式（@media print）基本可用
[ ] T2.6  無使用 !important（或 ≤ 3 處且有正當理由）
[ ] T2.7  CSS 不使用 inline style（class-based）
[ ] T2.8  在 Chrome / Firefox / Safari 三瀏覽器均正常渲染
```

## Tier 3 — 加分（可選）

```
[ ] T3.1  無 JavaScript（純 HTML/CSS 簡報）
[ ] T3.2  含淺色/深色模式切換
[ ] T3.3  CSS custom properties（變數）用於主題色
[ ] T3.4  動畫/過渡效果存在且非侵入式
[ ] T3.5  字體 fallback stack 正確（至少含 sans-serif 或 serif fallback）
```

## 品質分數換算

```
Tier 1 全部通過    → a11y ≥ 5
Tier 1 + Tier 2 ≥ 5 → a11y ≥ 7
Tier 1 + Tier 2 ≥ 7 → a11y ≥ 8
Tier 1 + Tier 2 All + Tier 3 ≥ 3 → a11y = 10
```

## 失敗處理

| 失敗項目 | 處理方式 |
|----------|----------|
| T1 任何一項 fail | `qaStatus: failed`，退回不錄入 |
| T2 < 5 項 pass | `qaStatus: needs-review`，附改善建議 |
| T2 ≥ 5 項 pass | `qaStatus: passed`，入庫 |