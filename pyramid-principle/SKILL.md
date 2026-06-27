---
name: pyramid-principle
description: 用 Barbara Minto 金字塔原理組織任何輸出——結論先行、由上而下、分組 MECE。使用者 要求所有給他的回答/報告/文件都照這套結構。任何產出文字、回答問題、寫報告、做摘要時都套用。
---

# 金字塔原理（Minto Pyramid）輸出結構

使用者 要求：**以後所有輸出都照金字塔原理組織。** 這個 skill 是操作規則。

## 一句話核心

**先講結論，再講理由。** 任何溝通的頂點是「一個主結論」，下面用「分組、有邏輯順序、彼此獨立的支持論點」撐住，每一層都是下一層的總結。

## 四條鐵律

1. **結論先行（answer first）**：開頭就給答案/建議/主張，不要鋪陳到最後才講。讀者先知道結論，再看理由。
2. **由上而下（top-down）**：金字塔頂 = 一個 governing thought；往下展開 key line（2–4 個關鍵論點）；再往下是各自的支持。
3. **同層分組 MECE**：同一組的論點要 **彼此獨立、互不重疊、合起來窮盡**（Mutually Exclusive, Collectively Exhaustive）。沒有遺漏、沒有重複。
4. **每層總結下層**：上一層的每一點，都是它下面那組的摘要；下面那組合起來支持上面那一點。

## 分組的兩種邏輯

- **演繹（deductive）**：大前提 → 小前提 → 結論。用於需要嚴密推理的論證。少用、慎用（鏈太長讀者會累）。
- **歸納（inductive）**：把同類的點並列（「三個理由」「四個步驟」「兩個風險」），給這組一個概括名詞。**多數情況用這個**，配 bullet 最好讀。

## 排序邏輯（同組內怎麼排）

- **時間順序**：步驟一→二→三
- **結構順序**：依空間/組成切（北區/中區/南區；前端/後端/DB）
- **重要性順序**：最重要先講

## 開場用 SCQA（要 framing 時）

- **S 情境(Situation)**：對方already知道的背景
- **C 衝突(Complication)**：打破現狀的變化/問題
- **Q 問題(Question)**：因此產生的疑問
- **A 答案(Answer)**：你的結論（= 金字塔頂）

短回答可略過 SCQA，直接給 A。

## 給 使用者 的實戰模板

```
【結論/建議一句話】

理由（MECE，2–4 點，bullet）：
- 論點 1 — 一句支持
- 論點 2 — 一句支持
- 論點 3 — 一句支持

（需要時）下一步 / 取捨 / 風險
```

## 搭配 使用者 其他偏好

- **分點 bullet 優先**（見 feedback_prefers_bullet_points）：金字塔的 key line 用 bullet 呈現
- **不要 emoji/裝飾性符號**（見 feedback_no_decorative_icons）：乾淨文字
- **結論先行 = 也符合他「結果導向、指令簡潔」**（見 user_communication_style）

## 自我檢查（輸出前問）

1. 第一句是結論嗎？還是還在鋪陳？
2. 支持論點是不是 MECE（沒重疊、沒遺漏）？
3. 每個論點都真的支持上面的結論嗎？
4. 同組的點是同類、有排序嗎？
5. 能不能更短？

## Reference

完整書籍內文已 OCR 萃取，**按需查閱**（日常套用看本檔即可，不必讀全文）：

- 索引：`reference/INDEX.md` — 17 個語意檔名的章節主題與「依任務找章檔」完整對照表
- 全文：`reference/ch00-…` … `ch12-…`、`appendix1-…`～`appendix3-…`、`references-bibliography`（簡體版，每檔標原書頁碼＋檔內 TOC）

最高頻查閱入口（完整對照見 `reference/INDEX.md`）：
- 搭金字塔步驟 → `reference/ch03-building-pyramid.md`
- 寫序言 / SCQA（背景-衝突-疑問-答案） → `reference/ch04-preface-writing.md`、`reference/appendix2-preface-examples.md`
- 同組論點排序（時間/結構/程度） → `reference/ch06-logical-order.md`
- 做書面報告 / PPT → `reference/ch10-written-presentation.md`、`reference/ch11-ppt-presentation.md`
