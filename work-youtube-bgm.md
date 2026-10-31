---
id: work-youtube-bgm
site: ai
cat: K
title: 视频背景乐
title_en: Background Music for Video
summary: 背景乐的任务是不抢戏，还要经得起十分钟重复
summary_en: Background music has to stay out of the way and survive ten minutes of repeats.
level: standard
tags: [视频, 背景乐, 授权, 循环]
tags_en: [video, background, licensing, loops]
alias: [视频背景乐, YouTube 配乐, BGM, youtube bgm]
order: 3
tool_kind: guide
tool_vendor: —
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [视频配乐, 长视频, 授权确认]
tool_verified: 2026-10-30
links:
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:sync-license]]"
  - "[[glossary:stems]]"
instances:
  - oga-000287 | 电子循环靠增减元素维持律动，听层间关系（C1）
  - mutopia-001411 | 三分钟的钢琴小品，短、单声部，适合做段落素材（C1）
  - pdmx-001010 | 一个乐章铺十分钟情绪，长弧最难维持（C1）
sources:
  - 视频平台响度归一与版权声明机制；平台公开说明是主要依据。
  - 背景乐与口播的比例——依据来自视频制作惯例。
updated: 2026-10-30
---

::: zh
## 需求长什么样

一条八到十五分钟的视频要全程铺底，不能盖住口播。观众戴耳机也听手机外放，音乐在小喇叭上仍要有轮廓。频道一旦开了广告，音乐必须能商用，还要避开版权声明。视频按章节推进，音乐要跟着换段，但不能换得突然。片头片尾与正片用同一套素材，听感才连成一条。

## 工具组合

用 Suno 或 Udio 生成无人声版本，Udio 适合多出几个变体做段落。需要唱句时用 ACE Studio。剪辑与段落拼接在 Ableton Live、Logic Pro 或 REAPER 里做。Demucs 处理参考曲，iZotope RX 去噪声，Ozone 统一到平台响度。生成只提供材料，段落关系在时间线上决定。

## 步骤

先按脚本划章节，标出每段的情绪、长度与口播位置。每段生成一到三分钟的循环素材，提示里写明 instrumental。把段落贴到时间线，用两到四秒交叉淡化或留白过渡。口播段把音乐降 6 到 10 dB，中频留给说话。整体听一遍重复感，必要时换配器或删层。母带后导出并填写元数据。

## 验收标准

成片全长与视频一致，片尾留两秒淡出。整体 -14 LUFS，真峰值不高于 -1 dBTP。口播段音乐比人声低 6 到 10 dB。段落切换处的电平差不超过 1.5 dB。全片都没有人声与歌词，策划要求除外。没有版权声明与 Content ID 冲突。授权覆盖频道广告收入。分轨与生成记录保留，文件按章节编号命名。

## 常见返工原因

提示写了 instrumental，仍出现人声切片。同一段循环用满十分钟，观众听腻。段落硬切，鼓点断在半拍。响度做到 -9 LUFS，被平台压回去。风格过于接近某首曲子，收到版权声明。授权不含商业频道，广告开通后下架。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["C4","E4","G4","A4","G4","E4","D4","C4"],"label":"十分钟也站得住的循环","label_en":"A loop that survives ten minutes","hint":"听两遍，第二遍还剩下什么","hint_en":"Listen twice and ask what is left on the second pass"}
```
:::

::: en
## What the brief looks like

An eight-to-fifteen-minute video needs music underneath throughout without covering narration. Viewers listen on headphones and on phone speakers, so the music still needs a shape on a tiny driver. The channel may run ads, which means the music has to be cleared for commercial use and must not trigger a claim. The video moves in chapters, so the music changes with them, but never abruptly. Opening, body and end use one pool of material, or the whole piece stops feeling continuous.

## Tool combination

Generate instrumental versions with Suno or Udio, and use Udio when several variants are needed for sections. ACE Studio covers sung lines. Edit and join sections in Ableton Live, Logic Pro or REAPER. Demucs handles references, iZotope RX removes noise, Ozone sets platform loudness. Generation supplies material; the timeline decides how sections relate.

## Steps

Map chapters from the script and note the mood, length and narration position of each. Generate one to three minutes of loopable material per section, with instrumental stated in the prompt. Place sections on the timeline and join them with a two-to-four-second crossfade or a gap. Under narration, drop the music 6 to 10 dB and leave the midrange to the voice. Listen through once for repetition and change orchestration or remove a layer if needed. Master, export and fill in metadata.

## Acceptance criteria

The finished track matches the video length and fades out over the last two seconds. It sits at -14 LUFS with true peak no higher than -1 dBTP. Under narration the music is 6 to 10 dB below the voice, and level jumps between sections stay under 1.5 dB. There are no vocals or lyrics unless the brief asks for them. No copyright claim or Content ID conflict appears. The licence covers channel advertising revenue. Stems and generation records are kept, and files are named by chapter.

## Common rework causes

The prompt says instrumental and vocal chops still appear. One loop runs for ten minutes and wears out. Sections are hard-cut and the drums stop mid-beat. The mix is pushed to -9 LUFS and the platform turns it down. The style sits too close to a known record and draws a claim. The licence excludes commercial channels, so ads force a takedown.

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["C4","E4","G4","A4","G4","E4","D4","C4"],"label":"A loop that survives ten minutes","label_en":"A loop that survives ten minutes","hint":"Listen twice and ask what is left on the second pass","hint_en":"Listen twice and ask what is left on the second pass"}
```
:::
