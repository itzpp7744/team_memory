# PP 團隊唯一安裝入口

目前版本 **0.2.1**。本 repo 是私人儲存庫，需先取得管理者授權並以自己的 GitHub 存取方式開啟；不要把登入憑證貼進聊天。

## 給安裝 AI

1. 下載同一版本的 [安裝包](department-agent-kit-v0.2.1.zip)、[SHA256SUMS](SHA256SUMS) 與 [manifest.json](manifest.json)。不要選舊版 0.1.1。
2. 比對 ZIP 的 SHA-256（檔案指紋，用來確認下載內容沒有變）。macOS 用 `shasum -a 256 department-agent-kit-v0.2.1.zip`；Windows PowerShell 用 `Get-FileHash .\department-agent-kit-v0.2.1.zip -Algorithm SHA256`。結果須與 SHA256SUMS 完全一致。
3. 檢查 ZIP 項目都在 `department-agent-kit-0.2.1/` 下，沒有絕對路徑、`..` 或符號連結，再解壓到專用新資料夾。不要覆寫現有專案，不要把套件放進 Google Drive 共享專案。
4. 進入解壓後的 `department-agent-kit-0.2.1`，完整讀取該目錄的 `START_HERE.md`，依它執行。套件保留在原位置，後續檢查仍會使用。
5. 沿用已知資訊，只補問缺少的：本人姓名／唯一團隊稱呼、共同專案代號、私有工作區路徑、實際 Google Drive 共享路徑。Avril 所有電腦都用 Avril 身分。
6. 依序預覽、安裝、檢查；在私有工作區確認 6 個 Skills、建立並驗證記憶草稿，再由兩人做真實雙向文件驗收。

PP Gmail 是 `itzpp7744@gmail.com`；這只是團隊帳號識別，不表示已授權登入。Google Drive 詳見包內設定指南；本頁的 [Google Drive 摘要](GOOGLE_DRIVE_SETUP.md) 供管理者先準備。

## 界線

- 不覆寫個人規則、不改全域 Skills、不連私人資料庫，不掃描私人聊天。
- 本機草稿成功要說「已存本機、未送出」。管理者尚未提供及部署正式服務時，不自行找 Neon 密碼，不宣稱手機 Claude 已接通。
- Google Drive 同步文件；Neon 未接通前沒有正式共用記憶。共同資料夾的檔案檢查不能取代兩台實機驗收。
- 網頁／手機 AI 若不能操作本機，請將這份入口交給電腦上的 Claude Code；無法存取私人 repo 時，由有權限者下載上述檔案交給本機 AI。

最後回報：成員、專案、版本、實際路徑、6 個 Skills、草稿檢查、雙向同步及雲端狀態。未驗證的項目要分開列出。

安裝後請繼續套件內的 pp-onboarding：先查 Obsidian 是否已安裝、保留私人 Vault，再打開正確團隊資料夾；完成閱讀／修改／同步練習。要提出新功能或分享自己做的技能，使用 pp-team-improvement，經審閱後更新發布。

管理者已建立 [PP 團隊專案](https://drive.google.com/drive/folders/1_OrdKAQBzqSQt9EIaKza9SwzA4GvZ2-J)，交付時尚未分享給兩人；先確認權限。新人可直接沿用同一包，安裝 AI 先問姓名，再建立自己的工作區及修改提案區。管理者另授予共享權限。
