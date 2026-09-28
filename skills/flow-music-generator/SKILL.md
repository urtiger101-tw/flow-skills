---
name: flow-music-generator
description: Use Google Flow Music in the user's connected Chrome session to create, refine, and download instrumental tracks or songs from prompts. Use when Google Flow Music or flowmusic.app is requested; do not route these requests to Flow TV or Suno.
---

# Google Flow Music 音樂生成

## 操作

1. 開啟 `https://www.flowmusic.app/`，沿用 Codex extension 已連線的 Chrome 工作階段。Flow Music 與 Flow 影片是不同站點；若目前顯示 `Log in`，先按目前站點流程確認可用登入狀態。遇到新 OAuth 權限、服務條款或購買畫面時，依實際內容請使用者處理必要步驟。
2. 確認使用者要純配樂或有人聲歌曲、語言、風格、情緒、樂器、節奏、時長、版本數與交付格式。若是旁白背景，提示詞要明確寫 `instrumental, no vocals, no lyrics`，並讓編曲保留人聲空間。
3. 在 `New session` 輸入包含曲風、編制、速度、結構與結尾的提示詞。圖片或音訊參考只能使用使用者指定的素材；上傳前核對檔案與帳號。送出前查看 UI 顯示的點數／輸出數。
4. 獲得授權的生成請求送出一次，等待歌曲結果並試聽。要修改時在該歌曲或 session 中描述具體差異，避免重做已有的滿意版本。若送出結果不明，先查看 `Songs` 與 session 紀錄。
5. 從 `Songs` 的 `More → Download` 下載選中的版本與格式；確認檔案存在、可解碼、長度及是否含預期人聲。提供歌曲連結時不要代替本機音檔；若要求公開發布，另依使用者的分享範圍操作。

## 參考

- 配樂與有人聲歌曲提示詞範例見 [references/examples.md](references/examples.md)。
- Google 官方：[開始使用 Flow Music](https://support.google.com/flow/answer/17083868?hl=en)、[建立及下載歌曲](https://support.google.com/flow/answer/17084348?hl=en)。
