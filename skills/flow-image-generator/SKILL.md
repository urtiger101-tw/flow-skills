---
name: flow-image-generator
description: Use Google Flow in the user's connected Chrome session to generate or edit standalone images, including reference images and frames for later video work. Use for Flow or Nano Banana image requests; Flow TV browsing and video generation belong to other skills.
---

# Google Flow 圖片生成

## 操作

1. 在已連線的 Codex Chrome extension 工作階段開啟 `https://flow.google.com/`，沿用使用者目前的登入帳號。Flow TV (`https://labs.google/flow/tv`) 是瀏覽作品的入口；若使用者指定其中一段作品，可從可見的 `Reuse Prompt` 取得靈感，再到 Flow 專案修改提示詞。
2. 確認專案、圖片用途、比例、張數、參考圖與交付路徑。未指定時，選與用途相符的比例及最少輸出數；不要假設每張都是 16:9。
3. 在專案提示框選 `Image`，以目前 UI 顯示的模型、比例、輸出數與點數為準。把主體、場景、構圖、光線、風格及需要避免的元素寫成清楚提示詞。參考圖只在使用者提供或指定時上傳。
4. 使用者要求實際生成時，核對設定後送出一次。送出後若逾時或畫面不明，先查看專案的生成紀錄與資產，不盲目重送。若只是要求構思或提示詞，停在可審閱的草稿。
5. 開啟結果檢查主體、比例、文字與參考一致性；必要時用 Flow 的編輯工具局部修改。下載選中的實際圖片，確認檔案存在、可開啟及尺寸符合要求；回報使用的模型／設定及實際檔案路徑。不要把 UI 中出現縮圖當作本機交付。

## 參考

- 需要可直接修改的構圖與修圖範例時讀 [references/examples.md](references/examples.md)。
- Google 官方：[建立與編輯圖片](https://support.google.com/flow/answer/16729550?hl=en)、[管理專案與資產](https://support.google.com/flow/answer/16935308?hl=en)。
