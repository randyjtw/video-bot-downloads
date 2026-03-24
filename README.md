# Video Auto Bot 下載版使用說明

本頁面只提供可執行檔下載，不含原始碼。

## 下載檔案

1. `video_bot_mac_v1.02.zip`（macOS）
2. `video_bot_win_v1.02.zip`（Windows）
3. `video_bot_mac_v1.01.zip`（macOS，舊版）
4. `video_bot_win_v1.01.zip`（Windows，舊版）
5. `video_bot_mac_v1.0.zip`（macOS，舊版）
6. `video_bot_win_v1.0.zip`（Windows，舊版）

## v1.02 變更內容

1. 修正Agent行為

## macOS 安裝與啟動

1. 解壓縮 `video_bot_mac_v1.02.zip`
2. 進入 `mac/`
3. 雙擊 `launch_mac.command`
4. 開啟瀏覽器進入 `http://localhost:8080`

第一次啟動若被系統阻擋，請到「系統設定 > 隱私權與安全性」允許執行。

## Windows 安裝與啟動

1. 解壓縮 `video_bot_win_v1.02.zip`
2. 進入 `win/`
3. 雙擊 `launch_windows.bat`
4. 開啟瀏覽器進入 `http://localhost:8080`

## 首次使用前必做

1. 在 Chrome 先登入 ChatGPT：<https://chatgpt.com>
2. 在 Chrome 先登入 Sora：<https://sora.chatgpt.com>

## 建立 Telegram Bot（BotFather）

1. 在 Telegram 搜尋 `@BotFather`
2. 輸入 `/newbot`
3. 設定 Bot 名稱與帳號（帳號需以 `bot` 結尾）
4. 取得 Bot Token（格式類似 `123456789:AA...`）

## 連接你的 Bot

1. 打開 Web 控制台「Telegram Bot 設定」
2. 貼上 Token 並按「儲存設定」
3. 按「啟動 Bot」

## 驗證使用者（300 秒效期）

Web 會同時顯示兩組 6 位驗證碼：

1. `owner` 驗證碼
2. `operator` 驗證碼

未授權使用者私訊你的 Bot 後，直接輸入 6 位數字即可（不需要 `/verify`）。

## 權限差異（完成通知）

1. `owner`：收到兩則訊息（先分享連結，再無水印連結）
2. `operator`：只收到無水印連結

## 基本操作

1. 在 UI 佇列輸入主題（自動）或完整提示詞（手動）
2. 按「開始執行」
3. 生成完成後，結果會同步回傳 Telegram

## 常見問題

1. Bot 無法啟動：通常是 Token 錯誤或失效，請回 BotFather 重建
2. 無法驗證：確認輸入的是 6 位數字，且在 300 秒內
3. 沒有回傳結果：先看 UI 是否仍在執行中，再查 Telegram `/status`
