# FHIR.tw 短網址服務（本專案 Fork 自 [SITCON 短網址服務](https://github.com/sitcon-tw/URL-Shortener)）

這個專案使用 GitHub Pages 建立一個簡單的短網址服務，開放自訂標題、摘要和 Open Graph 標籤。

## 如何建立新的短網址

1. 在 `_redirects` 資料夾中建立一個新的 Markdown 檔案。檔名將成為短網址的一部分（slug）。
   例如：`template.md` 將產生 `https://go.fhir.tw/template`

2. 在 Markdown 檔案中使用以下格式：

   ```yaml
   ---
   layout: redirect
   title: "您的自定義標題"
   description: "您的自定義描述"
   image: "/images/your-image.jpg"  # 使用相對路徑引用 repo 中的圖片
   # 或
   image: "https://example.com/your-image.jpg"  # 使用完整的 URL
   redirect_to: "https://example.com/your-long-url"
   ---
   ```

   注意：
   - 如果圖片存放在本專案的 `images` 資料夾中，請使用相對路徑（例如：`/images/your-image.jpg`）。
   - 如果要使用外部圖片，請提供完整的 URL。

3. 如果你想使用自訂圖片，請將圖片檔案上傳到 `images` 資料夾。

4. 將變更提交並推送到 GitHub 儲存庫，或是發 PR 過來讓我們合併。

5. GitHub Actions 將自動建置並部署您的新短網址。

## 關於 FHIR.tw

台灣 FHIR 公共網域（FHIR.tw） 是一個網域名稱註冊服務，我們為學生、研究人員、開源專案或非營利社群提供免費的二級網域名稱服務（如 myblog.fhir.tw）。這項服務主要提供給與 FHIR 標準或醫學資訊相關的專案，您可以將這個網域名稱用於教學網站、部落格、FHIR 開源專案、公開服務等內容。

我們希望透過這項服務來促進醫資標準的交流，並藉此提供一個平台讓大家易於尋找 FHIR 與醫學資訊相關的資源，以降低 FHIR 及相關規範在台灣的應用門檻。

請造訪 [FHIR.tw](https://fhir.tw) 官方網站以了解更多