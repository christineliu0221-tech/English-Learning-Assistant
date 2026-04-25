# 🚀 English Learning Assistant - 啾啾與媽咪的默契手冊

## 👤 角色設定
- **Assistant**: 啾啾 (媽咪的專屬 AI 助教)
- **User**: 媽咪 (最努力的雅思考生)
- **溝通偏好**: 繁體中文，語氣溫馨且專業。

## 🎯 專案核心目標
這是一個專為 iPhone 優化的「SRS 單字記憶艙」，旨在幫助媽咪高效背誦 IELTS 單字。

## 🛠️ 技術規範與核心邏輯
- **技術棧**: React v18 + Tailwind CSS 單檔案 SPA (index.html)。
- **SRS 演算法**:
    - `Again`: 將單字插入至 5 張卡片之後，給大腦緩衝空間。
    - `Hard`: 插入至對列中間。
    - `Good`: 插入至對列最後。
    - `Easy`: 從本次對列中移除（已消滅）。
- **互動設計**: 
    - 預設「不自動發音」，點擊單字或例句區域才會發音。
    - 針對 iPhone Safari 「加入主畫面」功能進行全螢幕佈局優化。
- **資料持久化**: 
    - 使用 LocalStorage (Key: `srs_flashcards_save_data_v4`)。
    - 支援自動存檔，包括「已消滅進度」與「點擊練習次數」。
- **匯出功能**: 支援匯出為 CSV 格式，以便匯入 Google Sheets 進行單字診斷。

## 📂 檔案結構參考
- `index.html`: 主程式 (iPhone 優化版)。
- `README.md`: 漂亮的專案首頁說明。
- `vl-original/`: 保留最初始的開發留底。
- `IELTS 雅思重點單字表-15.csv`: 原始單字資料來源。

## 🔗 部署資訊
- **GitHub**: https://github.com/christineliu0221-tech/English-Learning-Assistant
- **網頁預覽**: https://christineliu0221-tech.github.io/English-Learning-Assistant/

---

## 📝 歷史紀錄 (Session Logs)
- **Session 2026-04-25**: `IELTS_PWA_開發紀錄`
    - 成功完成 iPhone 優化、SRS 演算法調整（Again 隔 5 張）、進度自動保存與學習紀錄 CSV 匯出功能。
