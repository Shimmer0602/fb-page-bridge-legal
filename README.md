# F.B Page Bridge — GitHub Pages 法律資訊網站

此套件是一個**完全獨立的靜態網站**，只包含 HTML 與 CSS，不需要 Next.js、Vercel、網域 DNS 或任何 Facebook Token。

## 保護原網站

- 原專案：`Shimmer0602/Swin-Forward` —— **不修改**。
- 新專案（請自行建立）：`Shimmer0602/fb-page-bridge-legal` —— Public。
- 不使用 `swim-forward.com` 自訂網域，不修改 Cloudflare 或 Vercel。
- 本套件截至交付時**尚未建立 GitHub 儲存庫、尚未上線**。

## 新儲存庫的預期檔案

將這個 ZIP 解壓縮，並把下列檔案**放在新 Repository 根目錄**（不要再包一層子資料夾）：

```
index.html
privacy.html
terms.html
data-deletion.html
style.css
.nojekyll
README.md
```

## GitHub 網頁介面部署方式

1. 開啟 <https://github.com/new>。Owner 選 `Shimmer0602`，Repository name 填 `fb-page-bridge-legal`，Visibility 選 **Public**，初始化 README 可選擇關閉（以便一次上傳本套件）。建立後確認 URL 是 `https://github.com/Shimmer0602/fb-page-bridge-legal`。
2. 在新儲存庫 Code 頁面選 **Add file → Upload files**。解壓 ZIP，把檔案逐一拖進根目錄，Commit 到 `main`。
3. 進入新儲存庫的 **Settings → Pages**，在 Build and deployment → Source 選 **Deploy from a branch**；Branch 選 `main`，Folder 選 `/(root)`，按 **Save**。
4. 在 GitHub Pages 顯示網站 URL 後，用無痕／登出瀏覽器逐一打開下列網址，確認能看到完整內容，非 404／登入頁，且導覽連結正常。
5. **確認網址已經真的能開啟**之後，再到 Meta App (`F.B Page Bridge`，App ID `1514619050494702`) 的 Settings → Basic 填入三個 URL。再次檢查實際 Dashboard 的 Required actions，再決定是否發佈 App；不要預設 GitHub Pages 部署就等於 Meta App 已上線。

## 預期網址（建立並啟用 GitHub Pages 後才存在）

- 首頁：<https://shimmer0602.github.io/fb-page-bridge-legal/>
- 隱私權政策：<https://shimmer0602.github.io/fb-page-bridge-legal/privacy.html>
- 服務條款：<https://shimmer0602.github.io/fb-page-bridge-legal/terms.html>
- 用戶資料刪除說明：<https://shimmer0602.github.io/fb-page-bridge-legal/data-deletion.html>

## 公開發佈前人工核對

- 維護者姓名：`Rone Tseng`；個人維護、沒有公司登記。與目前事實一致。
- 聯絡方式：`shimmer0602@gmail.com` 將**公開顯示在所有法律頁面**，請確認願意公開或先替換為專用信箱。
- Data flow：Bridge 在受存取控制的託管環境內保存必要的 SQLite 紀錄／草稿；OAuth 授權憑證由憑證管理服務保管；實際功能或服務提供者若有變更，應同步更新隱私政策。
- App IDs／兩個管理粉專名稱／授權範圍是否仍符合現況。
- 法律聲明是依提供的 2026-11-09 原始文件修訂，不構成律師審核或 Meta 核准。

## Meta 欄位

| Meta Developer App Settings → Basic | 內容（在網站驗證成功後貼上） |
| --- | --- |
| Privacy Policy URL | `https://shimmer0602.github.io/fb-page-bridge-legal/privacy.html` |
| Terms of Service URL | `https://shimmer0602.github.io/fb-page-bridge-legal/terms.html` |
| User Data Deletion Instructions URL | `https://shimmer0602.github.io/fb-page-bridge-legal/data-deletion.html` |

選擇「資料刪除說明網址」方式時，Meta 是否顯示相同選項依當下 Dashboard 為準。App Domains 與 OAuth redirect URI 不要因為設立獨立法律網站而任意更動。

## 注意

本專案只有靜態文件，沒有登入／JavaScript／追蹤器／API 請求，也不包含任何 Token、Secret、SQLite 資料庫或圖片。GitHub Pages 一旦啟用，內容對任何人公開。