# 給接手安裝的 AI

> **2026-10-27 更新：PP 團隊先用 Google Drive。** 安裝前先讀 [Google Drive 安裝補充](GOOGLE_DRIVE_SETUP.md)，其共享文件步驟優先於本頁及 ZIP 內的 SharePoint／OneDrive 說明。現有雲端文件連接僅支援 Microsoft，尚未接上 Google Drive。

這是交付入口，完整安裝流程在 ZIP 裡。先完成以下步驟，再讀包內的 `START_HERE.md`。

1. 從 `https://github.com/itzpp7744/team_memory` 下載或 clone 到使用者選定的新資料夾；該位置須在共享文件區以外。私人 repo 由本人登入取得存取權，不要求把密碼或 token 貼進對話。
2. 讀取本層 `manifest.json` 與 `SHA256SUMS`，核對 `department-agent-kit-v0.1.1.zip` 的 SHA-256（檔案內容的指紋）。不同就停止，不安裝。
3. 檢查 ZIP 項目只在 `department-agent-kit/` 底下，沒有絕對路徑、`..` 或符號連結；目標 `department-agent-kit` 資料夾已存在就停止，不覆寫。
4. 解壓到這個交付資料夾，保留隱藏檔；再讀 `department-agent-kit/START_HERE.md`、`AGENTS.md`、`CLAUDE.md`、`README.md`。
5. 切到 `department-agent-kit`，依 Google Drive 補充文件確認共享路徑，並依包內流程確認本人成員、共同專案代號和私有路徑。執行 `plan`、`install`、`doctor`，再做雙向檔案驗收。有正式服務網址才設定雲端工具。

## 核對與解壓指令

以下從本檔所在資料夾執行。先核對指紋，再確認解壓目標不存在。Python 需要 3.11+。

Windows PowerShell（Wilson；Avril 備用 Windows 也適用）：

```powershell
Get-FileHash .\department-agent-kit-v0.1.1.zip -Algorithm SHA256
Get-Content .\SHA256SUMS
Test-Path .\department-agent-kit
# 只有指紋相同、上述 Test-Path 為 False，且 ZIP 項目檢查通過後才解壓：
py -3 -m zipfile -e .\department-agent-kit-v0.1.1.zip .
```

macOS（Avril）：

```sh
shasum -a 256 -c SHA256SUMS
# 確認目標尚未存在，並完成 ZIP 項目檢查後才解壓：
test ! -e department-agent-kit && python3 -m zipfile -e department-agent-kit-v0.1.1.zip .
```

上述註解是執行前提，不要把整段當成無條件安裝指令。AI 須實際讀取核對結果，不能因解壓成功就略過指紋或路徑檢查。

## 已知裝置與身分

Wilson：Windows。Avril：Mac 為主，另有公司電腦。Avril 每台都使用 `Avril` 成員名稱、同一公司 Microsoft 身分與同一專案代號，各台填自己的路徑；不要搬用另一台的 `.department-agent` 或 `.mcp.json`。

公司身分由 Microsoft 登入驗證；本機 `--member` 只是名稱，不是授權。兩人各自登入自己的公司帳號，不共用 Neon 金鑰。沒有正式服務網址時先完成本機工作，雲端狀態明確保留「尚未設定」。

本包沒有部署到既有 Neon，也沒有修改使用者原本的專案。管理者部署要另依包內 `docs/ADMIN_SETUP.md` 進行。
