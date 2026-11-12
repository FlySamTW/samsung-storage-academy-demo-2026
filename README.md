# 儲存實戰學院 | Storage Field Lab 2026

**台灣三星儲存設備產品公開資料教育訓練示範**。這是一個獨立設計、可免費部署的靜態教學網站，**非 Samsung 官方核可網站**，未完成 Samsung Brand VI 審核。

## 線上示範

預期 GitHub Pages：`https://flysamtw.github.io/samsung-storage-academy-demo-2026/` （須經實際部署驗收才算可用）

## 本次選品（2025–2026）

| 類型 | 產品 | 完整代表型號／容量 |
| --- | --- | --- |
| 內接 SSD | 9100 PRO PCIe 5.0 | MZ-VAP1T0CW · 1TB 含散熱片 |
| 內接 SSD | 2026 990 SSD PCIe 4.0 | MZ-V9V1T0BW · 1TB |
| 外接 USB4 SSD | P9 | MU-PJ1T0G/WW · 1TB |
| 外接 USB4 SSD | P7 | MU-PF1T0G/WW · 1TB |
| microSDXC | T9 | MB-MH256T/WW · 256GB |
| microSDXC | T7 | MB-MB256T/WW · 256GB |

選品旨在示範官方近期不同儲存類型的教學深度，**不宣稱銷售排行榜名次**。

資料來源以 `products.json` 中每款的 `official`、`priceSource` 為準。產品圖原始網址與 SHA256 在 `assets/sources.json`；圖片來自 Samsung 台灣正式商品頁，版權仍屬原權利人。未經授權，不應以此資料庫取代公司官方素材供商業發佈。

## 完整功能

- 6 組顧客需求：實際選擇後立即更新建議產品與其他可比較選項。
- 6 張產品教材卡：真實官方產品圖片、型號、客群、開場提問、3 個正向賣點、現場展示建議、動態完整規格（展開式）、指定容量上市建議售價及公開來源。
- 產品分類（內接／外接／記憶卡）、文字搜尋、空結果提示。
- 3 組同類型選購比較；不將不同介面速度數值直接排名。
- 6 項由這次產品特性形成的知識教室。
- 10 題銷售情境選擇題，即時答案解析、回產品複習、進度條、完成分數與重新作答。
- 全部本機前端執行，不要求登入、不寫入作答或使用者資訊、不需要付費 AI API。
- 360/390/1280/1440 尺寸響應式設計，頁面可列印。

## 完全免費的部署

GitHub Pages（公開 repository）：

1. 建立**新的公開 repository**，並放置本目錄內的 `index.html`、`style.css`、`app.js`、`products.json`、`questions.json`、`.nojekyll`、`assets/`（含來源 JSON、正式 WebP）。
2. Settings → Pages → Build and deployment → Deploy from a branch → Branch: main；資料夾: /(root)。
3. 使用 `https://<username>.github.io/<repository-name>/` 開啟公開網址，實際測試 JSON、圖片與互動功能。
4. GitHub Pages 本身需遵守官方使用條款；本站不接購物、交易、訂閱或收取個資。

另一種可行選擇：Cloudflare Pages Free 的靜態上傳。但此版**沒有使用 Cloudflare 或付費服務**。

## 檔案與維護

- `products.json`：選品、客群、官方規格、賣點、情境與來源。更新選品時保留正式 SKU，一律核實來源。
- `questions.json`：10 題有明確答案的正向銷售題，不考沒有實務價值的規格背誦。
- `app.js`：需求推薦、卡片渲染、比較、篩選與測驗互動引擎。
- `style.css`：版型、主題色、手機及大畫面。
- `assets/*.webp`：官方產品原圖（經尺寸縮放與 WebP 壓縮，不重畫）。
- `assets/sources.json`：產品照原始官方頁面、下載圖片 URL 及檔案雜湊。
- `qa_site.py`：僅在本機進行 Chrome 真實操作測試，透過暫時 HTTP server 跑四種尺寸，正式 repo 不需上傳此檔。
- `qa/`：調查用圖片、QA 報告、手機及桌面截圖（不公開至 GitHub Pages）。

調整 JSON、JS 或 CSS 後重新執行本機 QA，發布完成後再次從**公開** HTTPS 網址核對，不得以本機 PASS 冒充正式發布。

## Samsung 品牌使用與對外說明

本網站使用原創排版與通用矩形圖形，未額外產生或改造 Samsung Lettermark。正式品牌字標需依適用媒體模板與 Samsung Brand VI 規範審核，這份示範不是已核准的正式 Samsung 網站。先前私人 Google Drive 的品牌培訓 PDF 不公開，也未進 GitHub。

## 價格說明

網站顯示的是**特定容量 Samsung 台灣新聞稿發表時的上市建議售價**，不是今日通路價格、折扣或實際庫存；用戶購買前須以官方及販售現場為準。部分性能數據是指定條件下的「最高值」，不同容量、主機、線材可能不同。

版本：2026-11-13，示範用途。 
