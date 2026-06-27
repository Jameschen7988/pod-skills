---
name: wiring-check
description: 新增或修改任何機制、文件、規則、hook、skill、agent 後，驗證它真的被啟動流程或觸發器讀到/執行，且指向它的摘要不是 stale。當完成一個「會被別處引用或自動觸發」的產出時使用。觸發詞：「接好了嗎」「會被讀到嗎」「有沒有真的生效」「檢查有沒有接線」「這個會自動跑嗎」。
---

# Wiring Check — 整合驗證

## 為什麼存在

使用者 的工作區反覆出現同一個失敗模式：**機制/文件寫好了，但沒接進啟動流程或觸發器 → 變孤兒（沒人讀/沒人跑）或 stale（被指向但內容過時）**。

實例（都真的發生過）：PRD/memory 與實際 code 脫節、`activity_flush.sh` 寫好卻沒註冊進 settings.json、演化 hook 一開始沒進 Stop 鏈、`memory-layers.md` 沒進 agent 啟動流程、迴路一 feedback.md「強制」只寫規則無 enforcement。

寫完不等於生效。這個 skill 強制做「最後一哩」驗證。

## 何時使用

- 新增/改了：hook、skill、agent 定義、rule、shared 文件、自動化腳本、config
- 任何「預期會被別處引用、或預期會自動觸發」的產出
- 接手別人說「已經做好了」的機制，要確認它真在跑

## 檢查清單

對每個新產出，問四題，逐一拿證據（grep / ls / 實際觸發），不要憑印象：

1. **被讀到嗎？（reference path）**
   - 誰會讀它？`grep -rl "<檔名/機制名>"` 找引用點
   - 若它該被「啟動流程 / 必讀清單 / 索引」收錄 → 確認那些檔真的列了它
   - 孤兒 = 沒人引用 → 補進該引用它的地方

2. **被觸發嗎？（trigger path）**
   - 若是 hook/腳本/自動化 → 它註冊在哪？（settings.json hooks、launchd plist、cron、routine）
   - 用最小輸入實測一次它真的會跑（mock stdin、dry-run）
   - 寫了但沒註冊 = 孤兒

3. **指向它的摘要 stale 嗎？**
   - 任何「摘要 / 目錄 / 數字（如『五層』）/ 狀態（如『待 Dev 評估』）」指向這個機制的地方
   - 內容變了 → 把所有指向它的摘要一起更新，否則讀者看到舊版就不會深入

4. **enforcement vs 期望？**
   - 規則若只寫「必須 / 強制」但沒有 hook/檢查在背後執行 → 它會被忽略（參考死掉的 feedback.md 迴路一）
   - 需要真的發生的事 → 接 hook/排程，不要只寫在文件裡

## 輸出

一張小表：每個產出 × 四題的證據與結論（✅接好 / ❌孤兒 / ⚠️stale），以及補了哪些接線。沒問題也明講「四題皆過」。

## 與其他 skill 的關係

- 這是 `capture-skill` 提煉出來的（2026-06-24）
- 屬記憶體系第 6 層「演化層」的品質守則之一（見 `shared/memory-layers.md`、`shared/style-guide.md`）
