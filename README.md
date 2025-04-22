# HW02 Web Crawler

## 摘要

本報告旨在透過網路資料擷取技術，收集來自 JokeAPI 的笑話資料，
本次收集目標為隨機十則笑話，包含笑話標題與內容，整理成結構化資料，供未來進行內容分析或自然語言處理應用。

## 引言

隨著人工智慧、自然語言處理（NLP）與資料科學技術的快速發展，文字資料的收集與整理變得越來越重要。
笑話作為一種輕鬆有趣的文本素材，廣泛應用於情緒分析、對話系統訓練等領域，
本次目標是以程式自動化方式，快速擷取免費開放的 JokeAPI 平台笑話資料，並整理為結構化資料集，以供後續分析與應用。

## 方法

- 目標網站描述
  - 目標網站：JokeAPI 笑話 API
    https://v2.jokeapi.dev/
  - 資料來源說明：JokeAPI 提供免費且不需註冊的 API，使用者可自訂笑話類型（如：一般、程式設計、暗黑、聖誕節等），資料以 JSON 格式返回，包含笑話類型、標題（或設定語句）、笑話內容等欄位。

- 工具與技術
  - requests：用來發送 HTTP 請求，取得 API 回傳的資料。
  - pandas：用來整理、儲存資料為結構化的 DataFrame，並輸出為 CSV 格式。
  - 開發輔助工具：無需使用瀏覽器開發者工具，JokeAPI 為公開 API，直接透過 HTTP GET 方法即可取得資料。

## 程式碼

```python
!pip install pandas requests

import requests
import pandas as pd

url = "https://v2.jokeapi.dev/joke/Any?amount=10"
response = requests.get(url)
data = response.json()

jokes = []
for joke in data.get("jokes", []):
    if joke["type"] == "single":
        jokes.append({
            "Title": "One-liner",
            "Content": joke["joke"]
        })
    else:
        jokes.append({
            "Title": joke["setup"],
            "Content": joke["delivery"]
        })

df = pd.DataFrame(jokes)

csv_filename = "jokes_from_api.csv"
df.to_csv(csv_filename, index=False, encoding="utf-8-sig")

```

## 結果

- 數據存儲方式
  - 將數據存儲為 CSV 格式，方便後續分析。
```python
import pandas as pd

df = pd.read_csv("jokes_from_api.csv")

df.head()
```

## 問題與挑挑戰

- 資料格式不一致:  
    JokeAPI 的資料有兩種格式：單句型 (single) 和問答型 (twopart)，需要根據 type 欄位判斷資料並分別處理。
- 資料量與速度限制:  
    請求過多資料（例如一次抓100筆），可能會遇到伺服器拒絕請求。

## 結論

- 成功獲取並分析了 KKday 推薦的前十名東京住宿資訊，為旅遊提供了有價值的參考。
- 未來可擴展至其他旅遊平台，進行跨平台比較分析。

