---
id: common-mix-problems-ai
site: ai
cat: D
title: 常见混音问题
title_en: Common Mix Problems
summary: 闷、刺、飘、抽、平，五种症状各有先动的那一下
summary_en: Dull, harsh, unstable, pumping, flat, five symptoms and the first move for each.
level: standard
tags: [诊断, 低频堆积, 齿音, 抽吸]
tags_en: [diagnosis, low-mid build-up, harshness, pumping]
alias: [混音诊断, 常见问题, mix troubleshooting]
order: 10
links:
  - "[[glossary:eq]]"
  - "[[glossary:compressor]]"
  - "[[glossary:phase-check]]"
instances:
  - cyberhymnal-003612 | 管风琴赞美诗，持续音最能暴露 200 到 500 Hz 的堆积（C1）
  - atepp-000239 | 肖斯塔科维奇第十号赋格，高把位密集音最容易刺耳（C1）
  - groove-000007 | 65 BPM 摇滚鼓组，听压缩是否让每一拍都往下坐（C1）
  - atepp-005385 | 拉威尔《绞刑架》，钟声定位是否稳定，飘先从持续音开始（C1）
sources:
  - 混音症状与首要动作的对应，依混音诊断通识核对，未抄文本
  - Symptom-to-first-move mapping, based on general mix diagnosis practice, no text copied
updated: 2026-10-30
---

::: zh
## 问题

AI 混音出问题，症状通常只有几个。低频闷、高频刺、声像飘、压缩抽、整体平。每个症状背后有几种常见原因，先动哪一下，决定了要修多久。下面按症状给出第一动作，每一条都能在总线上立刻验证。

## 原理

闷多半是 200 到 500 Hz 堆积，来源是铺底与贝斯的重叠，不是缺高频。刺多半是 2 到 5 kHz 过多，来源是饱和、限幅和人声齿音。声像飘来自相位不一致或左右混响不同。抽吸来自压缩器释放太慢或侧链过深。整体平来自动态被提前压掉。症状会互相伪装，闷可能是相位抵消，刺可能是限幅失真，先做一次单声道与旁通对照，再判断原因。判断顺序比判断本身更重要，先排除相位与电平，再动音色。

## 做法

五种症状，各给一个第一动作。

- 闷，先在单声道里 solo 贝斯与铺底，把其中一个高通到 120 Hz 以上，再决定是否窄切 300 Hz
- 刺，先查饱和与限幅，把增益衰减降 1 dB，再对人声做 3 到 6 kHz 的动态削减
- 飘，翻极性、对齐时间、把混响发送改成单声道
- 抽，把释放调到 200 ms 以内，或把侧链深度减半
- 平，先写音量自动化，再考虑压缩

如果两个动作之后症状还在，停下来重听编曲，很多问题在素材本身，插件只能掩盖。每次只改一个变量，改完回到整体听十秒。

## 听什么

在管风琴赞美诗里，听低频是否糊成一块，持续音最能暴露堆积。在肖斯塔科维奇的赋格里，听高把位密集音是否刺耳。在 65 BPM 摇滚鼓组里，听压缩是否让每一拍都往下坐。在拉威尔《绞刑架》里，听钟声的定位是否稳定，飘往往先从持续音开始。四处都是先确认症状，再动手。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s q s s s s s s s q q q q","bpm":100,"label":"抽吸的节奏感","label_en":"The feel of pumping","hint":"听每一拍是否都被压下去又弹回来","hint_en":"Hear whether every beat is pushed down and springs back"}
```
:::

::: en
## The problem

AI mixes fail in a handful of ways. Dull lows, harsh highs, an unstable image, pumping compression, an overall flatness. Each symptom has a few usual causes, and the first move decides how long the repair takes. The moves below can each be checked immediately.

## How it works

Dullness is usually a 200 to 500 Hz pile-up from pad and bass overlapping, not a lack of treble. Harshness is usually too much between 2 and 5 kHz, coming from saturation, limiting and sibilance. An unstable image comes from inconsistent phase or mismatched left and right reverb. Pumping comes from a slow compressor release or too much sidechain. Flatness comes from dynamics being removed early. Symptoms disguise each other, since dullness can come from phase cancellation and harshness from limiter distortion, so run a mono check and a bypass comparison before naming the cause. Order matters as much as the diagnosis, so rule out phase and level before touching tone.

## Practice

Five symptoms, one first move each.

- Dullness, solo bass and pad in mono, high-pass one of them above 120 Hz, then decide whether a narrow cut at 300 Hz is still needed
- Harshness, check saturation and limiting, lower gain reduction by 1 dB, then apply a dynamic cut at 3 to 6 kHz on the vocal
- An unstable image, flip polarity, align timing, and make the reverb send mono
- Pumping, set release under 200 ms or halve the sidechain depth
- Flatness, write volume automation before considering compression

If the symptom survives two moves, stop and listen to the arrangement, since many problems live in the material and plugins only hide them. Change one variable at a time and return to the full mix for ten seconds.

## What to listen for

In the organ hymn, hear whether the low end has become one lump, since sustained notes expose a pile-up best. In Shostakovich's fugue, hear whether the dense high register turns harsh. In the 65 BPM rock groove, hear whether compression makes every beat sit down. In Ravel's Le gibet, hear whether the bell stays in place, because instability starts with sustained tones. In all four, confirm the symptom before touching anything.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s q s s s s s s s q q q q","bpm":100,"label":"The feel of pumping","label_en":"The feel of pumping","hint":"Hear whether every beat is pushed down and springs back","hint_en":"Hear whether every beat is pushed down and springs back"}
```
:::
