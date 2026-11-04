---
id: "quantization-of-generated-parts"
site: "ai"
cat: "C"
title: "生成结果的量化"
title_en: "Quantizing Generated Parts"
summary: "量化只修对不齐的音符，整轨全量量化会把演奏感一起修没"
summary_en: "Quantise only the notes that miss the grid; a blanket pass removes the playing along with the error."
level: "standard"
tags: ["量化", "网格", "律动", "强度"]
tags_en: ["quantization", "grid", "groove", "strength"]
alias: ["对网格", "量化强度", "quantize"]
order: 6
links: ["[[glossary:tempo]]", "[[glossary:rubato]]", "[[glossary:midi-protocol]]"]
instances: ["groove-000013", "abcmisc-000179", "atepp-000367", "atepp-000501"]
sources: ["https://www.ableton.com/en/live-manual/11/editing-midi-notes-and-velocities/", "量化的网格选择与强度设置（音序器公开文档）。", "量化对律动的影响，参考制作实践惯例。"]
updated: "2026-11-04"
---

::: zh
## 难在哪

生成的 MIDI 常常差一点点在格子上，听起来拖，或者和其他轨对不齐。全量量化能修好这个问题，也顺手把演奏感一起修没。更麻烦的是网格选错，量化之后重音跑到反拍上，比量化之前更难听。还有一种情况是整段都不齐，那不是量化问题，是速度或起点没对齐。

## 工作机制

量化是把音符起点吸到最近的网格点，强度决定吸多少。对选定音符使用百分之百强度，通常会把其起点移到目标网格；五成到七成可作为试听起点，是否合适仍取决于素材与软件设置。网格必须跟音乐匹配，三连音、六八拍、摇摆八分不能用十六分网格硬套。量化可作用于起点、终点或两者，具体取决于软件选项；终点量化会改变时值。起点校正不会自动修好力度、踏板或所有音符长度问题，应分别检查。量化也会把琶音的滚奏压到同一格，几个音挤在一起，听感就变硬。

## 从哪开始

先听再量化，别一导入就全选。只量化明显不对的音符，用软件里的量化选定音符。网格按拍号与细分选，摇摆段落按实际摇摆比例选择 groove；只有接近三连音分配时才适合三连音网格。也可以不量化。强度从六成开始，每次加一成听变化。量化完把重音手动提前或推后几毫秒，把律动找回来。鼓和贝斯可以量化得重一些，旋律与独奏要轻。量化前后各存一版，A/B 时才能确认是改善了还是只是变整齐了。

## 耳朵要抓的点

保留自己 MIDI 素材的原时序，在副本上尝试量化，再比较重音、装饰音与自由速度。本页合成练习只呈现长短时值分配，没有执行量化或提供处理后的对照。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"T t T t T t T t","bpm":116,"label":"合成节奏示意","label_en":"Synthesized rhythm","hint":"浏览器合成示意；不是模型输出或处理前后对比。","hint_en":"A browser-synthesized exercise, not model output or a processing comparison."}
```
:::

::: en
## Where it gets hard

Generated MIDI often sits slightly off the grid, so it drags or refuses to line up with other tracks. A blanket quantise fixes that and removes the playing at the same time. Worse, the wrong grid can push accents onto the offbeat, which sounds less musical than the original error. When a whole passage is off, the cause is tempo or start point, not quantisation.

## The working mechanism

Quantising pulls each note onset to the nearest grid point, and strength decides how far. Full strength generally moves selected onsets to the target grid; try fifty to seventy percent as a starting point and listen in context. The grid has to match the music, because triplets, six-eight and swung eighths do not fit a sixteenth grid. Quantization can target starts, ends or both, depending on the software settings. Quantizing ends changes note lengths. Onset correction does not automatically fix velocity, pedal data or every length problem; check those separately. It also collapses rolled chords and arpeggios onto one point, which hardens the attack.

## Where to start

Listen before quantising and never select all on import. Quantise only the notes that are clearly wrong, using quantise selected notes. Choose the grid by meter and subdivision, use a groove matching the actual swing ratio; a triplet grid suits only a triplet-like subdivision. Skipping quantization is also an option. Start at sixty percent strength and add ten percent at a time while listening. Afterwards nudge accents a few milliseconds early or late to recover the feel. Drums and bass can take heavier settings, melody and solos far lighter. Keep a copy before and after, so an A/B tells you whether it improved or merely tidied, and check the result against the other tracks rather than alone.

## What the ear catches

Keep the original timing of your MIDI material and try quantization on a copy, then compare accents, ornaments and rubato. The synthesized exercise here presents a long-short subdivision; it does not apply quantization or provide an edited comparison.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"T t T t T t T t","bpm":116,"label":"Synthesized rhythm","label_en":"Synthesized rhythm","hint":"A browser-synthesized exercise, not model output or a processing comparison.","hint_en":"A browser-synthesized exercise, not model output or a processing comparison."}
```
:::

