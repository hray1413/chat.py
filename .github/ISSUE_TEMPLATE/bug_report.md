````markdown
---
name: 🐛 Bug 報告 (Bug Report)
about: 報告 Bot 運行中出現的非預期錯誤或故障。
title: '[BUG] 簡潔描述錯誤：例如 Webhook 轉發失敗'
labels: bug
assignees: ''
---

感謝您報告此問題！請盡可能提供詳細的資訊，以便我們重現並修復這個錯誤。

## 💥 問題描述 (The Bug)

請清楚描述 Bot 運行時發生的錯誤或非預期行為。

## 🔄 重現步驟 (To Reproduce)

請提供重現此 Bug 的**完整步驟**。這對於我們理解問題發生的原因至關重要。

1. **環境設定：** 您的 Bot 正在哪個 Discord 伺服器上運行？（例如：伺服器 A 和伺服器 B 之間橋接）
2. **操作步驟：** 在哪個頻道 (Source Channel) 執行了什麼操作？（例如：在 A 伺服器頻道 #chat 發送了一條帶有圖片的消息）
3. **預期結果：** 您預計會發生什麼？（例如：消息應該成功轉發到所有其他橋接頻道）
4. **實際結果：** 實際發生了什麼？（例如：消息沒有轉發，或者轉發了但沒有頭像/附件）

## 📢 錯誤訊息或日誌 (Error Message or Log)

請貼上任何相關的錯誤日誌、堆棧追蹤 (Stack Trace) 或控制台輸出。

<details>
<summary>點擊展開貼上日誌</summary>

```log
# 將您的錯誤訊息貼在這裡
````

\</details\>

## 📋 環境資訊 (Environment)

請提供您的運行環境資訊：

  * **Python 版本：** (例如: `Python 3.10.12`)
  * **discord.py 版本：** (例如: `discord.py 2.3.2`)
  * **Bot 使用的 Cog 版本：** (例如: `chat.py v1.0` 或提交該 Bug 的 `commit hash`)
  * **作業系統：** (例如: `Linux/Ubuntu 22.04` 或 `Windows 11`)

## 💡 額外資訊 (Additional Context)

是否有任何您認為相關的額外資訊？例如：

  * 只有特定類型的消息會觸發此錯誤 (例如：只有回覆訊息會失敗)。
  * 錯誤只在 Bot 運行一段時間後才發生。
  * Bot 在目標頻道中擁有的 Webhook 權限是否完整？

<!-- end list -->

```

---

這個模版將確保您每次收到 Bug 報告時，都擁有足夠的上下文和技術細節來進行高效的除錯。
```
