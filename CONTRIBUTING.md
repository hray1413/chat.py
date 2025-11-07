# 🤝 貢獻指南 (Contributing Guide)

感謝您對 **CrossChatBridge** 專案的興趣！我們非常歡迎所有形式的貢獻，無論是 Bug 報告、功能建議還是程式碼提交。

請先閱讀我們的 **[policy.md](./policy.md)**，了解行為準則和程式碼標準。

## 💬 如何報告 Bug 或提出建議

在提交程式碼之前，請務必遵循以下步驟：

1.  **檢查現有 Issue：** \* 前往 Issue 檢查您的問題是否已被報告或您的建議是否已被討論過。
2.  **提交 Bug 報告 (Bug Report)：**
      * 請提供清晰的**重現步驟**、預期行為和實際發生的行為。
      * 附上相關的 Bot **日誌錯誤訊息**或堆棧追蹤 (Stack Trace)。
3.  **提交功能請求 (Feature Request)：**
      * 清楚描述您希望新增的功能，以及它將如何解決現有的問題或提升用戶體驗。

## 💻 程式碼貢獻流程

### 1\. 設置您的開發環境

1.  **分叉 (Fork)：** 在 GitHub 上分叉（Fork）本專案的儲存庫。
2.  **克隆 (Clone)：** 將您的分叉版本克隆到本地：
    ```bash
    git clone https://github.com/hray1413/chat.py.git
    cd chat.py
    ```
3.  **建立虛擬環境 (Virtual Environment)：**
    ```bash
    python -m venv venv
    source venv/bin/activate  # macOS/Linux
    .\venv\Scripts\activate   # Windows
    ```
4.  **安裝依賴：** 安裝運行和測試 Bot 所需的所有函式庫。
    ```bash
    pip install discord.py aiohttp
    ```
    
### 2\. 撰寫程式碼

1.  **建立分支：** 始終從 `main` 或 `develop` 分支建立一個新的、描述性的分支：
    ```bash
    git checkout -b feature/新增功能名稱
    # 或
    git checkout -b bugfix/修復錯誤編號
    ```
2.  **遵循程式碼標準：**
      * 請務必遵守 **[policy.md](./policy.md)** 中列出的 **PEP 8 風格指南**、4 個空格縮排和類型提示慣例。
      * **運行測試：** 如果專案包含測試套件（例如使用 `pytest`），請確保您的變更通過所有現有測試，並為您的新功能/修復編寫新的單元測試。

### 3\. 提交 (Commit) 規範

我們鼓勵清晰、簡潔的 Git 提交訊息。每次提交都應該描述一個邏輯上的單一變更。

  * **格式：** 使用簡潔的主旨行（50 個字符以內），並可選地加上一個詳盡的內文。
    ```
    fix: 修復 Webhook 轉發時未處理附件 URL 的問題

    此修復確保在 message.content 為空時，附件 URL 仍能被正確地添加到轉發內容中。
    連結到相關 Issue: #123
    ```
  * **推薦前綴 (Prefixes)：**
      * `feat:` (新功能)
      * `fix:` (Bug 修復)
      * `docs:` (文件變更，例如 README 或 https://www.google.com/search?q=policy.md)
      * `refactor:` (重構，不改變功能)
      * `chore:` (雜項任務，例如更新依賴)

### 4\. 提交拉取請求 (Pull Request, PR)

1.  **同步分支：** 在提交 PR 之前，請確保您的分支與主儲存庫保持同步。
    ```bash
    git pull origin main
    ```
2.  **建立 PR：** 將您的分支推送到您的 GitHub 分叉儲存庫，然後在 GitHub 介面中建立一個拉取請求，目標指向本專案的 `main` 或 `develop` 分支。
3.  **描述 PR：** 在 PR 描述中：
      * 連結到任何相關的 Issue 編號（例如 `Closes #123`）。
      * 清楚說明您的變更是什麼，以及為什麼要做此變更。

感謝您的時間和貢獻！我們期待您的 PR！
