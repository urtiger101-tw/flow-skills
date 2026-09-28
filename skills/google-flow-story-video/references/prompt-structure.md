# Prompt Structure For Flow Story Clips

## Character Consistency Block

Use this block in every storyboard and Flow prompt:

```text
保持一致性。Same six anthropomorphic fruit AI characters from the character bible: mango girl, pineapple man, rose-apple lady, small green fruit child, muscular green fruit rider, and elegant pear/lemon lady. Keep identical outfits, fruit textures, accessories, body proportions, facial personalities, and Taiwanese night-market environment.
```

## ChatGPT 2K+ Storyboard Prompt

Before generating images, ask ChatGPT to create a director-style, timecoded storyboard plan. Use the clip duration to define shots, then generate one 2K+ image for each key frame.

```text
請先用導演分鏡表規劃這段 8 秒影片，再依分鏡生成單張 16:9、2K 以上解析度的分鏡圖。

分鏡表格式：
- 時間：0-2s
- 鏡頭：35mm medium shot / 低角度 / 緩慢推近
- 導演敘事：角色正在做什麼、情緒是什麼、觀眾要感受到什麼
- 場景敘事：夜市攤位、燈光、背景人物、道具、氣氛與前後鏡頭如何銜接
- 動作：角色表情、手勢、走位、物件互動
- 一致性：固定角色外觀、服裝、果皮材質、比例、配件、夜市場景

接著為每個 key frame 生成獨立圖片，不要只做拼貼 contact sheet。
```

## Timecoded Director Shot Template

Use this structure for each 8-second Flow/Veo clip:

```text
Clip [number], total duration 8s.

0-2s | 24mm establishing shot | camera slowly pushes into the Taiwanese night-market fruit stall.
Director narrative: introduce the fruit team and the emotional problem of the scene.
Scene narrative: wet street reflections, warm string lights, fruit crates, scooter lights in the background.
Action: characters hold their opening poses, subtle breathing and eye contact.
Continuity: start from storyboard_[N]_2k.png and keep all character details identical.

2-5s | 35mm medium shot | camera tracks from left to right.
Director narrative: reveal the main character reaction and the comic tension.
Scene narrative: keep the same stall geography and background extras.
Action: [specific character] speaks or gestures; other characters react naturally.
Continuity: no costume, prop, scale, or fruit texture changes.

5-8s | 50mm close-up or 85mm portrait close-up | gentle push-in.
Director narrative: end on a clear emotional beat that connects to the next clip.
Scene narrative: lights shimmer behind the character; keep color and weather consistent.
Action: character finishes the spoken line, glance points toward next scene direction.
Continuity: final pose should become the next clip's start or end-frame reference.
```

## Single 2K+ Key Frame Prompt

```text
Create one 16:9 cinematic storyboard frame at 2K or higher resolution.
保持一致性。Use the fixed fruit AI character bible: [paste character consistency block].
Clip [number], key frame at [time range, e.g. 0-2s].
Lens and camera: [35mm medium shot, low angle, slow push-in].
Director narrative: [what the audience should understand emotionally].
Scene narrative: [market geography, lighting, props, background action, continuity].
Action: [specific character blocking, expression, gesture, and interaction].
Taiwanese night market at night, warm string lights, neon signs, wet street reflections, fruit stall details, cinematic 3D animated film still, high detail, no text, no watermark.
```

## Flow Clip Prompt

```text
8-second 1080P 16:9 video, Veo 3.1 Fast. 保持一致性。
Use the selected start frame as the first frame and selected end frame as the final frame.
Keep identical characters, outfits, fruit textures, accessories, proportions, and Taiwanese night-market setting.
Follow this timecoded direction:
0-2s: [lens, camera, director narrative, scene narrative, action].
2-5s: [lens, camera, director narrative, scene narrative, action].
5-8s: [lens, camera, director narrative, scene narrative, action].
Smooth cinematic camera motion, natural character animation, no on-screen text, no watermark.
[Chinese dialogue]
```

## Dialogue Style

- Use Taiwanese Mandarin that sounds casual and spoken.
- Keep each 8-second clip to one short spoken line.
- Put speech in this form: `Character says: "..."` or `角色說：「...」`.
