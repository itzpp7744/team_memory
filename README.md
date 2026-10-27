# PP 團隊 AI 安裝包

目前版本 **0.2.1**，2026-10-27。Wilson（Windows）與 Avril（Mac／備用 Windows）共用這一份安裝流程。

**從 [START_HERE.md](START_HERE.md) 開始。** 請交給有本機檔案與終端機能力的 AI，例如 Claude Code。手機聊天本身不能替電腦安裝。

## 這版交付什麼

- 6 個 PP 專用 Skills：開工接續、記憶交接、PM 文件、同步檢查、Obsidian 上手、團隊改進。
- 兩人一致的共享資料夾分類、團隊規則和文件範本；本機磁碟路徑可以不同。
- `pp-memory/2` 記憶草稿格式與檢查工具，避免兩人各建一套欄位。
- Google Drive 電腦版路徑設定與雙向驗收工具；保留既有個人設定。

| 位置 | 用途 |
| --- | --- |
| GitHub | 安裝包、程式與空白範本 |
| 本機私有區 | 本人草稿、暫存、這台電腦的設定 |
| Google Drive | 兩人分享的文件、修改提案、已核准交付 |
| Neon（部署後） | 正式共用記憶、待辦與操作紀錄；不是另一份文件硬碟 |

PP 團隊 Gmail：`itzpp7744@gmail.com`。管理者分享指定 Drive 資料夾給兩人各自核准的 Google 帳號；套件不登入信箱、不更動分享權限、不要求共用密碼。

## 可用範圍

本機安裝與草稿工具已測試。實際 Windows／Mac、Google Drive 雙向同步、Claude Code Skills 載入仍須依驗收表確認。共享資料夾同步不等於聊天同步，手機 Claude 也不會自動取得本機 Skills。

**Neon 正式服務尚未部署，Google 雲端文件 API／Google 登入尚未實作。** 既有可選記憶服務仍使用 Microsoft 公司登入。不要把安裝完成寫成雲端已接通。Google Docs／Slides 的本機捷徑也不等於可讀取全文。

完整原始碼、測試與管理文件在 [0.2.1 安裝包](department-agent-kit-v0.2.1.zip)。舊 0.1.1／0.2.0 ZIP 僅供留存，新安裝不要使用。此 repo 以 ZIP 交付，包內 GitHub Actions 尚未展開啟用。

安裝後請繼續套件內的 pp-onboarding：先查 Obsidian 是否已安裝、保留私人 Vault，再打開正確團隊資料夾；完成閱讀／修改／同步練習。要提出新功能或分享自己做的技能，使用 pp-team-improvement，經審閱後更新發布。

管理者已建立 [PP 團隊專案](https://drive.google.com/drive/folders/1_OrdKAQBzqSQt9EIaKza9SwzA4GvZ2-J)，交付時尚未分享給兩人；先確認權限。新人可直接沿用同一包，安裝 AI 先問姓名，再建立自己的工作區及修改提案區。管理者另授予共享權限。

驗證：90 項程式測試全通過，沒有跳過；含獨立本機 Postgres 測試，未連現有 Neon。
