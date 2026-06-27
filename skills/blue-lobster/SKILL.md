---
name: blue-lobster
description: Blue Lobster 設計系統——使用者 的個人暗色 UI/UX 風格規範（深夜黑底 + Lark 藍紫漸層 + 玻璃質感 + 動態呼吸）。任何涉及做網頁、App、儀表板、元件、介面、前端畫面、原型、設計稿的任務都預設套用此規範，即使用戶沒明說要「Blue Lobster 風格」也要主動套用，除非創辦人明確指定其他風格。
---

# Blue Lobster Design System

使用者 的個人 UI/UX 設計風格規範。
任何 UI 任務預設套用此規範，除非創辦人明確指定其他風格。

---

## 設計原則

- **暗色為王**：深夜黑底，不做白色主題
- **藍紫漸層**：Lark 藍 × 紫羅蘭，帶科技感光效
- **玻璃質感**：毛玻璃 backdrop-blur，卡片帶微光邊框
- **動態呼吸**：進度、狀態用動畫表達，不靜態等待

---

## 色盤（Blue Lobster v1）

| Token | 值 | 用途 |
|---|---|---|
| `--bg` | `#0F1117` | 頁面底色（深夜黑）|
| `--card` | `#1A1D2E` | 卡片、面板底色 |
| `--card-deep` | `#13162A` | sidebar、header 深底 |
| `--secondary` | `#23263A` | 次要區塊、hover |
| `--primary` | `#1456F0` | Lark 藍，CTA 按鈕、active |
| `--accent` | `#6B3FF5` | 紫羅蘭，強調、漸層尾 |
| `--text` | `#E8EAED` | 主要文字 |
| `--text-secondary` | `#9CA3AF` | 次要文字 |
| `--muted` | `#6B7280` | placeholder、disabled |
| `--subtle` | `#4B5563` | 時間戳、輔助資訊 |
| `--border` | `rgba(99,102,241,0.2)` | 卡片邊框（靛藍透明）|
| `--border-active` | `rgba(20,86,240,0.4)` | 選中狀態邊框 |
| `--success` | `#00C48C` | 成功狀態 |
| `--error` | `#EF4444` | 失敗、刪除 |
| `--progress` | `linear-gradient(90deg,#1456F0,#6B3FF5)` | 進度條 |
| `--logo-gradient` | `linear-gradient(135deg,#1456F0,#6B3FF5)` | Logo、heading 漸層 |

---

## 元件規格

### 按鈕

```css
/* 主要 CTA */
background: linear-gradient(135deg, #1456F0, #6B3FF5);
color: #fff;
border-radius: 0.5rem;
box-shadow: 0 2px 12px rgba(20,86,240,0.3);

/* 次要 / Ghost */
background: rgba(99,102,241,0.1);
color: #A5B4FC;
border: 1px solid rgba(99,102,241,0.2);

/* 危險 */
background: rgba(239,68,68,0.1);
color: #EF4444;
border: 1px solid rgba(239,68,68,0.2);
```

### 卡片

```css
background: #1A1D2E;
border: 1px solid rgba(99,102,241,0.15);
border-radius: 0.75rem;
box-shadow: 0 0 0 1px rgba(99,102,241,0.05), 0 4px 24px rgba(0,0,0,0.4);
```

### Header / Sticky Bar

```css
background: rgba(26,29,46,0.8);
border-bottom: 1px solid rgba(99,102,241,0.2);
backdrop-filter: blur(12px);
```

### Tab 指示器

```css
/* Active underline */
background: linear-gradient(90deg, #1456F0, #6B3FF5);
height: 2px;
border-radius: 2px 2px 0 0;
```

### 進度條

```css
/* Track */
background: rgba(99,102,241,0.15);
height: 6px;
border-radius: 9999px;

/* Fill */
background: linear-gradient(90deg, #1456F0, #6B3FF5);
box-shadow: 0 0 8px rgba(107,63,245,0.6);
transition: width 700ms ease;
```

### Logo / 品牌文字

```css
background: linear-gradient(135deg, #1456F0, #6B3FF5);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
font-weight: 700;
```

---

## 字型規格

- 字型：`-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif`
- 主要文字：14px / `#E8EAED`
- 次要文字：12px / `#6B7280`
- 標題：16px bold / `#E8EAED`
- 等寬（進度數字）：`font-mono`

---

## 動效規格

- 卡片 hover：`transition: all 200ms`
- 進度條更新：`transition: width 700ms ease`
- Loading 文字：`animate-pulse`
- Tab 切換：`transition-colors`

---

## 參考作品

- **CaptureOS**（`~/claude-workspace/capture-os`）— v1 實作，2026-06-20

---

## 版本歷史

| 版本 | 日期 | 說明 |
|---|---|---|
| v1.0 | 2026-06-20 | 初版，CaptureOS 實作確立 |
