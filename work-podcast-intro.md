---
id: work-podcast-intro
site: ai
cat: K
title: 播客片头
title_en: A Podcast Intro
summary: 片头是每周复用的模板，人声清楚比音乐好听更重要
summary_en: An intro is a weekly template; clear speech matters more than a pretty bed.
level: standard
tags: [播客, 片头, 人声, 响度]
tags_en: [podcast, intro, voice, loudness]
alias: [播客片头, 节目片头, podcast intro]
order: 2
tool_kind: guide
tool_vendor: —
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [播客, 片头包装, 人声处理]
tool_verified: 2026-10-30
links:
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:mixdown]]"
  - "[[glossary:reference-track]]"
instances:
  - oga-000293 | 菜单循环，听首尾接缝与进入速度（C1）
  - groove-000492 | 短循环素材复用率高，适合做片头床（C1）
  - thesession-015842 | 传统曲调的演唱版本，咬字与呼吸是合成人声的弱点（C1）
sources:
  - 播客响度与交付口径；播客分发平台公开规范是主要依据。
  - 片头结构（口播、标签、收尾）的划分——依据来自节目制作惯例。
updated: 2026-10-30
---

::: zh
## 需求长什么样

一期播客的固定片头通常在二十到四十秒，包含节目名、主播名、一句口号和一段可辨识的音乐标签。片头之后要接得上正片，结尾还要有更短的收尾。节目每周更新，片头每次一样，模板比单条文件更重要。客户还会要求赞助口播版和视频版。

## 工具组合

铺底用 Suno 或 Udio 生成无人声的循环床，需要唱节目名时用 ACE Studio。人声在 Ableton Live、Logic Pro 或 REAPER 里录和修。iZotope RX 处理喷麦、齿音与底噪，Ozone 统一响度。Demucs 只在处理旧素材或参考曲时用，它分不出干净的播客人声。

## 步骤

先写十五到二十五秒的口播稿，念一遍计时。录主播人声，修齿音与呼吸，不改语速。生成两三个循环床，速度与情绪贴近节目基调。把床垫在人声下，做 6 到 9 dB 的侧链或手写自动化。单独做三到五秒的音乐标签，片尾用同素材的短版。所有素材放在一个工程里，命名统一，方便下期替换。统一响度后导出 wav 与 mp3。

## 验收标准

片头长度与约定一致，误差不超过半秒。整段 -16 LUFS，真峰值不高于 -1 dBTP。人声全程清楚，床在人声下低 6 到 9 dB。音乐标签三到五秒，可单独抽出复用。单声道检查不塌。片头文件与整集文件都要能独立播放。授权覆盖节目、赞助口播与视频版。工程与模板留给下一期。

## 常见返工原因

床太满，人声被压。片头超过四十秒，听众直接跳过。主播名读错，只能重录。每期响度不同，连播时音量忽大忽小。音乐标签和正片音乐不是一套。授权只覆盖非商业，接赞助后整条重做。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q e e q q e e","bpm":92,"label":"人声下面的循环床","label_en":"A loop bed under speech","hint":"听床的密度，留出说话的位置才算合格","hint_en":"Hear the density; a bed is right when speech still has room"}
```
:::

::: en
## What the brief looks like

A fixed podcast intro runs twenty to forty seconds and carries the show name, the host name, one line of copy and a recognisable musical tag. It has to lead into the episode and end with a shorter outro. The show updates weekly and the intro stays the same, so a template matters more than a single file. Clients also ask for a sponsored-read version and a video version.

## Tool combination

Build the bed with Suno or Udio as an instrumental loop, and use ACE Studio when the show name is sung. Record and edit voice in Ableton Live, Logic Pro or REAPER. iZotope RX handles plosives, sibilance and room noise, Ozone sets loudness. Demucs is for old material or references, not for rescuing a host recording; it does not return a clean podcast voice.

## Steps

Write fifteen to twenty-five seconds of copy and read it against a clock. Record the host, repair sibilance and breaths, and leave the pacing alone. Generate two or three loop beds whose tempo and mood fit the show. Sit the bed under the voice with 6 to 9 dB of ducking, by sidechain or drawn automation. Make a separate three-to-five-second tag and a shorter outro from the same material. Keep every asset in one session with one naming scheme, so next week is a swap rather than a rebuild. Set loudness once and export wav and mp3.

## Acceptance criteria

The intro matches the agreed length within half a second. The whole segment sits at -16 LUFS with true peak no higher than -1 dBTP. Speech stays clear with the bed 6 to 9 dB below it. The tag runs three to five seconds and can be lifted out on its own. A mono check does not collapse. The intro file and the full episode each play on their own. The licence covers the show, sponsored reads and video. The session and template are handed over for the next episode.

## Common rework causes

The bed is too busy and presses on the voice. The intro passes forty seconds and listeners skip it. The host name is mispronounced and the take is unusable. Loudness drifts between episodes, so a binge listen jumps in volume. The tag and the episode music come from different worlds. The licence covers non-commercial use only and a sponsor forces a rebuild.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q e e q q e e","bpm":92,"label":"A loop bed under speech","label_en":"A loop bed under speech","hint":"Hear the density; a bed is right when speech still has room","hint_en":"Hear the density; a bed is right when speech still has room"}
```
:::
