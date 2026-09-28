---
name: google-flow-story-video
description: Operate Google Flow via the Codex Chrome extension to generate consistent 8-second 1080p Veo 3.1 Fast story-video clips from high-resolution ChatGPT storyboard frames, including x1 output count, 16:9 framing, first/last-frame continuity, and download verification. Use when the user asks to use Flow, labs.google/fx, Veo, or Google Flow as an alternative to Grok Imagine for storyboard-to-video production.
---

# Google Flow Story Video

Use this skill for real Google Flow video generation. Do not replace failed Flow output with a local still-image animatic unless the user explicitly asks for a preview.

## Core Rules

- Use the Codex Chrome extension browser session for logged-in Google Flow.
- Generate or upscale storyboard frames to 2K or higher before importing them into Flow.
- Use `Veo 3.1 - Fast`, video mode, 16:9, 1080p when available, and output count `1x`.
- Each Flow job should produce exactly one 8-second clip unless the user asks otherwise.
- Use two frame references whenever the Flow UI supports it:
  - Start frame: the current clip opening frame.
  - End frame: the intended last frame or the next storyboard frame.
- Before pressing submit, hover or move to the circular arrow to the right of the `video 1x` chip and confirm it behaves like a clickable pointer target. Do not click the text chip as if it were submit.
- After generation, download the real Flow video and verify it with `ffprobe`.

## High-Resolution Storyboards

1. Use ChatGPT web image generation to create individual storyboard frames at 2K+ resolution.
2. Before image generation, create a director-style timecoded storyboard plan:
   - Use the target clip duration to define shots, for example `0-2s`, `2-5s`, and `5-8s`.
   - For each time range, specify lens, camera movement, subject blocking, action, emotion, scene narrative, lighting, and continuity notes.
   - Example lens details: `24mm establishing`, `35mm medium shot`, `50mm close-up`, `85mm portrait close-up`, `macro insert`.
   - Use the director plan as the source for each 2K+ storyboard image prompt.
3. Keep a fixed character bible in every prompt:
   - Same six anthropomorphic fruit AI characters.
   - Same outfits, fruit textures, proportions, accessories, and Taiwanese night-market setting.
   - Same cinematic 3D animation style, lighting, camera language, and color continuity.
4. Generate all frames as separate images when possible, not only a contact sheet.
5. Download each frame and name it predictably:
   - `storyboard_01_2k.png`
   - `storyboard_02_2k.png`
   - etc.
6. Prepare upload copies if Flow rejects large files, but keep them high quality:
   - Prefer 1920x1080 or higher for 16:9.
   - Use JPEG quality 92+ only for upload copies.

See `references/prompt-structure.md` for prompt blocks.

## Flow Setup

1. Open `https://labs.google/fx/zh/tools/flow` in the Codex Chrome extension session.
2. Create or open the target project.
3. Switch from image mode to video mode if the project opens on Nano Banana.
4. Open the model/settings chip and set:
   - Mode: video.
   - Model: `Veo 3.1 - Fast`.
   - Aspect ratio: `16:9`.
   - Output count: `1x`.
   - Resolution: `1080p` if the UI exposes it.
   - Duration: `8 seconds` if the UI exposes it.
5. If duration or resolution controls are not visible, state the request explicitly in the prompt and verify the downloaded file afterward.

## Frame Upload And Assignment

1. Upload or paste the start and end storyboard frames.
2. Wait until both uploads finish and the thumbnails are visible in the project media grid.
3. In frame mode, assign both reference slots:
   - Click the start slot, choose the start frame thumbnail.
   - Click the end slot, choose the end frame thumbnail.
4. If the UI labels are in Simplified Chinese:
   - The "start" label means start frame.
   - The "end" label means end frame.
   - The swap-horizontal button swaps the two frame references.
5. If the create button remains disabled, re-open the frame picker and confirm both frame slots contain thumbnails.

## Prompt Structure

Use a compact prompt so the Flow text editor accepts it cleanly:

```text
8-second 1080P 16:9 video, Veo 3.1 Fast. Keep consistency.
Use the selected start frame as the first frame and selected end frame as the final frame.
Keep the same six anthropomorphic fruit AI characters, outfits, fruit textures, proportions, accessories, and Taiwanese night-market setting.
Cinematic 3D animation, neon lights, wet street reflections, smooth camera push-in, lively natural motion, no on-screen text, no watermark.
[Chinese dialogue if needed; load references/prompt-structure.md for examples.]
```

When Chinese speech is desired, use natural Taiwanese Mandarin phrasing, for example:

```text
Mango girl says: "[short Taiwanese Mandarin line]"
```

## Submitting Correctly

1. Fill the prompt using real typing or paste followed by a small keyboard edit, so Flow's editor state updates.
2. Confirm the `video 1x` chip is visible.
3. Locate the circular submit arrow immediately to the right of the `video 1x` chip.
4. Move or hover onto the arrow and confirm the cursor target is the clickable arrow, not empty padding or the settings chip.
5. Click once. If nothing happens:
   - Do not repeatedly click random coordinates.
   - Re-check that both frames are assigned.
   - Re-check that the prompt exists in Flow's editor state.
   - Re-hover the arrow and click the center of the arrow icon.
6. After successful submission, wait for generation. Flow can be slow; wait in 60-120 second intervals before declaring a stall.

## Download And Verification

1. When the generated video appears, open its result page or card.
2. Use Flow's download menu/button to download the real video file.
3. Rename the file into a deterministic folder, for example:
   - `clips_flow/flow_clip_01.mp4`
4. Run `ffprobe` and record:
   - duration,
   - width,
   - height,
   - codec,
   - audio presence.
5. If the file is not 1080p or not about 8 seconds, look for Flow's quality/download option. If none is available, report the actual verified media properties.

## Quality Gate

- Do not call the Flow test successful until a real downloaded video exists.
- Do not merge or subtitle Flow clips until each clip is verified.
- Use ASS subtitles for final bilingual output. Keep the combined subtitle block under one-sixth of frame height, with English smaller than Chinese.
