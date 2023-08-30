# LineBot ChatGPT3.5-阿敏之音

* 一個簡易的LineBot，[串接Open AI](https://www.npmjs.com/package/openai)，讓使用者可以直接在Line上和ChatGPT問問題。

* LineBot ID：阿敏之音　@560fzvhu
* 雲端伺服器佈署：[Render](https://render.com/)
* LINE官方：[LineBot API](https://developers.line.biz/zh-hant/services/messaging-api/)

## LineBot畫面

![image](https://github.com/AlanChiangg/LineBot-ChatGPT3.5/blob/main/images/linebotgif.gif)

## 如何套用成自己的LineBot

1. 註冊 [OpenAI 帳號](https://platform.openai.com) 並取得 API Key
2. 申請 [Line Developer 帳號](https://developers.line.biz/zh-hant/) 並取得 API Key
3. 開啟終端機，Clone 此專案
    ```
    git clone https://github.com/AlanChiangg/LineBot-ChatGPT3.5.git
    ```
4. 接著進入存放此專案的資料夾
    ```
    cd LineBot-ChatGPT3.5
    ```
5. 安裝 npm 套件
    ```
    npm install
    ```    
6. 建立.env檔案，輸入你的環境變數
    ```
    CHANNEL_ACCESS_TOKEN=輸入你的Channel Access Token
    CHANNEL_SECRET=輸入你的Channel Secret
    OPENAI_API_KEY=輸入你的openai API Key
    ```
7. 更改AI腳色設定，至app.js的handleEvent function中的messages，修改成自己想要的AI腳色設定
    ```
    messages: [
      {
        role: 'user',
        content: '<輸入你想要的AI腳色設定>'
      },
      {
        role: 'user',
        content: event.message.text
      }
    ]
    ```
8. 佈署於自己的雲端伺服器，本專案佈署於[Render](https://render.com/)，完成佈署後即可使用！


## 開發環境與主要套件

* VS Code - 編程環境
* JavaScript - 程式語言
* node.js / express.js@4.18.2 - 後端框架
* openai@4.3.1 - 串接chatGPT API 套件
* @line/bot-sdk@7.5.2 - 串接LineBot API 套件
* dotenv@16.0.3 - 管理環境變數
* eslint@8.36.0 - 代碼風格
