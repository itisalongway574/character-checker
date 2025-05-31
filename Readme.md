

# 繁體中文用字檢查與取代工具

本專案是一個基於 HTML + TailwindCSS + Firebase 的繁體中文用字檢查工具，協助使用者自動檢查、標示、與取代常見的繁體中文同音／通用字，並支援自訂規則、Google 登入與匿名使用。

---

## 主要功能

- **自動檢查並標示常見的繁體中文用字問題**  
- **高亮顯示、批次取代、逐筆忽略／取代**  
- **檢查項目可自訂並儲存（需登入）**
- **支援 Google 登入／匿名登入**
- **深淺色主題切換**
- **資料雲端同步（Firebase Firestore）**

---

## 專案架構

- 只需單一 `index.html` 檔案（可直接部署於靜態主機）
- 前端完全純 HTML + CSS（Tailwind）+ 原生 JavaScript
- 資料儲存與登入驗證使用 Firebase

---

## 快速開始

1. **下載專案**
   ```bash
   git clone <你的 repo 位置>
   cd checker
   ```

2. **Firebase 設定（可選）**  
   若需使用雲端同步與登入功能，請至 [Firebase Console](https://console.firebase.google.com/) 建立專案並取得 config。  
   預設程式碼中已填入測試用的 config（僅供測試用，請務必更換為自己的 Firebase config）。

   - 將 config 資訊（apiKey、projectId...等）填入 `index.html` 內的 `firebaseConfig` 變數。

3. **開啟 `index.html`**
   - 用瀏覽器開啟 `index.html` 即可使用。
   - 若要部署到網站，只需將本檔案上傳至你的靜態主機（如 GitHub Pages、Vercel、Netlify...）。

---

## 主要技術

- [Tailwind CSS](https://tailwindcss.com/)（CDN 版）
- [Font Awesome](https://fontawesome.com/icons)
- [Firebase JS SDK v11](https://firebase.google.com/docs/web/setup)  
  - Auth (Google, 匿名)
  - Firestore

---

## 注意事項

- **個人化與自訂規則需登入，未登入僅能使用預設規則且不會雲端儲存。**
- 若需要多帳號、團隊共用，請調整 Firebase rules。
- 此專案所有內容皆於前端運算與顯示，不會將使用者原文資料上傳到後端（僅同步規則設定）。

---

## 版權

MIT License.

---

如有問題或建議，歡迎提出 issue 或聯絡作者。