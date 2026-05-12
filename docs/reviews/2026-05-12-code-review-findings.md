Findings

  1. Medium: index.html 仍依賴外部 CDN，和 README 的「下載單一檔案即可執行」不完全一致。
     index.html:7 載入 Tailwind CDN，index.html:8 到 index.html:10 載入 React / ReactDOM / Babel。也就是說使用者如果離
     線、CDN 被擋，或 GitHub Pages 網路不穩，頁面會直接不能跑。可是 README.en.md:18 說下載 index.html 用任何瀏覽器開即
     可，這點會誤導使用者。
  2. Medium: 目前是 production 頁面用 Babel Standalone 在瀏覽器即時編譯 JSX。
     index.html:10 載入 @babel/standalone，index.html:27 使用 type="text/babel"。這對小專案可以跑，但首次載入比較慢，也
     增加外部依賴。若之後要長期放 GitHub Pages，建議改成 build 後的靜態 JS，或至少把依賴版本固定下來。
  3. Low/Medium: README 說圖片有「背景預載」，但程式碼看起來沒有真的預載。
     README.en.md:20 寫了 background pre-loading；但實作只是在翻面後才建立圖片 URL：index.html:331，並在答案面才 render
     <img>：index.html:409。網路慢時翻面可能會先看到空白或載入中的圖片。
  4. Low: 空白鍵快捷鍵沒有 preventDefault()，桌面瀏覽器可能會同時觸發頁面捲動。
     快捷鍵邏輯在 index.html:309，空白鍵處理在 index.html:316。如果頁面高度超過視窗，按 Space 翻卡時可能也會讓頁面跳動。
  5. Low: 匯出的 CSV 沒有處理欄位內的雙引號。
     index.html:273 直接把 word、level、meaning 包在雙引號裡。如果之後單字解釋含有 "，CSV 會格式錯。現在資料大多可能沒問
     題，但這是容易補強的小風險。

  其他觀察

  Git 狀態目前乾淨，main 和 origin/main 同步。整體結構很單純，主要風險不是演算法壞掉，而是「單檔可執行」和實際 CDN 依賴
  不一致、以及 README 描述和程式實作有幾處落差。