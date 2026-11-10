# F.B Page Bridge — GitHub Pages 法律資訊網站

此套件是一個**完全獨立的靜態網站**，只包含 HTML 與 CSS，不需要 Next.js、Vercel、網域 DNS 或任何 Facebook Token。

## 本儲存庫用途

- 此為 **F.B Page Bridge** 專用的公開法律資訊網站，與其他產品及儲存庫無關。
- 儲存庫：`Shimmer0602/fb-page-bridge-legal`（Public）。
- 使用 GitHub Pages 靜態託管，不需要自訂網域或變更其他服務設定。
- 網站檔案已上傳至 `Main` 分支；GitHub Pages 仍須在儲存庫 Settings → Pages 啟用並核對公開網址。

## 新儲存庫的預期檔案

目前儲存庫根目錄已包含：

```
index.html
privacy.html
terms.html
data-deletion.html
style.css
.nojekyll
README.md
```

## GitHub Pages 啟用方式（程式碼已上傳）

1. 開啟 <https://github.com/Shimmer0602/fb-page-bridge-legal/settings/pages>。
2. 在 **Build and deployment → Source** 選擇 **Deploy from a branch**。
3. 在 **Branch** 選擇 **Main**（大小寫以實際儲存庫為準），資料夾選 **/(root)**，按 **Save**。
4. 等 GitHub Pages 頁面顯示公開網站網址，再以未登入／無痕瀏覽器逐一測試首頁及三個法律網址，確保頁面可見且無 404。
5. 驗證成功後，才把法律頁面網址填入 Meta App Settings → Basic。這些設定僅適用於此獨立法律網站。

## 預期網址（啟用 GitHub Pages 後才可公開存取）

- 首頁：<https://shimmer0602.github.io/fb-page-bridge-legal/>
- 隱私權政策：<https://shimmer0602.github.io/fb-page-bridge-legal/privacy.html>
- 服務條款：<https://shimmer0602.github.io/fb-page-bridge-legal/terms.html>
- 用戶資料刪除說明：<https://shimmer0602.github.io/fb-page-bridge-legal/data-deletion.html>

## 公開發佈前人工核對

- 維護者姓名：`Rone Tseng`；個人維護、沒有公司登記。與目前事實一致。
- 聯絡方式：`shimmer0602@gmail.com` 將**公開顯示在所有法律頁面**，請確認願意公開或先替換為專用信箱。
- Data flow：Bridge 在受存取控制的託管環境內保存必要的 SQLite 紀錄／草稿；OAuth 授權憑證由憑證管理服務保管；實際功能或服務提供者若有變更，應同步更新隱私政策。
- App ID、授權粉專的操作權限與允許清單是否仍符合實際使用情況。
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