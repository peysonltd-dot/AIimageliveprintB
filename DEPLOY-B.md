# B 前台 v8

解壓縮後把全部內容覆蓋到 peysonltd-dot/AIimageliveprintB 根目錄，包括 assets/ip-catalog.js、assets/ip-catalog.json、assets/ips/ 六張 SVG。不更動 A 機。

先部署 B 後端 v8，再部署本前台；網址固定連到 https://aicamera-backend-b.onrender.com。

前台流程：選一個 IP → 拍照 → 水彩／超 Q 二選一 → 確認送出 → 工作人員下載 PNG 印製。
畫面應有六個角色選項；未選角色時不能開始拍照。若仍顯示舊畫面，請 Ctrl+Shift+R 或以無痕視窗開啟。

新任務為含透明背景及四周 8% 空隙的 PNG，水花保留。棋盤格只用於顯示透明度，下載不會包含。結果預覽完整顯示，不裁切；後台與手機下載不再將 PNG 存成 JPG，人工補傳也使用 PNG。

舊 JPG 任務不會自動轉成透明；請建立新任務驗收。詳情及技術限制見後端 DEPLOY-B.md。
