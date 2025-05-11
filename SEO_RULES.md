# 星啟點國際娛樂網站 SEO 通用規則

## 1. 基本 Meta 標籤
- `<title>`：每頁唯一且具描述性
- `<meta name="description">`：每頁唯一，簡明描述頁面內容，建議 120-160 字
- `<meta name="viewport" content="width=device-width, initial-scale=1">`：響應式設計必備
- `<meta name="robots" content="index, follow">`：允許搜尋引擎索引
- `<meta name="author" content="星啟點國際娛樂">`：標註作者

## 2. Open Graph（og）標籤（社群分享）
- `<meta property="og:title">`：分享標題
- `<meta property="og:description">`：分享描述
- `<meta property="og:image">`：分享圖片（建議1200x630px，jpg/png/webp）
- `<meta property="og:url">`：頁面網址
- `<meta property="og:type" content="website">`：網站類型
- `<meta property="og:site_name">`：網站名稱

## 3. Twitter Card 標籤
- `<meta name="twitter:card" content="summary_large_image">`
- `<meta name="twitter:title">`
- `<meta name="twitter:description">`
- `<meta name="twitter:image">`

## 4. Canonical 標籤
- `<link rel="canonical" href="https://你的網站/">`：避免重複內容

## 5. 結構化資料（schema.org）
- 使用 Organization 與 Website 型別，標註 name、url、logo、sameAs（社群連結）、contactPoint（聯絡資訊）
- 範例：
```json
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "url": "https://你的網站/",
  "name": "星啟點國際娛樂",
  "publisher": {
    "@type": "Organization",
    "name": "星啟點國際娛樂",
    "logo": {
      "@type": "ImageObject",
      "url": "https://你的網站/logo.png"
    }
  }
}
```

## 6. Logo 顯示於 Google 搜尋結果
- logo 圖片需公開、正方形（建議112x112px以上）、透明背景
- 於 Google Search Console 設定品牌標誌
- 結構化資料需正確標註 logo

## 7. robots.txt
- 允許 Googlebot 抓取：
```
User-agent: *
Allow: /
```

## 8. sitemap.xml
- 於網站根目錄提供 sitemap.xml，並提交至 Google Search Console

## 9. 其他建議
- 圖片加上 lazyload、alt 屬性
- 內容定期更新，保持高品質
- 網站速度優化（壓縮圖片、精簡 JS/CSS）
- 行動裝置友善設計

## 10. 結構化資料同步維護
網站內容（如職缺、FAQ、公司資訊、評分等）有任何變動時，必須同步更新對應的結構化資料（schema.org JSON-LD），確保內容與結構化資料一致。
例如：
新增、刪除或修改職缺時，JobPosting 結構化資料也要同步調整。
FAQ 問答有異動時，FAQPage 結構化資料也要同步更新。
公司名稱、logo、評分等資訊有變動時，Organization、Logo、AggregateRating 等欄位也要同步更新。
網站結構或重要頁面有調整時，請檢查 canonical、sitemap、結構化資料是否需要同步調整。
這樣可確保 Google 與其他搜尋引擎抓到的資訊永遠是最新、最正確的，有助於 SEO 與豐富結果展現。

---
如需範例程式碼或進階設定，請參考官方文件或聯絡網站維護人員。 


🙅‍♂️不建議
- `<meta name="keywords">` 標籤對現代 SEO 幾乎沒有幫助，Google 已不再參考 meta keywords，建議不必特別設定。
