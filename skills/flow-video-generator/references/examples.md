# Flow 影片提示詞範例

先以目前 UI 選定模型、比例、長度及輸出數；提示詞中的秒數不能取代實際設定。範例沒有實際送出生成。

## 1. 文字生成影片

```text
16:9 cinematic video. A quiet Taipei night market just after rain. A vendor opens a small paper lantern, and warm light spreads across the wet stone pavement. Start with a wide establishing shot, then a slow dolly-in to the vendor's hands. Natural human motion, realistic reflections, restrained color palette, one continuous shot, no on-screen text or subtitles. Ambient street sounds only; no music.
```

檢查：主體動作連續、鏡頭沒有突跳、音訊符合「只有環境聲」。

## 2. 起始與結束影格

前提：使用者提供兩張已確認的影格，並在 Flow `Frames` 中分別放入 start/end slot。

```text
Use the selected start image as the first frame and selected end image as the final frame. Between them, the camera slowly pans right while the same character walks toward the lantern stall. Preserve the character's outfit, face, location geometry, and lighting continuity. Smooth physical motion, no extra characters, no cuts, no text.
```

檢查：首尾影格都對得上，途中人物、服裝和場景未無故改變。

## 3. 影片內台灣華語對白

```text
Medium close-up of a shopkeeper in a quiet tea shop. She looks toward the customer and says in natural Taiwanese Mandarin:「今天雨大，先喝杯熱茶再走吧。」 Calm, warm delivery, visible mouth movement synchronized with the spoken line. Soft room ambience, no background music, no subtitles or on-screen text.
```

若使用 `Voices`，先確認當前模型支援且已選 `Ingredients`；影片內對白不等於獨立 TTS 音檔。
