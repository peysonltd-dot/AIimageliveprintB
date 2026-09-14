# B 前台 V19：雲端保存狀態與 PNG 下載

本包配合 B 後端 V19 使用，新增後台「已保存／保存未完成／重新保存」與雲端圖片的 PNG 下載。
「重新保存」只儲存既有圖片，不呼叫 Leonardo。原有備註若保存失敗，會明確提示。

## 更新順序

1. 先下載舊版後台需要保留的成品；Render 更新或修改環境設定會清除舊記憶體。
2. 依後端包的 DEPLOY-B.md 完成 Firebase Storage 與 Render 服務帳戶設定，更新 B 後端 V19。
3. 將本包解壓縮，內容覆蓋到 `peysonltd-dot/AIimageliveprintB` 根目錄，不要只上傳 ZIP。
4. Ctrl＋Shift＋R 或開無痕視窗，登入後台，試拍確認「已保存至雲端」。

首頁、Loading、合影確認頁、完成頁、QR 下載頁與 V18 相同；保留活動 SVG 高清標題、船與海浪、進度條、倒數與回首頁按鈕。
本次只調整 admin.html。管理密碼仍由 Render 的 ADMIN_PASSWORD 決定（本次指定 admin888），前台沒有儲存密碼。

## 注意

- Firebase 專案以 B 機 Render 的 FIREBASE_CONFIG.projectId 為準，不依顯示名稱猜測。
- Firebase Storage 目前需要 Blaze 方案；此更新沒有替你開啟計費。
- 保存失敗的圖片仍可預覽、下載備份；「確定」會等雲端保存成功後才完成，不需工作人員核准畫質。
- 原有白底產圖與去背設定保持不變。
- 前後端請搭配 V19；舊後端沒有新版的圖片下載／重新保存接口。

已通過前台語法與後台 DOM 模擬驗證。尚未在你的 Firebase 與實際瀏覽器完成上線驗收；後端包附完整測試與設定步驟。
