# 數據平台資料集 JSON 樣板說明

## 內容說明

### dataset 區塊

dataset 區塊在每個 json 檔裡只有一個，內容是整個資料集的概略說明，有以下欄位需要填寫：

1. title: 資料集標題
2. sub_title: 資料集副標題
3. description: 資料集內容說明
4. imgsrc: 在 unsplash 上找到的代表性圖片 (可不填)

### datasetfiles 區塊

datasetfiles 區塊的內容，在每個 json 檔裡可有可無，若沒有 datasetfiles，即代表此資料集沒有 CSV、JSON 可供下載。若有 datasetfiles，需填寫以下欄位：

1. file_name: 檔名
2. description: 各別檔案的敘述說明

### api 區塊

api 區塊的內容，在每個 json 檔裡可有可無，若沒有 api，即代表沒有 API 服務可供呼叫。若有 api，需填寫以下欄位：

1. api_name: API 名稱
2. url: API 的 URL 示意，因網址會公開在網路上，須請注意資安議題，主機位址或名稱部分可以省略
3. method: API 的呼叫方式，即 HTTP Method，如：GET、POST、PUT、DELETE
4. format: API 的回傳格式，如：JSON、XML，或沒有特定格式，則寫 PLAIN
5. frequency: API 的內容更新頻率，如果沒有固定頻率，請寫 "不定期"
6. authentication: API 的認證機制，"有" 或 "無"
7. query_mode: API 的查詢模式，若沒有特定查詢模式，請寫 HTTP，或為 ReST、SOAP、WebSocket 等

## 目錄結構與資料集建置說明

1. 建立 JSON 檔: 將第 n 個資料集的說明內容編輯完成後，命名為 n.json 
2. 建立資料集內容: 將第 n 個資料集的實際內容，壓縮成 `data.zip` 檔案，放在名為 n 的目錄下即可

## 品牌說明

品牌資料，請先修改 BRAND.json 的檔名為自己的品牌代碼，並把品牌的 logo 放入，置換 BRAND.png，檔名也是品牌代碼。並編寫以下欄位：

1. code: 品牌代碼，英文與數字，不可有空格或特殊符號，大小寫有區分
2. name: 品牌全名
3. imgsrc: 一開始所放之品牌 logo 圖片檔名
4. official_tel: 聯絡電話
5. official_email: 聯絡信箱
6. address: 聯絡地址，格式為：郵遞區號 + 地址
7. website: 品牌網址
8. description: 品牌簡介，格式為：HTML
