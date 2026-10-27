# PP 團隊 Google Drive 安裝補充

更新：2026-10-27。這份文件取代 0.1.1 安裝包中關於 SharePoint／OneDrive 的文件儲存步驟。PP 團隊帳號為 `itzpp7744@gmail.com`；尚未確認它是否屬於付費 Google Workspace，不能預設有「共用雲端硬碟」功能。不要在未經授權的情況下登入、讀取或變更此帳號。

## 先釐清各自的位置

- **Google Drive：** 部門共享文件的原稿、已核准文件及待審提案。Google Drive 電腦版把同一共享資料夾呈現在各自電腦，並負責同步。
- **本機私有資料夾：** 每個人、每台電腦自己的草稿及 AI 設定，不自動同步。
- **Neon：** 計畫存共用記憶、待辦與文件索引；現有服務尚未部署。不要把 Neon 當作 Google Drive 的檔案備份。
- **GitHub：** 安裝包、空白範本與程式，不存工作文件與密鑰。

PP 帳號由管理者保管。由管理者確認 Wilson、Avril 各自具備公司允許使用的 Google 帳號，再把指定資料夾分享給兩人。使用各自帳號便於撤權和辨識修改者；不要把 PP 密碼給兩人或他們的 AI。若公司政策不允許使用這個 Gmail 保存公司資料，先讓公司確認替代帳號或文件位置。

## 管理者要做的事

1. 由 PP 帳號本人在 Google Drive 建立專用的「PP 團隊專案」資料夾；若已有合適資料夾，先確認後沿用，不擅自搬動既有檔案。
2. 僅分享給 Wilson、Avril 各自獲公司允許的 Google 帳號，權限依工作需要設定；避免「知道連結的任何人」都能開啟。通知、分享及帳號設定由管理者完成。
3. 若使用者確認有 Google Workspace 且具備共用雲端硬碟，可評估將文件放在團隊持有的共用雲端硬碟；否則先用 PP 帳號「我的雲端硬碟」內的共享資料夾。兩種不是同一種功能：前者以團隊為持有單位，後者仍與擁有者帳號綁定。
4. 將共享資料夾連結、兩人各自的 Google 帳號及共同專案代號交給本人。不在聊天貼密碼、驗證碼或資料庫金鑰。

## Wilson／Avril 各自的電腦

1. 若公司設備允許，從 Google 官方網站安裝 [Google Drive 電腦版](https://support.google.com/drive/answer/10838124?hl=zh-Hant)。Wilson 用 Windows 安裝程式；Avril 用 Mac 安裝程式。已有程式時不用重裝。
2. 由本人登入自己的授權 Google 帳號。從網頁的「與我共用」開啟管理者分享的專案資料夾；需要時在網頁新增捷徑至自己的「我的雲端硬碟」，再於電腦版找到該資料夾。詳見 [Google：尋找與你共用的檔案](https://support.google.com/drive/answer/2375057?hl=zh-Hant)。
3. 在檔案總管或 Finder 開啟已同步的目標資料夾，確認實際路徑及所用帳號；Windows 和 Mac 路徑不會相同。不要自行建立一個普通空資料夾冒充共享資料夾。
4. 從 ZIP 解壓的 `department-agent-kit` 目錄，按原 `START_HERE.md` 執行 `plan`、`install`、`doctor`，但 `--shared-root` 填上剛確認的 Google Drive 本機路徑。`--private-root` 則選同步區之外的個人路徑；兩人用同一專案代號。套件內舊有 OneDrive 文字僅是舊版提示，不能證明同步來源。
5. 執行包內的雙向 `probe-create`／`probe-verify`；依 Google Drive 電腦版顯示的同步狀態等待，並由本人轉交識別碼與指紋。兩個方向都通過，才算實際檔案交換有證據。
6. Avril 的備用電腦重新執行上述步驟，沿用 `Avril` 和相同專案代號，但使用自己該台電腦的路徑；私有設定與草稿不要直接複製。

安裝器有拒絕符號連結／Windows junction 的防護。Google Drive 在特定系統或設定呈現的路徑可能不被接受；若 `plan` 拒絕，保留錯誤並停止，不要關掉安全檢查、改用假共享路徑或自行宣稱完成。本版未在兩人的真實電腦或 Google Drive 環境實測。

## 文件與 AI 的限制

- 本機 Claude Code 可以在本人授權下讀取實際同步且可讀的檔案，例如 Markdown 或下載到電腦的文件；Google 文件／試算表／簡報在電腦版可能只是開啟網頁的項目，不能假設 AI 讀到完整內容。需要文件連接工具，或由本人匯出為適合的檔案後再處理。
- Google Drive 雲端 AI 文件搜尋、讀取、索引與授權**尚未實作或驗收**。0.1.1 的文件連接程式只支援 Microsoft Graph／SharePoint，不能讀 Google Drive。不要依舊版文件填 Google Drive ID 到 Microsoft 的欄位，也不要宣稱手機 Claude 已可讀取 Google 文件。
- 0.1.1 的遠端記憶服務仍使用 Microsoft Entra 身分登入；文件改用 Google 不會自動改掉這項設定。部署之前須確認兩人公司帳號、服務網址與管理員授權；現階段 Neon／MCP 尚未部署。
- 桌面同步不等於本機草稿同步、聊天記錄同步、共用記憶寫回或完整備份。同步衝突與誤刪可能影響共用資料；同一份非 Google 原生文件應錯開編輯，出現衝突時人工比對處理。Google 文件使用瀏覽器內建共同編輯及版本紀錄。
- 簡報需求範本已提供，但本包未實作 Google Slides 自動產生功能。Gmail 也未自動連接。

## 官方案例文件

- [Google Drive 電腦版安裝與同步](https://support.google.com/drive/answer/10838124?hl=zh-Hant)
- [尋找及新增與你共用檔案的捷徑](https://support.google.com/drive/answer/2375057?hl=zh-Hant)
