# 金字塔原理 — 全文 Reference 索引

Barbara Minto《The Pyramid Principle / 金字塔原理》中文版（簡體）全書內文，由原始 PDF 經 macOS Vision OCR 萃取。日常套用看 `../SKILL.md` 即可；以下各章檔供需要查證原文細節、範例、技巧時**按需讀取**（不要一次全讀）。

每個章檔開頭都標了對應的原書頁碼，並有 `## 本章小節` 檔內 TOC。內文為簡體中文（書本身是簡體版）。

## 各章主題

| 檔案 | 章節 | 主題 / 何時讀 |
|------|------|--------------|
| ch00-preface-intro | 中文版序 + 前言 | 全書概念總覽、Minto 寫作緣起、金字塔結構為何有效 |
| ch01-why-pyramid | 第1篇 表達的邏輯 / 第1章 為什麼要用金字塔結構 | 歸類分組、自上而下表達（結論先行）、自下而上思考。**最核心入門章** |
| ch02-internal-structure | 第2章 金字塔內部的結構 | 縱向關係（疑問/回答）、橫向關係（演繹/歸納）、序言的結構 |
| ch03-building-pyramid | 第3章 如何構建金字塔 | 自上而下法、自下而上法、初學者注意事項。**實際動手搭金字塔的步驟** |
| ch04-preface-writing | 第4章 序言的具體寫法 | 序言講故事結構（SCQA：背景-衝突-疑問-答案）、常見序言模式、咨詢案例。**寫開場/序言查這章** |
| ch05-deductive-inductive | 第5章 演繹推理與歸納推理 | 演繹 vs 歸納的差別與使用時機 |
| ch06-logical-order | 第2篇 思考的邏輯 / 第6章 應用邏輯順序 | 時間順序、結構順序、程度順序——同組論點怎麼排 |
| ch07-summarizing-groups | 第7章 概括各組思想 | 總結句寫法、避免「缺乏思想」的空洞句、找出各結論的共性。**寫 key line 標題查這章** |
| ch08-defining-problem | 第3篇 解決問題的邏輯 / 第8章 界定問題 | 界定問題的框架、展開問題要素、發掘讀者疑問、開始寫序言 |
| ch09-structured-analysis | 第9章 結構化分析問題 | 從資料入手、設計診斷框架、建立邏輯樹、是非問題分析 |
| ch10-written-presentation | 第4篇 演示的邏輯 / 第10章 在書面上呈現金字塔 | 突出文章框架結構、上下文過渡。**做書面報告排版查這章** |
| ch11-ppt-presentation | 第11章 在 PPT 演示文稿中呈現金字塔 | 文字 PPT 幻燈片、圖表 PPT 幻燈片、故事梗概設計。**做簡報查這章** |
| ch12-between-the-lines | 第12章 在字裡行間呈現金字塔 | 畫腦圖（在大腦中畫圖像）、把圖像複製成文字 |
| appendix1-unstructured-problem-solving | 附錄1 在無結構情況下解決問題的方法 | 分析法 vs 科學法 |
| appendix2-preface-examples | 附錄2 序言結構範例 | 多個真實序言/文件範例與評析。**找實例參考查這裡** |
| appendix3-key-points | 附錄3 本書要點匯總 | 全書每章要點濃縮。**想快速複習全書精華讀這個** |
| references-bibliography | 參考文獻 | Minto 引用書目 |

## 快速指引（依任務找章檔）

- 想理解整套原理 → ch00-preface-intro、ch01-why-pyramid、appendix3-key-points
- 動手搭金字塔 → ch03-building-pyramid
- 寫開場/序言（SCQA） → ch04-preface-writing、appendix2-preface-examples
- 同組論點排序 → ch06-logical-order
- 寫小標題/總結句 → ch07-summarizing-groups
- 解決問題 / 診斷框架 / 邏輯樹 → ch08-defining-problem、ch09-structured-analysis
- 做書面報告 → ch10-written-presentation
- 做 PPT 簡報 → ch11-ppt-presentation
- 快速複習全書 → appendix3-key-points

## 萃取方法備註

原 PDF 文字層損壞（CID TrueType 缺 ToUnicode，pdftotext / pymupdf 皆撈不出文字）。改用：pymupdf 渲染每頁為 200dpi PNG → macOS Vision 框架（`VNRecognizeTextRequest`, `recognitionLanguages=["zh-Hant","en-US"]`）逐頁 OCR。已清除頁眉頁腳、頁碼、篇章裝飾字圖雜訊。OCR 品質高，少數標點符號雜訊（如孤立的｛！；）無傷大意。
