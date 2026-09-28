# Flow 提示詞運鏡工作方式

## 流程

1. 先規劃小故事、角色設定與每段 0–2、2–5、5–8 秒的動作。
2. 生成各段獨立的高解析分鏡圖片，下載後查驗尺寸、角色與構圖。
3. 在 Flow 選影片模式，依當下 UI 確认模型、長度、比例、數量與點數。已實跑設定為 Veo 3.1 Fast、16:9、8 秒、x1。
4. 用對應圖片作初始影格。需要精確結尾時才另加結束影格；結尾要自由拉回或升高時，可以只指定初始影格。
5. 在提示詞寫出攝影機方向、時間順序、焦點及角色動作。確認提交一次；若結果不明，先檢查生成狀態，不重複扣點。
6. 下載原始影片，以 ffprobe 檢查尺寸、時長與音軌，再以逐秒取樣檢查真正的場景透視變化、推近與回拉。
7. 後製只負責串接、淡接、字幕與聲音；指定使用 Flow 運鏡時，不以裁切縮放取代生成運鏡。

## 已實跑的運鏡範例

主題為動物園裡的小猴子、老先生與彩虹；使用對應圖片作初始影格。以下整理實際使用的鏡頭段落，角色與場景應依任務改寫。

### 1. 發現葉尖水珠

```text
8-second single continuous cinematic 3D animated shot. Match the uploaded first frame and preserve the characters.
0-2 seconds physically truck RIGHT along the pond, foreground leaves sliding past with clear background parallax.
2-5 seconds smoothly DOLLY IN toward the curious monkey and sparkling droplet, rack focus from the droplet to the monkey eyes.
5-8 seconds DOLLY BACK OUT to a wide shot as the monkey points toward the pond and the elderly farmer gently follows its gaze.
Real camera translation through the 3D scene, visible changing perspective, smooth eased movement. Stable anatomy, consistent clothes, warm morning light. No cuts, text or logos.
```

### 2. 大象噴出彩虹

```text
0-2 seconds glide UPWARD from the low pond-level view toward the elephant trunk, real pedestal/crane movement.
2-5 seconds smoothly DOLLY IN toward the elephant face and spraying trunk, droplets sparkle in focus and the rainbow brightens.
5-8 seconds smoothly DOLLY BACK while trucking LEFT to reveal the elderly farmer and the delighted monkey watching the complete rainbow across the pond.
Strong natural parallax, changing 3D perspective, smooth gentle motion suited to a children story. One uninterrupted take.
```

### 3. 朋友一起分享

```text
0-2 seconds smoothly truck LEFT, keeping the monkey as focal subject while nearby railing and leaves shift with strong parallax.
2-5 seconds DOLLY IN to the monkey joyful face and waving hand; the elderly farmer smiles and waves back.
5-8 seconds slowly DOLLY BACK and CRANE UP to reveal the entire pond, rainbow and all three friends in a beautiful wide ending composition.
Genuine camera movement through three-dimensional space and changing perspective, gentle smooth easing. Keep stable anatomy and character design.
```

指定秒數是生成指示；模型不一定精確遵循每個時間點。應以原片驗收，不只以提示詞存在判定成功。

## 下載、版本與聲音

- 編輯圖片可能建立同一 Flow 資產的新修訂。需保留舊圖時先下載，再進行編輯；不同本機圖片重新上傳為獨立影格可避免誤用最新修訂。
- 「下載完成」提示不代替本機檔案查驗。必須確定檔案存在且可解碼。
- 「1080p 已提升畫質」與原生 1080p 應區分；報告原片與輸出尺寸。
- 無聲回傳若會改變持續性設定，需有該使用者對該設定的授權；本文件不代表其他使用者已授權。
- 以獨立版本資料夾保存 images、clips、audio、qa、final、提示詞與 manifest。
- 合成後確認影片與音訊長度，執行全片解碼，檢查字幕字形與音量峰值。若混合濾鏡造成音軌截斷，可先獨立製成固定樣本數的 PCM 旁白，再混音與封裝。
