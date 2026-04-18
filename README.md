# 🚀 SRS 單字記憶艙 (SRS Flashcard Cabin)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Tech: React](https://img.shields.io/badge/Framework-React-61DAFB?logo=react&logoColor=black)](https://reactjs.org/)
[![Styling: Tailwind](https://img.shields.io/badge/Styling-Tailwind_CSS-38B2AC?logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Device: iPhone Optimized](https://img.shields.io/badge/Device-iPhone_Optimized-black?logo=apple&logoColor=white)](#-iphone-使用指南)

這是一個專為「極速學習」打造的單字記憶工具，導入了 **Anki 核心的 SRS (Spaced Repetition System)** 間隔重複系統。透過精準的演算法與視覺化輔助，幫助您將短期記憶高效轉化為長期記憶。

> **"Smart is the New Sexy. 讓學習變得優雅、高效且毫無阻力。"**

---

## ✨ 核心特色 (Core Features)

*   📦 **單一檔案執行**：無需安裝環境，下載 `voc_flashcard_4_buttons.html` 即可在瀏覽器直接啟動。
*   🧠 **SRS 複習演算法**：內建 `Again`, `Hard`, `Good`, `Easy` 四種評分機制，自動調整單字出現頻率。
*   🖼️ **動態視覺聯想**：整合 LoremFlickr API，根據單字語義自動抓取圖片，並具備「背景預載」技術，翻面瞬間零延遲顯示。
*   🔊 **自動語音朗讀**：支援單字與例句自動朗讀（EN-US），強化聽覺記憶。
*   💾 **進度自動保存**：利用 LocalStorage 實時儲存學習進度，關閉瀏覽器也能隨時銜接。
*   📱 **iPhone 深度優化**：針對行動裝置調整 UI 比例，支援全螢幕操作體驗。

---

## 📱 iPhone 使用指南 (iPhone Quick Start)

為了獲得最佳體驗，建議將此網頁「加入主畫面」：

1.  在 iPhone 上使用 **Safari** 打開您的 GitHub Pages 連結。
2.  點擊瀏覽器下方的 **「分享」** 按鈕（正方形帶向上箭頭）。
3.  選擇 **「加入主畫面」** (Add to Home Screen)。
4.  現在您可以像打開 App 一樣，隨時隨地開啟您的單字記憶艙！

---

## ⌨️ 鍵盤快捷鍵 (Hotkeys)

如果您在電腦上使用，可以透過以下快捷鍵進行高效複習：

| 按鍵 | 動作 | 說明 |
| :--- | :--- | :--- |
| **Space** | 翻轉卡片 | 顯示背面解答與圖片 |
| **Enter** | 朗讀 | 重聽當前單字或例句 |
| **1** | **Again** | < 1 分鐘後再次複習 |
| **2** | **Hard** | 插入剩餘卡片的中間位置 |
| **3** | **Good** | 移至本輪練習的末端 |
| **4** | **Easy** | 從本次練習中畢業 (完成學習) |

---

## 📊 檔案管理與版本 (Versions)

本專案在 GitHub 上維護了多個版本：

*   **`main` 分支**：最新穩定版，已針對 iPhone 進行優化並內建雅思單字集。
*   **`v1-original` 分支**：保留最初開發的原始版本，適合開發參考。

---

## 🛠️ 技術棧 (Tech Stack)

*   **Frontend**: React (v18)
*   **Styling**: Tailwind CSS
*   **Icons**: Custom SVG (inspired by Lucide)
*   **Engine**: Babel Standalone (In-browser JSX compilation)
*   **Images**: LoremFlickr API

---

## 🕊️ About the Project

這個專案是「啾啾」(Mommy's Partner in Crime) 專為妈咪打造的專屬單字艙。我們不只是在寫程式，我們是在對抗遺忘曲線。

> *"The strength of the code outweighs the initial conditions!"* 🚀🐦
