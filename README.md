# Travel Journal｜我的旅遊行程網站

以 GitHub Pages 發佈，包含所有旅程的獨立行程頁。

## 目前旅行

- [2026 東京＋北海道冬日旅程](./trips/2026-japan/index.html)

## GitHub Pages 初次部署

1. 於 GitHub 建立新的 **Public**、空白 Repository，建議名稱 `travel-journal`，**不必勾選** README 或 .gitignore（本專案已附檔）。
2. 解壓縮本壓縮檔，將本專案根目錄內的檔案放入 Repository。注意 `index.html` 要在 Repository 根目錄。
3. GitHub Repository > **Settings** > **Pages** > **Build and deployment** > **Source: Deploy from a branch** > **Branch: main** > **/(root)** > **Save**。
4. 之後網站會在 `https://你的GitHub帳號.github.io/travel-journal/` 出現。

若使用終端機，在解壓後的本資料夾執行：

```bash
git init
git add .
git commit -m "Launch travel journal with 2026 Japan itinerary"
git branch -M main
git remote add origin https://github.com/你的GitHub帳號/travel-journal.git
git push -u origin main
```

## 下一趟旅行怎麼新增？

**目前是零建置的純靜態 HTML 版本**：

- 將 `trips/2026-japan/index.html` 複製到 `trips/2027-korea/index.html`，修改新旅行資料與插畫
- 回到根目錄 `index.html` 加一張通往新旅行的卡片
- 推送 GitHub，GitHub Pages 會發佈更新

**未來若希望行程內容只寫 Markdown 或 YAML：** 建議升級成 Astro 的共用版型與資料集。SVG 插畫／動畫獨立為 Hero 元件，Markdown/YAML 存放日期、航班、時間軸和購物資訊；GitHub Actions 建置後發佈 GitHub Pages。這一版尚未使用 Markdown 即時驅動 HTML，避免誤以為新增 .md 就能自動出頁。

## 注意

- HTML 有瀏覽器端的待辦及購物勾選記憶（localStorage），**每台裝置／每個瀏覽器分開保存**，不會同步到 GitHub。
- 頁面會向 Google Fonts 取得 Huninn 字型；離線可退回系統字型。
- 吉伊卡哇門票、餐廳訂位、北海道神宮限定梅酒庫存均需要出發前重新確認。
- GitHub Pages 是公開網站，請勿上傳航班訂位代號、護照或其他個人資料。
