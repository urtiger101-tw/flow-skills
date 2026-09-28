---
name: flow-video-generator
description: Use Google Flow in the user's connected Chrome session to generate and download video clips from text, start/end frames, or visual references. Use for general Flow or Veo video requests; use the existing google-flow-story-video skill for its specialized multi-clip storyboard pipeline.
---

# Google Flow 影片生成

## 操作

1. 在 Codex Chrome extension 連線的原有 Chrome 帳號開啟 `https://flow.google.com/`，選擇使用者指定的專案或建立新專案。Flow TV 只供觀賞及尋找範例；其 `Reuse Prompt` 可作為新影片提示詞的起點。
2. 記下交付要求：主題、動作、場景、鏡頭、比例、時長、張數、是否有聲、參考素材與儲存位置。在提示框選 `Video`，依目前 UI 確認模型、長度、比例、輸出數、解析度及每次生成的點數；不要把舊模型設定硬套到新 UI。
3. 純文字影片直接描述可見動作和鏡頭運動；需要一致性時用 `Ingredients` 加參考；指定起迄畫面時用 `Frames` 放入 start/end frame。若要在影片中維持角色聲線，檢查當前模型是否支援 `Voices`，並依 UI 限制設定。上傳前核對素材及目的。
4. 使用者要求生成時只提交一次，記錄結果卡或 job 狀態；結果不明先查專案，不重複扣點生成。檢查成片內容、時長、畫幅和音訊；用 Flow 的下載選單取得實際影片。
5. 驗證本機影片存在、可播放，並用 `ffprobe` 或等價工具讀取解析度、長度、影片與音訊串流。只有看到實際影片檔才回報本機交付成功；在頁面顯示「已提交」只代表工作已送出。

## 參考

- 提示詞、起迄影格與有聲影片範例見 [references/examples.md](references/examples.md)。
- Google 官方：[建立影片](https://support.google.com/flow/answer/16353334?hl=en)、[模型與支援功能](https://support.google.com/flow/answer/16352836?hl=en)、[下載資產](https://support.google.com/flow/answer/16935308?hl=en)。
