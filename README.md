# 弈思學堂 網站

單頁式靜態網站，`index.html` 為自包含檔案（CSS / JS 皆內嵌），唯一外部資源是 Google Fonts。

## 用 GitHub Pages 部署

1. 在 GitHub 建立一個新 repo（例如 `yisi-academy`）。
2. 把這個資料夾裡的 `index.html` 和 `favicon.svg` 放到 repo 根目錄，推上去：

   ```bash
   git init
   git add index.html favicon.svg README.md
   git commit -m "弈思學堂網站初版"
   git branch -M main
   git remote add origin https://github.com/<你的帳號>/<repo名稱>.git
   git push -u origin main
   ```

3. 到 repo 的 **Settings → Pages**，Source 選 `Deploy from a branch`，Branch 選 `main` / `/(root)`，存檔。
4. 等 1～3 分鐘，網站會上線在：
   `https://<你的帳號>.github.io/<repo名稱>/`

   如果 repo 名稱取 `<你的帳號>.github.io`，網址就會是根網域 `https://<你的帳號>.github.io/`。

## 之後要換自訂網域

在 repo 根目錄加一個 `CNAME` 檔案，內容寫你的網域（例如 `yisi.tw`），並到網域的 DNS 設定裡把 A 記錄指到 GitHub Pages 的 IP（或用 CNAME 記錄指到 `<你的帳號>.github.io`）。

## 注意事項

- 網頁裡包含真實地址（高雄市鳳山區保安二街）與陳老師的真實學歷/經歷，上線後任何人都能看到，請確認要公開這些資訊。
- 之後若要換圖片、Logo 向量檔，建議另外開一個 `assets/` 資料夾放置，再修改 `index.html` 裡對應的路徑。
