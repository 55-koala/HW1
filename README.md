# HW1
程式應用作業
{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "authorship_tag": "ABX9TyMP8NkyFXiKIcCfQK1a6QB1",
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/imchihchao/aop113b/blob/main/hw02.ipynb\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "# HW02 Web Crawler"
      ],
      "metadata": {
        "id": "eo72fZ0YlURV"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "## 摘要"
      ],
      "metadata": {
        "id": "hbqT3pl04Hl9"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "本報告旨在透過網路爬蟲技術，收集 KKday 網站上東京住宿的前十名推薦資料，為旅遊提供參考。"
      ],
      "metadata": {
        "id": "eweMw-wh4TC0"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "## 引言"
      ],
      "metadata": {
        "id": "9nb1aHAM4XiE"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "隨著旅遊需求的增加，選擇合適的住宿成為旅遊規劃中的重要環節。KKday 作為知名的旅遊平台，提供多樣的住宿選擇。\n",
        "\n",
        "本次爬蟲的目標是獲取 KKday 平台上東京住宿的前十名推薦，分析其價格、地理位置、評價等資訊，為旅遊者提供決策支持。"
      ],
      "metadata": {
        "id": "0ZmT034r5F9R"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "## 方法"
      ],
      "metadata": {
        "id": "8YMFd39F4n4l"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "- 目標網站描述\n",
        "  - 目標網站：KKday 東京住宿推薦頁面。  \n",
        "  https://www.kkday.com/zh-tw/category/jp-tokyo/accommodation\n",
        "  - 頁面結構：包含住宿名稱、圖片、價格、評價等資訊。\n",
        "\n",
        "- 工具與技術\n",
        "  - 使用 Python 的 `requests` 庫發送 HTTP 請求。\n",
        "  - 使用 `BeautifulSoup` 解析 HTML。\n",
        "  - 使用 Google Chrome 開發者工具取得 AJAX 資料。\n"
      ],
      "metadata": {
        "id": "zkix6XqZ429E"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# 爬取資料程式碼"
      ],
      "metadata": {
        "id": "ziaWIQ0t8vKt"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "## 結果\n"
      ],
      "metadata": {
        "id": "mHEo_iad7QMa"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "- 數據存儲方式\n",
        "  - 將數據存儲為 CSV 格式，方便後續分析。"
      ],
      "metadata": {
        "id": "Fx3h33cU8n8t"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# 展示資料程式碼"
      ],
      "metadata": {
        "id": "jsLbLuSa8mnY"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "## 問題與挑戰"
      ],
      "metadata": {
        "id": "6yHFop_b73gY"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "- 技術挑戰  \n",
        "    需透過 AJAX 取得資料\n",
        "- 資料限制  \n",
        "    部分住宿資訊可能不完整，影響分析結果。"
      ],
      "metadata": {
        "id": "D6roihku8PBu"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "## 結論"
      ],
      "metadata": {
        "id": "VeQHgVuqqD3J"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "\n",
        "- 成功獲取並分析了 KKday 推薦的前十名東京住宿資訊，為旅遊提供了有價值的參考。\n",
        "- 未來可擴展至其他旅遊平台，進行跨平台比較分析。"
      ],
      "metadata": {
        "id": "Baea2g7J9DAL"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "## 參考文獻"
      ],
      "metadata": {
        "id": "j5hI_9QW9dTt"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "* [KKDay](https://www.kkday.com/)"
      ],
      "metadata": {
        "id": "eLFvp2Fk9fSa"
      }
    }
  ]
}
