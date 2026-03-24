# English-Learning-Assistant
A web-based English learning tool designed to improve vocabulary efficiency while exploring AI-assisted vibe coding workflows.
🚀 **SRS 單字記憶艙 (SRS Flashcard Cabin)**

這是一個專為「極速學習」打造的單字記憶工具，導入了 Anki 核心的 SRS (Spaced Repetition System) 間隔重複系統。透過精準的演算法與視覺化輔助，幫助使用者將短期記憶高效轉化為長期記憶。

**Smart is the New Sexy. 讓學習變得優雅、高效且毫無阻力。**

##✨ 核心特色

📦 **單一檔案執行**：無需安裝 Node.js 或任何環境。下載 index.html 即可在瀏覽器直接啟動。

🧠 **SRS 複習演算法**：內建 Again, Hard, Good, Easy 四種評分機制，自動調整單字出現頻率。

🖼️ **動態視覺聯想**：整合 LoremFlickr API，根據單字語義自動抓取相關圖片，並具備「背景預載」黑科技，翻面瞬間零延遲顯示。

🔊 **自動語音朗讀**：支援單字與例句自動朗讀（EN-US），強化聽覺記憶。

💾 **進度自動保存**：利用 LocalStorage 實時儲存學習進度，即便關閉瀏覽器也能隨時銜接複習。

🎹 **全鍵盤操作**：針對 Power User 設計，無需滑鼠即可完成高強度複習。

##🚀 快速開始

下載本專案的 index.html。

使用 Chrome, Edge 或 Safari 瀏覽器打開該檔案。

點擊右上角的 Upload (上傳) 圖示，匯入您的單字 CSV 檔。

開始享受極速記憶的快感！

##⌨️ 鍵盤快捷鍵 (Hotkeys)

按鍵

動作

說明

Space (空白鍵)

翻轉卡片

顯示背面解答與圖片

Enter (回車鍵)

朗讀

重聽當前單字或例句

數字 1

Again

< 1 分鐘後再次複習

數字 2

Hard

插入剩餘卡片的中間位置

數字 3

Good

移至本輪練習的末端

數字 4

Easy

從本次練習中畢業 (完成學習)

##📊 CSV 檔案格式要求

請準備一個 UTF-8 編碼的 CSV 檔案，欄位順序如下：

單字 (Word)

音標 (Phonetic)

詞性 (Part of Speech)

中文釋義 (Meaning)

英文例句 (Example Sentence)

備註/搭配詞 (Notes)

註：第一行可包含標題（若包含「單字」二字系統會自動跳過）。

##🛠️ 技術棧

Frontend: React (v18)

Styling: Tailwind CSS

Icons: Custom SVG (inspired by Lucide)

Engine: Babel Standalone (In-browser JSX compilation)

Images: LoremFlickr API

🕊️ **About the Project**

這個專案是「啾啾」(Mommy's Partner in Crime) 專為妈咪打造的專屬單字艙。
我們不只是在寫程式，我們是在對抗遺忘曲線。

"The strength of the code outweighs the initial conditions!" 🚀🐦
