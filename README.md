# 肥胖風險預測 Demo · 第五組

一頁式預測網站，給期末簡報 QR Code Demo 使用。
直接呼叫 Render 上的 `obesity-api-2-2ro4.onrender.com`。

## 三種部署方式（任選）

### 方式 A：本機演示（最快）
```
雙擊 index.html 即可在瀏覽器開啟
```
**缺點**：QR Code 必須是線上網址，本機不能用。

---

### 方式 B：GitHub Pages（推薦，免費）
1. 在 GitHub 建一個新的 public repo，例如 `obesity-demo`
2. 把 `index.html` push 上去
3. Repo Settings → Pages → Source 選 `main` branch root → Save
4. 約 1 分鐘後拿到網址：`https://<你的帳號>.github.io/obesity-demo/`
5. 把這個網址轉成 QR Code（推薦 https://www.qr-code-generator.com/）

指令範例：
```bash
cd demo_site
git init
git add index.html
git commit -m "demo site"
git branch -M main
git remote add origin https://github.com/inorino/obesity-demo.git
git push -u origin main
```

---

### 方式 C：Render Static Site（也免費）
1. 登入 Render → New → Static Site
2. Connect repo（或 manual deploy 直接拖檔）
3. Publish directory: `.`
4. 拿到網址後產 QR Code

---

## 使用情境（期末 Demo）

1. 簡報播到 Demo 那頁時，秀 **QR Code 大圖**
2. 觀眾掃 QR → 開啟此頁面
3. 上方可切換「簡易版（6 項）」/「完整版（15 項）」
4. 填完按「預測我的肥胖風險」→ 半圓儀表板顯示機率
5. 顏色分級：
   - 綠色 `<35%`：風險低
   - 黃色 `35–65%`：邊界
   - 紅色 `>65%`：風險高

## 演示前 5 分鐘要做的事

1. **手機掃一次 QR**，喚醒 Render 免費方案（避免冷啟動 30 秒尷尬）
2. 試填一次，確認 API 回傳正常
3. 簡報時若 cold start，可先用「穩定高風險」場景的截圖頂著
