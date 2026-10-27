# Wilson／Avril 部門 AI 安裝包

> **2026-10-27 更新：PP 團隊先用 Google Drive。** 安裝前先讀 [Google Drive 安裝補充](GOOGLE_DRIVE_SETUP.md)，其共享文件步驟優先於本頁及 ZIP 內的 SharePoint／OneDrive 說明。現有雲端文件連接僅支援 Microsoft，尚未接上 Google Drive。

版本 **0.1.1**，交付日期 **2026-10-27**。完整程式、設定範本、測試與操作說明都在 [安裝包 ZIP](department-agent-kit-v0.1.1.zip) 裡。

請把這個 repo 網址交給電腦上有檔案操作能力的 AI，例如 Claude Code，請它從 [START_HERE.md](START_HERE.md) 開始。只有手機聊天功能的 AI 無法替電腦安裝。

可直接貼給安裝 AI：

> 請讀取這個 repo 的 START_HERE.md，核對安裝包後解壓，依裡面的安裝流程協助我設定。Wilson 使用 Windows；Avril 使用 Mac，其他電腦沿用 Avril 身分。請先確認我的成員名稱與專案路徑，再預覽、安裝、檢查。不要覆寫現有私人設定、存取個人資料庫或把尚未部署的服務回報成已連線。

## 這一版能做什麼

- 本機安裝：建立私有草稿區、共享文件分類與 AI 工作規則，保留既有個人設定。
- 文件同步：使用 Google Drive 電腦版同步選定資料夾，附兩人互傳測試檔的驗收工具。
- 共用記憶與待辦：提供 Neon 服務程式與公司 Microsoft 登入設定，須由管理者部署。
- PM 文件：需求、會議與簡報需求範本。簡報範本不是自動產生 PPTX 的完整服務。

## 資料放哪裡

| 位置 | 負責什麼 |
| --- | --- |
| GitHub | 安裝包、程式與空白範本；不放公司工作文件或金鑰。 |
| 本機私有區 | 個人的草稿、暫存與這台電腦的設定；不會自動同步給同事或其他電腦。 |
| Google Drive | 兩人要交換的文件原稿與修改提案；Google Drive 電腦版將指定共享資料夾呈現在各自電腦。 |
| Neon | 共用記憶、正式待辦、文件索引與操作紀錄；不存另一份文件原稿。 |

部門 Gmail 可保留作聯絡用途；本包不會自動連接 Gmail。檔案同步先採 Google Drive，設定見上方 Google Drive 安裝補充。各人可用自己的 Claude，但讀取公司資料時仍需自己的公司 Microsoft 帳號授權。兩人共用 Claude 帳密無法提供可靠的個人操作歸屬，不能拿它取代公司身分驗證。

## 已驗證與還沒上線的部分

服務程式基準版通過 **54 項測試、沒有跳過**；0.1.1 僅更新交付及裝置說明，程式碼未變，另重跑 **24 項本機安裝器測試通過**。ZIP 內容及檔案指紋也已核對。

**公司雲端服務尚未部署。** 真實 Neon、公司登入、Google Drive 權限、Windows 實機及兩人跨電腦同步仍須驗收。這個 repo 採完整原始碼 ZIP 交付，包內的 GitHub Actions（自動測試設定）尚未解壓到 repo 根目錄，因此不會自動執行；未宣稱遠端 CI 已通過。

解壓後，管理者讀 `department-agent-kit/docs/ADMIN_SETUP.md`；兩人及管理者共同使用 `docs/ACCEPTANCE.md` 留下驗收紀錄。完整限制在 `docs/KNOWN_LIMITATIONS.md`。
