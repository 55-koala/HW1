# HW02 Web Crawler

## 摘要

本報告旨在透過網路爬蟲技術，收集 KKday 網站上東京住宿的前十名推薦資料，為旅遊提供參考。

## 引言

隨著旅遊需求的增加，選擇合適的住宿成為旅遊規劃中的重要環節。KKday 作為知名的旅遊平台，提供多樣的住宿選擇。

本次爬蟲的目標是獲取 KKday 平台上東京住宿的前十名推薦，分析其價格、地理位置、評價等資訊，為旅遊者提供決策支持。

## 方法

- 目標網站描述
  - 目標網站：KKday 東京住宿推薦頁面。  
  https://www.kkday.com/zh-tw/category/jp-tokyo/accommodation
  - 頁面結構：包含住宿名稱、圖片、價格、評價等資訊。

- 工具與技術
  - 使用 Python 的 `requests` 庫發送 HTTP 請求。
  - 使用 `BeautifulSoup` 解析 HTML。
  - 使用 Google Chrome 開發者工具取得 AJAX 資料。
