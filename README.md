# Flow Skills for Codex

透過已登入的 Chrome 與 Codex Chrome extension 操作 Google Flow，製作圖片、影片、歌曲與多段故事影片。

## 包含技能

| 技能 | 用途 | 參考範例 |
|---|---|---|
| [flow-image-generator](skills/flow-image-generator/SKILL.md) | Flow 圖片生成與參考圖編修 | [圖片範例](skills/flow-image-generator/references/examples.md) |
| [flow-video-generator](skills/flow-video-generator/SKILL.md) | 文字／影格生成影片與下載驗證 | [影片範例](skills/flow-video-generator/references/examples.md) |
| [flow-music-generator](skills/flow-music-generator/SKILL.md) | Flow Music 歌曲與配樂 | [音樂範例](skills/flow-music-generator/references/examples.md) |
| [google-flow-story-video](skills/google-flow-story-video/SKILL.md) | 多段分鏡、角色一致性與故事影片 | [導演分鏡範例](skills/google-flow-story-video/references/prompt-structure.md) |

## 使用前提

- Codex 可使用已連線的 Chrome extension 瀏覽器工具。
- 使用者可登入對應的 Flow／Flow Music 服務，且具備生成權限與足夠額度。
- 媒體檢查使用 FFmpeg / ffprobe；合成字幕時需安裝合適的中文字型。
- 技能是操作指引，不包含 API 金鑰、登入狀態、瀏覽器設定檔或影片素材。

## 安裝

下載或 clone 此儲存庫，把 `skills/` 內需要的技能資料夾複製到 Codex 的技能目錄，預設為 `~/.codex/skills/`。若設定了 `CODEX_HOME`，使用該目錄下的 `skills/`。遇到同名既有技能先比較或備份，再決定替換；重新載入 Codex 技能後使用。

範例請求：

> 使用 flow-image-generator 製作 3 張一致角色的動物園分鏡圖，再使用 flow-video-generator 生成每段 8 秒的影片。依 docs/prompt-camera-workflow.md 在 Flow 提示詞中安排側移、推近與拉回。

## 本次實作經驗

請搭配 [Flow 提示詞運鏡工作方式](docs/prompt-camera-workflow.md)。先完成分鏡圖片，再讓 Flow 生成攝影機移動，後製處理串接、聲音與字幕。模型、比例、解析度、時長及額度以目前 UI 為準。

`google-flow-story-video` 是較早的專案技能，其六位水果角色、夜市場景、ChatGPT 圖片來源及首尾影格安排，應依使用者當次要求調整。這次封存保留原始技能內容，未修改已安裝版本。

## 版本與驗證

封存日期：2026-09-28。共 4 個技能、12 個來源檔，SHA-256 記錄於 [source-checksums.json](source-checksums.json)，複製後與本機來源逐檔比對。

本次故事實跑：3 張 2752×1536 JPG，3 段 Veo 3.1 Fast 影片；原片為 1280×720、24 fps、8 秒，透過逐秒取樣確認運鏡與角色。合成新篇 23.2 秒，影片與音訊均完整解碼。這些驗證反映當次環境，不保證未來 UI 或所有帳號可用功能相同。

此儲存庫僅封存技能與文件；未附專案圖片、影片、私人專案連結或帳號憑證。
