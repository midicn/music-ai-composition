---
id: quantization-of-generated-parts
site: ai
cat: C
title: 生成结果的量化
title_en: Quantizing Generated Parts
summary: 量化只修对不齐的音符，整轨全量量化会把演奏感一起修没
summary_en: Quantise only the notes that miss the grid; a blanket pass removes the playing along with the error.
level: standard
tags: [量化, 网格, 律动, 强度]
tags_en: [quantization, grid, groove, strength]
alias: [对网格, 量化强度, quantize]
order: 6
links:
  - "[[glossary:tempo]]"
  - "[[glossary:rubato]]"
  - "[[glossary:midi-protocol]]"
instances:
  - groove-000013 | 116 BPM 爵士放克鼓组，反拍容易被拉到正拍（C1）
  - abcmisc-000179 | Garofitsa 吉格舞曲，六八拍重音要成组（C1）
  - atepp-000367 | 格里格挪威进行曲，规整节奏本来就不需要量化（C1）
  - atepp-000501 | 李斯特夜曲即兴，自由速度一旦量化就没了（C1）
sources:
  - 量化的网格选择与强度设置，依音序器公开文档核对，未抄原文
  - 量化对律动的影响，依制作实践通识核对，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

生成的 MIDI 常常差一点点在格子上，听起来拖，或者和其他轨对不齐。全量量化能修好这个问题，也顺手把演奏感一起修没。更麻烦的是网格选错，量化之后重音跑到反拍上，比量化之前更难听。还有一种情况是整段都不齐，那不是量化问题，是速度或起点没对齐。

## 原理

量化是把音符起点吸到最近的网格点，强度决定吸多少。百分之百会消除所有微时序差异，五成到七成通常既能对齐又保留感觉。网格必须跟音乐匹配，三连音、六八拍、摇摆八分不能用十六分网格硬套。量化只改起点，不改时值与力度，所以它修不了音太短这类问题。量化也会把琶音的滚奏压到同一格，几个音挤在一起，听感就变硬。

## 做法

先听再量化，别一导入就全选。只量化明显不对的音符，用软件里的量化选定音符。网格按拍号与细分选，摇摆段落用三连音网格，或者干脆不量化。强度从六成开始，每次加一成听变化。量化完把重音手动提前或推后几毫秒，把律动找回来。鼓和贝斯可以量化得重一些，旋律与独奏要轻。量化前后各存一版，A/B 时才能确认是改善了还是只是变整齐了。

## 听什么

在 116 BPM 的爵士放克鼓组里，听反拍有没有被拉到正拍上。在 Garofitsa 吉格舞曲里，听六八拍的重音是否还成组。在格里格的挪威进行曲里，听规整的节奏本来就不需要量化，量化只是让它更死。在李斯特的夜曲即兴里，听自由速度一旦被量化会失去什么。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"T t T t T t T t","bpm":116,"label":"摇摆八分","label_en":"Swung eighths","hint":"量化到十六分网格后，这种摆动会被抹平","hint_en":"Quantised to a sixteenth grid, this swing flattens out"}
```
:::

::: en
## The problem

Generated MIDI often sits slightly off the grid, so it drags or refuses to line up with other tracks. A blanket quantise fixes that and removes the playing at the same time. Worse, the wrong grid can push accents onto the offbeat, which sounds less musical than the original error. When a whole passage is off, the cause is tempo or start point, not quantisation.

## How it works

Quantising pulls each note onset to the nearest grid point, and strength decides how far. Full strength erases every microtiming difference; fifty to seventy percent usually aligns without flattening. The grid has to match the music, because triplets, six-eight and swung eighths do not fit a sixteenth grid. Quantising changes onsets only, not lengths or velocity, so it cannot fix notes that are too short. It also collapses rolled chords and arpeggios onto one point, which hardens the attack.

## Practice

Listen before quantising and never select all on import. Quantise only the notes that are clearly wrong, using quantise selected notes. Choose the grid by meter and subdivision, use a triplet grid for swing, or skip it entirely. Start at sixty percent strength and add ten percent at a time while listening. Afterwards nudge accents a few milliseconds early or late to recover the feel. Drums and bass can take heavier settings, melody and solos far lighter. Keep a copy before and after, so an A/B tells you whether it improved or merely tidied, and check the result against the other tracks rather than alone.

## What to listen for

In the 116 BPM jazz-funk kit, whether the offbeats get pulled onto the beat. In the Garofitsa jig, whether the six-eight accents still group correctly. In Grieg's Norwegian march, how the already regular rhythm needs no quantising, so a pass only makes it stiffer. In Liszt's impromptu nocturne, what free tempo loses once it is snapped to a grid.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "T t T t T t T t", "bpm": 116, "label": "Swung eighths", "label_en": "Swung eighths", "hint": "量化到十六分网格后，这种摆动会被抹平", "hint_en": "Quantised to a sixteenth grid, this swing flattens out"}
```
:::
