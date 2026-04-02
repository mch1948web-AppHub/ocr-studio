# OCR Studio — 手寫文字辨識工具

純前端應用，使用 Claude Vision API 辨識手寫文字，輸出 Excel。

## 功能
- 上傳多張照片
- 在照片上自由拖曳圈選區域（每個區域可命名欄位）
- 呼叫 Claude API 辨識手寫文字
- 逐張確認後，一次匯出 Excel

## 部署到 Netlify

1. 將整個資料夾上傳到 GitHub
2. 在 Netlify 建立新 Site，連結 GitHub repo
3. Build 設定：
   - Build command：（留空）
   - Publish directory：`.`
4. 部署完成！

## 使用方式

1. 開啟網頁後，在頂部輸入你的 **Anthropic API Key**（`sk-ant-...`）
2. 從左側上傳一或多張照片
3. 點選照片後，在中間畫布上 **拖曳圈選** 要辨識的區域
4. 右側為每個區域輸入 **欄位名稱**（如：姓名、日期、金額）
5. 點「辨識此區域」或「辨識全部區域」
6. 確認結果後點「確認加入清單」
7. 重複 3-6 步驟處理每張照片
8. 所有照片完成後，點「匯出 Excel」

## API Key 說明

- API Key 僅存在瀏覽器 session 中，不會上傳任何伺服器
- 照片圖檔也在瀏覽器本地處理
- 每位使用者需自行輸入自己的 Anthropic API Key
- 取得 API Key：https://console.anthropic.com
