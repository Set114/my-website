# 教師個人網頁

學術正式風格的教師個人網站，適合部署至 Netlify。

## 檔案結構

```
teacher-website/
├── index.html          首頁
├── about.html          個人簡介
├── research.html       研究領域
├── publications.html   著作發表
├── teaching.html       開授課程
├── contact.html        聯絡我們
├── style.css           共用樣式
└── netlify.toml        Netlify 設定
```

## 部署到 Netlify 步驟

### 方法一：拖放上傳（最簡單）
1. 前往 https://app.netlify.com
2. 登入後點選 **"Add new site" → "Deploy manually"**
3. 將整個 `teacher-website` 資料夾**拖放**到上傳區域
4. 數秒後即完成部署，獲得 `.netlify.app` 網址

### 方法二：連結 GitHub（推薦，可自動更新）
1. 將本資料夾上傳至 GitHub 儲存庫
2. 在 Netlify 點選 **"Add new site" → "Import an existing project"**
3. 連結 GitHub，選取該儲存庫
4. Publish directory 設為 `/`（根目錄），點選 Deploy
5. 日後 push 到 GitHub 即自動重新部署

## 個人化修改指引

### 修改基本資訊
- 搜尋 `林冠妤` 並替換為真實姓名
- 搜尋 `dmwang@ntu.edu.tw` 並替換為真實 email
- 搜尋 `國立臺灣大學` 並替換為真實學校
- 搜尋 `資訊管理學系` 並替換為真實學系
- 搜尋 `NTU` (logo) 並替換為學校縮寫

### 新增大頭照
在 `about.html` 將 `.avatar-lg` 裡的文字改為 `<img>` 標籤：
```html
<div class="avatar-lg">
  <img src="photo.jpg" alt="教授照片" style="width:100%; border-radius:12px; object-fit:cover;">
</div>
```
將照片命名為 `photo.jpg` 放入同一資料夾。

### 嵌入 Google Maps（聯絡頁面）
在 `contact.html` 找到 `.map-placeholder` 並替換為：
```html
<iframe
  src="https://www.google.com/maps/embed?pb=YOUR_EMBED_URL"
  width="100%" height="300" style="border:0; border-radius:10px;"
  allowfullscreen loading="lazy">
</iframe>
```

### 自訂網域
在 Netlify → Site settings → Domain management 設定您的網域。
