---
id: work-slides
site: ai
cat: K
title: 给演示文稿配乐
title_en: Music for Presentations
summary: 音乐只负责开场、换段和收尾，歌词与长旋律都会分心
summary_en: Music only opens, bridges and closes; lyrics and long melodies pull attention away.
level: standard
tags: [演示文稿, 开场, 淡出, 无歌词]
tags_en: [presentation, opening, fades, instrumental]
alias: [演示配乐, PPT 配乐, 演讲音乐, presentation music]
order: 269
tool_kind: guide
tool_vendor: —
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [演示配乐, 会议开场, 音频嵌入]
tool_verified: 2026-10-31
links:
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:dynamics]]"
  - "[[glossary:reference-track]]"
instances:
  - mutopia-001411 | 三分钟钢琴小品，句子短、留白多，讲话时不会抢注意力（C1）
  - aria-039011 | 一百秒的钢琴前奏，句法干净，适合开场与等待（C1）
  - pdmx-001010 | 七分半的连续乐章，长弧可作分段演示的参照（C1）
sources:
  - 微软 PowerPoint 官方支持文档中关于嵌入音频与跨幻灯片播放的说明。
  - 会议演讲与演示制作的公开音频指南。
updated: 2026-10-31
---

::: zh
## 一场演讲需要的音频

给演示文稿配乐，交付的通常不是一整首，而是三段：开场二十到三十秒、换段提示两到四秒、结尾三十到六十秒。长演讲可以在问答环节留一条极轻的循环，但要有随时关掉的开关。所有文件无人声、无歌词，采样率 48 kHz，留三秒尾巴方便淡出。嵌入版与独立播放版各交一份。

## 从时长表开始

第一步把演讲按分钟切开，标出必须换气的三到五个位置，算出每段音乐的长度。第二步做素材：开场用一个动机，换段用同动机的短句，结尾把动机放慢；三段同调，速度差不超过 4 BPM。第三步嵌进 PowerPoint 或 Keynote，设跨幻灯片播放、淡入两秒、淡出三到五秒，逐页试播。

## 演示软件与音频工具

剪辑在 Audacity 或 Adobe Audition 里做，生成用 Suno 或 Udio 的纯音乐模式。Ozone 统一三段响度，iZotope RX 去生成素材的尾噪。PowerPoint 的跨幻灯片播放和 Keynote 的播放列表都要试，嵌入后文件会变大，超过限制就改用链接并随包带上音频。

## 放映前的试听

| 用途 | 长度 | 处理 | 忌讳 |
|---|---|---|---|
| 开场 | 20–30 秒 | 淡入 2 秒 | 有人声、有歌词 |
| 换段 | 2–4 秒 | 硬收或短淡出 | 旋律完整、抢话 |
| 结尾 | 30–60 秒 | 淡出 5 秒 | 突然结束 |
| 问答 | 循环 60 秒 | 音量 -30 LUFS | 节奏强、有鼓 |

在会议室的音响与笔记本自带喇叭各听一遍。讲话时音乐压在人声下 18 dB，换段提示不盖住上一句话的尾字。

## 音乐什么时候该消失

幻灯片翻得比音乐快，说明段落写长了。开场还在响，主讲人已经开始说话。结尾淡出没做完，放映员直接切黑。嵌入的音频在别人的电脑上变成红色叉号。歌词是外语，观众开始听词而不是听内容。授权只覆盖现场，录播上传后收到声明。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","B4","G4","E4","C4"],"label":"开场三十秒的钢琴","label_en":"Thirty seconds of piano for an opening","hint":"听它有没有歌词和抓人的旋律，两样都不该有","hint_en":"Listen for lyrics or a hook; neither belongs here"}
```
:::

::: en
## What a talk actually needs

A presentation rarely needs a whole track. It needs three pieces: twenty to thirty seconds for the opening, a two-to-four-second bridge, and thirty to sixty seconds for the close. A long talk can keep a very light loop under questions, with a switch to kill it instantly. Everything is instrumental and wordless, at 48 kHz, with three seconds of tail for the fade. Deliver an embedded copy and a standalone copy.

## Start with a duration map

Cut the talk into minutes and mark the three to five places where it changes gear; that sets the length of each piece. Build the material from one motif: state it at the opening, compress it into the bridge, slow it for the close. Keep all three in the same key, within 4 BPM. Then place them in PowerPoint or Keynote, set play-across-slides, a two-second fade-in and a three-to-five-second fade-out, and run every slide.

## Presentation software and audio tools

Edit in Audacity or Adobe Audition and generate with Suno or Udio in instrumental mode. Ozone matches the three pieces, iZotope RX removes tail noise from generated files. Test both PowerPoint's play-across-slides and Keynote's playlist. Embedding inflates the file; when it exceeds the limit, link the audio and carry it in the same folder.

## The run-through

| Use | Length | Treatment | Avoid |
|---|---|---|---|
| Opening | 20–30 s | 2 s fade-in | Voices, lyrics |
| Bridge | 2–4 s | Hard stop or short fade | A complete tune that grabs attention |
| Close | 30–60 s | 5 s fade-out | A sudden cut |
| Q&A | 60 s loop | -30 LUFS | Strong pulse, drums |

Listen once on the room system and once on the laptop speakers. Under speech the music stays 18 dB below the voice, and a bridge never covers the last word of the previous sentence.

## When the music should vanish

Slides advance faster than the music, which means a section was written too long. The opening is still playing when the speaker starts. The closing fade is unfinished and the operator cuts to black. An embedded file turns into a red cross on someone else's computer. The lyric is in a language the audience understands, and they follow the words instead of the argument. The licence covers the room only, and an uploaded recording brings a claim.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","B4","G4","E4","C4"],"label":"Thirty seconds of piano for an opening","label_en":"Thirty seconds of piano for an opening","hint":"Listen for lyrics or a hook; neither belongs here","hint_en":"Listen for lyrics or a hook; neither belongs here"}
```
:::
