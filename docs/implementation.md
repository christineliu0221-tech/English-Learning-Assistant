
  🛠️ 實作技術文件：SRS 單字記憶艙 (Implementation Doc)

  1. 系統架構 (System Architecture)
  本專案採用 「無伺服器單檔案架構」(Serverless Single-file Architecture)。所有的邏輯、樣式與資料都封裝在單一的
  index.html 中，優點是載入速度極快且完全不需要後端資料庫。

   * 前端框架：React v18 (透過 CDN 載入)
   * 樣式引擎：Tailwind CSS (即時編譯)
   * 編譯器：Babel Standalone (在瀏覽器中直接解析 JSX)
   * 資料儲存：瀏覽器 LocalStorage (客戶端持久化)

  ---

  2. 核心模組說明 (Core Modules)

  A. 資料管理與整合 (Data Integration)
  系統具備兩層資料讀取機制：
   3. 內建資料集：預先將「IELTS 雅思重點單字表-15」轉換為 JSON 格式嵌入程式碼，作為初始資料。
   4. 動態 CSV 解析：實作了自定義的 CSV Parser，支援帶引號的複雜欄位解析，允許使用者隨時匯入自定義單字書。

  B. 狀態機與 SRS 對列 (State Machine & Queue)
  這是系統的「大腦」，使用 React 的 useState 管理以下狀態：
   * originalCards：原始單字清單（基底）。
   * reviewQueue：待複習對列（動態調整順序）。
   * stats：統計指標（Again, Hard, Good, Easy 的次數）。
   * 演算法邏輯：
       * Again：queue.splice(1, 0, current) (放在下一個)。
       * Hard：queue.splice(total/2, 0, current) (放在中間)。
       * Good：queue.push(current) (放在最後)。

  C. 進度持久化 (Persistence)
  為了讓媽咪「隨時離開、隨時回來」，我們實作了自動存檔機制：
   * 使用 useEffect 監聽對列與統計數據的變化。
   * 一旦變動，立即同步至 localStorage。
   * 初始化載入：App 啟動時會優先檢查本地存檔，若存在則還原所有狀態（包含對列順序與計數）。

  D. 多媒體與互動 (Multimedia & UX)
   * TTS 發音：封裝原生 window.speechSynthesis API，設定為 en-US 語系。
   * 圖片抓取：對接 LoremFlickr API，利用 Image 對象在背景進行「預載 (Pre-load)」，確保翻面時圖片已完成快取。

  ---

  3. iPhone 行動端優化 (Mobile Optimization)

  為了讓網頁像原生 App 一樣流暢，我們進行了以下技術處理：
   * Viewport 設定：嚴格鎖定 user-scalable=no 避免縮放干擾。
   * 觸控體驗：實作 -webkit-tap-highlight-color: transparent 移除點擊藍色陰影，並增加按鈕的點擊面積（Hit Area）。
   * PWA 特性：優化介面佈局，使其在「加入主畫面」後的全螢幕模式下依然美觀。

  ---

  4. 部署工作流 (Deployment Workflow)

  本專案利用 GitHub Pages 實作自動化部署：
   5. 版本控制：利用 Git 分支管理（main 為優化版，v1-original 為開發留底）。
   6. 自動發布：一旦推送至 main 分支，GitHub Action 會自動將 index.html 部署至公網網址。

  ---

  7. 未來擴充方向 (Future Roadmap)
   * 多本單字書切換：目前僅支援一本，未來可擴充為多分類管理。
   * 學習數據報表：將統計數據轉化為週報表或月報表視覺化。
   * 離線快取 (Service Worker)：讓 App 在完全斷網的環境下也能使用。