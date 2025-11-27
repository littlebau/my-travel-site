# 冰島旅行網頁教學專案

這是一個模仿專業旅行網站設計的教學專案，展示如何建立一個美觀的單頁式旅行網站。

## 📁 專案結構

```
travel-website/
├── index.html      # 主要 HTML 結構
├── styles.css      # 樣式表
├── script.js       # JavaScript 互動功能
└── README.md       # 說明文件
```

## 🎨 主要特色

### 1. 響應式設計
- 適配手機、平板、電腦等不同螢幕尺寸
- 使用 CSS Grid 和 Flexbox 進行布局
- 媒體查詢（Media Queries）實現自適應

### 2. 互動功能
- 平滑滾動導航
- 漢堡選單（移動端）
- FAQ 展開/收合
- 滾動動畫效果
- 返回頂部按鈕

### 3. 視覺效果
- 漸層背景
- 懸停（Hover）動畫
- 圖片畫廊
- 陰影和圓角設計

## 🚀 使用方法

### 快速開始
1. 直接用瀏覽器打開 `index.html`
2. 或使用 VS Code 的 Live Server 擴充功能

### 使用 Live Server（推薦）
```bash
# 安裝 Live Server（如果尚未安裝）
# 在 VS Code 中按 Ctrl+Shift+X 搜尋 "Live Server" 並安裝

# 右鍵點擊 index.html
# 選擇 "Open with Live Server"
```

### 使用 Python 簡易伺服器
```bash
# Python 3
cd travel-website
python -m http.server 8000

# 然後在瀏覽器開啟 http://localhost:8000
```

## 📚 學習重點

### HTML 結構
- **語義化標籤**：使用 `<nav>`, `<section>`, `<footer>` 等語義化標籤
- **區塊設計**：將網頁分為多個獨立區塊（導航、英雄區、行程、畫廊等）
- **圖片優化**：使用 Unsplash 高品質免費圖片

### CSS 技巧

#### 1. CSS 變數（自訂屬性）
```css
:root {
    --primary-color: #1a5f7a;
    --secondary-color: #159895;
}
```
優點：方便主題切換和維護

#### 2. Flexbox 布局
```css
.nav-menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

#### 3. Grid 布局
```css
.gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
}
```

#### 4. 動畫效果
```css
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
```

### JavaScript 功能

#### 1. 平滑滾動
```javascript
element.scrollIntoView({
    behavior: 'smooth',
    block: 'start'
});
```

#### 2. Intersection Observer（滾動動畫）
```javascript
const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.classList.add('visible');
        }
    });
});
```

#### 3. 事件監聽
```javascript
element.addEventListener('click', () => {
    // 執行動作
});
```

## 🎯 自訂化建議

### 更換顏色主題
在 `styles.css` 中修改 CSS 變數：
```css
:root {
    --primary-color: #你的顏色;
    --secondary-color: #你的顏色;
    --accent-color: #你的顏色;
}
```

### 更換圖片
1. 替換 Unsplash 圖片連結
2. 或使用本地圖片：
   ```html
   <img src="images/your-image.jpg" alt="描述">
   ```

### 新增更多內容
1. 複製 `.day-card` 區塊
2. 修改內容
3. 更新日期和資訊

### 整合 Google Maps
```html
<iframe 
    src="https://www.google.com/maps/embed?pb=..." 
    width="100%" 
    height="450" 
    style="border:0;">
</iframe>
```

## 🔧 進階功能建議

### 1. 表單功能
新增聯絡表單或報名表單：
```html
<form>
    <input type="text" placeholder="姓名" required>
    <input type="email" placeholder="Email" required>
    <textarea placeholder="訊息"></textarea>
    <button type="submit">送出</button>
</form>
```

### 2. 輪播圖（Carousel）
使用 Swiper.js 或自行開發

### 3. 燈箱效果（Lightbox）
點擊圖片後放大顯示

### 4. 多語言支援
使用 JavaScript 切換語言

### 5. 深色模式
```javascript
const toggleDarkMode = () => {
    document.body.classList.toggle('dark-mode');
};
```

## 📱 響應式斷點

```css
/* 手機 */
@media (max-width: 480px) { }

/* 平板 */
@media (max-width: 768px) { }

/* 桌機 */
@media (min-width: 1024px) { }
```

## 🌐 部署到網路

### GitHub Pages（免費）
1. 在 GitHub 建立新倉庫
2. 上傳所有檔案
3. Settings → Pages → 選擇 main 分支
4. 網站會發布到 `https://你的帳號.github.io/倉庫名稱/`

### Netlify（免費）
1. 拖放整個資料夾到 Netlify
2. 自動部署並獲得網址

### Vercel（免費）
1. 連接 GitHub 倉庫
2. 自動部署

## 📖 延伸學習資源

- **MDN Web Docs**：https://developer.mozilla.org/
- **CSS-Tricks**：https://css-tricks.com/
- **Google Fonts**：https://fonts.google.com/
- **Unsplash（免費圖片）**：https://unsplash.com/
- **Font Awesome（圖示）**：https://fontawesome.com/

## 🎓 練習建議

1. **修改現有內容**：更換文字、圖片、顏色
2. **新增新區塊**：如「客戶評價」、「價格方案」
3. **改善 RWD**：測試不同裝置的顯示效果
4. **加入動畫**：使用 AOS.js 或 GSAP
5. **優化效能**：壓縮圖片、最小化 CSS/JS

## ⚡ 效能優化

### 圖片優化
- 使用 WebP 格式
- 設定適當尺寸
- 實作延遲載入（Lazy Loading）

### CSS 優化
- 移除未使用的樣式
- 使用 CSS Minifier 壓縮

### JavaScript 優化
- 延遲非必要的腳本載入
- 使用事件委派（Event Delegation）

## 🐛 常見問題

### Q: 圖片顯示不出來？
A: 確認圖片連結是否正確，或使用本地圖片

### Q: 在手機上選單無法點擊？
A: 檢查 z-index 和 JavaScript 是否正確載入

### Q: 動畫不流暢？
A: 使用 `transform` 和 `opacity` 而非 `width`, `height` 等屬性

## 📝 授權

本專案為教學用途，可自由使用和修改。

---

**祝你學習愉快！🎉**

如有問題歡迎詢問或查閱相關文件。
