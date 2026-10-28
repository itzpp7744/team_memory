# PP 團隊共用記憶與 AI 安裝包

版本 **0.3.0**，2026-10-28。請從 [START_HERE.md](START_HERE.md) 開始，新成員也使用同一份入口。

**Neon 共用記憶已上線。** 已用同一位測試成員完成：Claude Code 寫入 → 網頁 Claude 讀到同一筆 → 網頁更新為版本 2 → Claude Code 讀回版本 2。Google 登入、重送不重複新增、錯誤版本拒絕覆寫也已驗證。

成員先連記憶，再設定 Google Drive 與 Obsidian。每人須由管理者核准自己的 Google 帳號，並在自己的 Claude 與 Claude Code 完成登入；拿到 ZIP 不會自動取得資料權限。

| 位置 | 放什麼 |
| --- | --- |
| Neon | 經同意共享的筆記、決策、交接、待辦與操作紀錄 |
| Google Drive | 團隊文件、附件、提案與交付物 |
| GitHub | 安裝包、規則、6 個 Skills、程式與空白範本 |
| 本機私有工作區 | 個人草稿、暫存與這台電腦的路徑設定 |

下載 [0.3.0 安裝包](department-agent-kit-v0.3.0.zip)，配合 [檔案指紋](SHA256SUMS) 與 [發布紀錄](manifest.json) 使用。完整原始碼、測試、管理文件都在 ZIP 內；舊版 ZIP 保留供回溯，新安裝請選 0.3.0。本 repo 以 ZIP 發布，包內 GitHub Actions 尚未展開啟用。

6 個 Skills 涵蓋開工接續、記憶交接、PM 文件、同步檢查、Obsidian 上手及團隊改進。安裝 AI 先問新人的姓名，不限定 Wilson、Avril。全員使用相同資料夾分類與 `pp-memory/2` 記憶格式，本機磁碟路徑可以不同。

這次驗證包含建置通過、28 項共用記憶服務測試及 57 項安裝／草稿測試；不代表每位成員裝置都已驗收。手機 Claude、Windows 實機、Drive 雙向同步與各裝置 Obsidian 仍須逐一確認。

管理者已建立 [PP 團隊專案](https://drive.google.com/drive/folders/1_OrdKAQBzqSQt9EIaKza9SwzA4GvZ2-J)，分享權限尚待逐人設定。文件操作使用 Drive 電腦版；這版沒有另接 Google Docs／Slides 全文 API。共用記憶不會自動同步私人聊天，也不會自動上傳整個資料夾。

目前維持免費方案，未升級、未啟用付費 AI Gateway。免費額度與服務可用性仍受平台限制，不能保證永久免費或全天無中斷。Google 登入目前為測試模式，新人需先加入核准名單與 Google 測試使用者。

同時使用私人記憶時，請依入口的分流規則：私人對話關閉 PP 工具，PP 寫入前核對目的地、可見者與摘要。不以「與工作有關」直接判定可分享，服務的成員權限也不等於內容分類器。
