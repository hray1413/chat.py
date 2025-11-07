# 🌉 CrossChatBridge (跨群聊天橋接 Bot)

[](https://www.google.com/search?q=LICENSE)
[](https://www.python.org/)
[](https://pypi.org/project/discord.py/)

## 📝 簡介 (About)

`CrossChatBridge` 是一個基於 `discord.py` 框架開發的 Discord Bot 擴展 (Cog)，旨在為多個 Discord 伺服器之間建立一個**無縫、即時的聊天橋樑**。

它利用 Discord 的 **Webhook** 功能，將消息從一個已設定的頻道轉發到所有其他橋接頻道，同時**模擬原始發送者的身份**，讓跨群交流如同在單一群組內一樣自然。

## ✨ 主要特色

  * **身份保留：** 透過 Webhook 轉發，消息顯示為原始用戶的名稱和頭像，而非 Bot 本身。
  * **回覆支援：** 智慧處理並模擬回覆訊息，保留對話上下文。
  * **附件處理：** 自動將附件 URL 附加到轉發內容中。
  * **持久化配置：** 橋接設定會儲存在 `bridge_webhooks.json` 檔案中，Bot 重啟後無需重新設定。
  * **斜線指令 (Slash Commands)：** 方便管理員設定和移除橋樑。

## 🚀 快速開始 (Quick Start)

### 1\. 安裝與設定

1.  **環境準備：** 確保您已安裝 Python 3.10+ 和 `discord.py` 2.0+ 版本。

2.  **檔案放置：** 將 `chat.py` 檔案放置在 Bot 的 `cogs` 或擴展目錄中。

3.  **Bot 核心載入：** 在您的 Bot 主檔案中載入此 Cog：

    ```python
    # 在您的 bot.py (或其他主檔案) 中
    async def setup_hook():
        await bot.load_extension("cogs.chat") # 假設 chat.py 位於 cogs 資料夾

    # bot.setup_hook = setup_hook # 如果您的主檔案使用 setup_hook
    ```

### 2\. Discord 權限要求

為了讓 Bot 能夠建立和發送 Webhook，請確保 Bot 在您希望設定橋樑的伺服器中擁有以下權限：

  * `manage_channels` (管理頻道)
  * `manage_webhooks` (管理 Webhook)
  * `read_messages` (讀取訊息)
  * `send_messages` (傳送訊息)

### 3\. 設定橋樑 (指令)

管理員可以在希望建立橋樑的頻道中使用以下斜線指令：

| 指令 | 說明 | 權限要求 |
| :--- | :--- | :--- |
| `/setbridge` | 在當前頻道建立一個 Webhook，並將此頻道添加到跨群橋樑中。 | `manage_channels` |
| `/removebridge`| 移除當前頻道的橋樑設定，並嘗試刪除相關 Webhook。 | `manage_channels` |

## ⚙️ 貢獻與政策

我們歡迎社群對 `CrossChatBridge` 做出貢獻！

  * **貢獻指南：** 請查閱 [CONTRIBUTING.md] (如果您有此檔案) 和 **https://www.google.com/search?q=policy.md**，了解程式碼標準和提交流程。
  * **程式碼政策：** 詳細的行為準則、貢獻規範和治理結構，請參閱：[policy.md](https://www.google.com/search?q=policy.md)

## ⚖️ 授權 (License)

本專案根據 **MIT 授權** 條款發布。詳情請參閱 `LICENSE` 檔案。

```
Copyright (c) 2025 hray1413
```
