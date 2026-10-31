---
id: tempo-drift-fix
site: ai
cat: C
title: 速度漂移修复
title_en: Fixing Tempo Drift
summary: 先分清拼接错位与演奏伸缩，再决定拉伸还是重生成
summary_en: Tell a bad splice from expressive timing before choosing between stretching and regenerating.
level: standard
tags: [速度, 漂移, 对齐, 拼接]
tags_en: [tempo, drift, alignment, splicing]
alias: [速度漂移, 对速, tempo drift]
order: 132
links:
  - "[[glossary:tempo]]"
  - "[[glossary:rubato]]"
  - "[[glossary:meter]]"
instances:
  - groove-000013 | 116 BPM 爵士放克鼓组，稳定的网格用来判断漂移从哪小节开始（C1）
  - abcmisc-000288 | 凯什吉格舞曲，六八拍的重音成组，漂移会先毁掉分组（C1）
  - abcmisc-000179 | Garofitsa 吉格舞曲，复合拍里每个分组的第一拍都要对齐（C1）
  - atepp-000501 | 李斯特夜曲即兴，渐慢与抢拍是演奏信息，不该被 tempo map 拉平（C1）
sources:
  - Ableton Live 手册与 Walter Piston, Harmony 中关于速度、拍号与复合拍的记法与听辨。
  - 音频拼接与时间拉伸的取舍，依据数字音频编辑惯例。
updated: 2026-10-31
---

::: zh
## 先分清三种不齐

整轨量化之后，鼓点是对上了，副歌却比主歌早半拍，接缝处像被人拽了一下。速度问题至少有三类：整曲比目标略快或略慢，段落拼接时拍点没对齐，演奏本身的渐慢与抢拍。前两类要修，第三类常常不该动。

## 检测：每八小节对一次首拍

- 铺一条节拍器轨，从头到尾听，记下第一次偏离的小节
- 每八小节标一次首拍，偏差超过十毫秒就记录
- 在拼接点前后各听两拍，检查重音是否叠在一起
- 贝斯与底鼓单独听，判断是整体漂移还是个别音错位
- 看波形上的瞬态间距，确认漂移是渐变还是跳变
- 修完从头听两遍，确认段落之间的相对速度没变

渐变多半来自生成时的速度估计，跳变多半来自拼接。两者的修法不同，先分清再动手。

## 修法按代价排序

最省事的是重生成边界两小节，让模型在同一速度下自己接上。其次是切片对齐：切在静音或鼓点上，移动整段，接缝处补极短交叉淡化。最后才是时间拉伸，拉伸超过百分之二，瞬态会变软，音色会发闷。用 tempo map 逐段修正，不要整轨量化；整轨量化会把渐慢和抢拍一起抹平，段落之间的呼吸也没了。

## 不该修的情形

三连音、复合拍、真正的渐慢都不该被拉直。把吉格舞曲的六八拍塞进四四，把夜曲的自由速度对齐到网格，得到的是准确而死的演奏。判断标准很简单：偏离是否每次都一样。每次都一样是误差，每次不同是表达。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q q q q q","bpm":120,"label":"八拍里的第一拍","label_en":"The downbeat across eight beats","hint":"跟着数一到四，再把整条节奏往后挪半拍，听接缝处哪里变了","hint_en":"Count one to four, then shift the whole pattern half a beat late and hear what changes at the seam"}
```
:::

::: en
## Separate three kinds of misalignment

Quantise a whole track and the drums line up, yet the chorus arrives half a beat before the verse and the seam feels yanked. Tempo trouble comes in at least three forms: the whole piece runs slightly fast or slow, a splice lands off the beat, or the performance itself pushes and pulls. The first two need repair; the third usually does not.

## Detect it by checking the downbeat every eight bars

- Lay a click under the whole track and note the first bar that drifts
- Mark the downbeat every eight bars and log any offset beyond ten milliseconds
- Listen two beats either side of every splice for stacked accents
- Solo bass and kick to separate overall drift from a single misplaced hit
- Read transient spacing in the waveform to see whether drift is gradual or a jump
- After the repair, listen twice from the top and confirm the relative tempo between sections is unchanged

Gradual drift usually comes from tempo estimation during generation; a jump usually comes from splicing. The fixes differ, so identify the kind first.

## Order the fixes by cost

The cheapest repair is regenerating the two bars around the boundary so the model joins at one tempo. Next is slice alignment: cut on silence or a drum hit, move the whole section, and add a very short crossfade at the seam. Time-stretching comes last, because beyond about two percent transients soften and the tone dulls. Correct section by section with a tempo map rather than quantising the whole track; a blanket pass erases rubato and ritardando along with the breathing between sections.

## When not to fix it

Triplets, compound metre and genuine ritardando should not be straightened. Forcing a jig in six-eight into 4/4, or snapping a nocturne's free timing to a grid, yields a performance that is accurate and dead. The test is simple: does the deviation repeat identically? The same offset every time is an error; a different one each time is expression.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q q q q q","bpm":120,"label":"The downbeat across eight beats","label_en":"The downbeat across eight beats","hint":"Count one to four, then shift the whole pattern half a beat late and hear what changes at the seam","hint_en":"Count one to four, then shift the whole pattern half a beat late and hear what changes at the seam"}
```
:::
