---
id: work-yoga-class
site: ai
cat: K
title: 瑜伽课音乐
title_en: Music for a Yoga Class
summary: 一节课六十分钟不出现突发事件，音量比曲子重要
summary_en: Sixty minutes without an event; level matters more than the track.
level: standard
tags: [瑜伽, 长段, 音量, 循环]
tags_en: [yoga, long-form, level, loops]
alias: [瑜伽课音乐, 瑜伽配乐, yoga class music, 课堂音乐]
order: 272
tool_kind: guide
tool_vendor: —
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [瑜伽课, 长段音乐, 教室扩声]
tool_verified: 2026-10-31
links:
  - "[[glossary:reverb]]"
  - "[[glossary:lufs]]"
  - "[[glossary:true-peak]]"
instances:
  - mutopia-001412 | 三分钟无鼓氛围，句尾自然消失，适合呼吸段（C1）
  - pdmx-000070 | 慢速弦乐长弧，起伏克制，适合挺尸段（C1）
  - oga-000021 | 游戏洞穴环境，底噪宽、无事件，适合长时间铺底（C1）
sources:
  - NIOSH 噪声暴露指南与 WHO Guidelines for Community Noise 中关于音量与暴露时间的建议。
  - PRS for Music 与 PPL 公开的健身与课程音乐许可说明。
  - 瑜伽课堂制作与播放的公开访谈。
updated: 2026-10-31
---

::: zh
## 一节课的音频交付

六十分钟的瑜伽课，交付一条连续播放列表或一个整段文件，附段落表、音量计划与离线备份。音乐不能有突然的鼓点、铃声、人声喊叫，也不能有忽大忽小的段落。教室扩声多为天花板喇叭，低频容易糊，音量以教练口令能轻松盖过音乐为准。授权要覆盖工作室的商业课程，个人流媒体账号不算。

## 按呼吸分段

第一步把课分成到场、呼吸、体式、平衡、挺尸五段，标出每段分钟数。第二步选素材：到场用稀疏的持续音，体式段保持六十到七十五 BPM 的弱脉冲，平衡段去掉鼓，挺尸段只留长音。第三步拼接，段与段交叉淡化八到十五秒，整条压到 -20 到 -18 LUFS，教室试音后再定最终音量。

## 播放器与音量工具

剪辑在 Ableton Live 或 REAPER 里做，生成用 Suno 或 Udio 的氛围模式。播放用 djay、rekordbox 或带交叉淡化的播放器，手机通知全部关掉。音量用声压计测，教室中间不超过 75 dBA，以教练口令清晰为准。备用文件存本地，不依赖网络。

## 教室里的分段与电平

| 段落 | 时长 | 音乐行为 | 音量 |
|---|---|---|---|
| 到场 | 5–10 分钟 | 单层持续音 | -24 LUFS |
| 呼吸 | 5 分钟 | 无鼓、无旋律钩子 | -22 LUFS |
| 体式 | 30–40 分钟 | 弱脉冲、可循环 | -20 LUFS |
| 平衡 | 5–10 分钟 | 抽掉鼓与低频 | -22 LUFS |
| 挺尸 | 8–12 分钟 | 长音、自然消失 | -24 LUFS |

相邻段落的音量差不超过 3 dB，整节课不做渐强。循环点连续听三遍，接缝处不能有呼吸感。

## 突发音与版权

生成结果里冒出人声哼唱，安静时最明显。低频堆太多，天花板喇叭发出嗡嗡声。前段音量合适，挺尸段显得吵。用个人订阅账号播放，工作室被平台判定商用。播放列表里有一首歌下架，整节课少一段。手机来电或通知音打断挺尸，课前必须开飞行模式。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C3","G3","D4","A4","G4","D4","C4","G3"],"label":"呼吸段的持续音","label_en":"A drone for the breathing section","hint":"听两分钟里有没有突然的音头","hint_en":"Listen for any sudden attack across two minutes"}
```
:::

::: en
## What a class takes

A sixty-minute class needs one continuous playlist or a single long file, plus a segment sheet, a level plan and an offline backup. There can be no sudden drum hits, bells or shouted vocals, and no section that jumps in volume. Most studios use ceiling speakers, where low end turns muddy; set the level so the teacher's voice sits comfortably above the music. The licence must cover commercial classes at the studio. A personal streaming account does not.

## Divide by breath

Split the class into arrival, breathing, asana, balance and savasana, with minutes for each. Choose material accordingly: sparse drones for arrival, a weak pulse at sixty to seventy-five BPM for asana, no drums for balance, long tones only for savasana. Join the sections with eight-to-fifteen-second crossfades, bring the whole file to -20 or -18 LUFS, then set the final level in the room.

## Players and level tools

Edit in Ableton Live or REAPER and generate with Suno or Udio in ambient mode. Play from djay, rekordbox or a player with crossfade, with phone notifications off. Measure with an SPL meter; keep the middle of the room under 75 dBA and let the teacher's voice be the reference. Keep a backup file locally rather than relying on a connection.

## Three lines in the room

| Section | Length | Musical behaviour | Level |
|---|---|---|---|
| Arrival | 5–10 min | One drone layer | -24 LUFS |
| Breathing | 5 min | No drums, no hook | -22 LUFS |
| Asana | 30–40 min | Weak pulse, loopable | -20 LUFS |
| Balance | 5–10 min | Drums and low end removed | -22 LUFS |
| Savasana | 8–12 min | Long tones, natural decay | -24 LUFS |

Adjacent sections stay within 3 dB and the class never builds to a crescendo. Play the loop point three times through; the seam must not breathe.

## Sudden sounds and rights

A hummed vocal appears in the generation and is most obvious in silence. Too much low end makes the ceiling speakers buzz. The level suits the first half and feels loud in savasana. A personal subscription is used for playback and the studio is treated as commercial. One track leaves the playlist and the class loses a section. A phone call or notification breaks savasana, so the device goes into flight mode before class.

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C3","G3","D4","A4","G4","D4","C4","G3"],"label":"A drone for the breathing section","label_en":"A drone for the breathing section","hint":"Listen for any sudden attack across two minutes","hint_en":"Listen for any sudden attack across two minutes"}
```
:::
