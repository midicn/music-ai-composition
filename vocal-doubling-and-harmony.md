---
id: vocal-doubling-and-harmony
site: ai
cat: E
title: 叠录与和声
title_en: Doubling and Harmony
summary: 叠录让一条人声变厚，堆到第三层就开始相位打架
summary_en: Doubling thickens one voice, but a third copy starts fighting itself in phase.
level: standard
tags: [叠录, 和声, 相位, 声部]
tags_en: [doubling, harmony, phase, voice leading]
alias: [叠唱, 人声和声, vocal stacking]
order: 4
links:
  - "[[glossary:doubling]]"
  - "[[glossary:phase-check]]"
  - "[[glossary:voicing]]"
instances:
  - m21-000489 | 蒙特威尔第牧歌，听各声部独立而不互相抵消（C1）
  - mutopia-001849 | 韦尔克斯四部颂歌，听和声块的厚度从哪里来（C1）
  - cyberhymnal-003945 | 四部众赞歌，最简单的和声堆叠参照（C1）
  - musicnet-000091 | 贝多芬四重奏慢乐章，听四条线如何互相让位（C1）
sources:
  - 叠录与和声的相位问题——依据来自录音实践与公开技术说明。
  -  — based on Doubling and phase cancellation.
updated: 2026-10-30
---

::: zh
## 门槛

叠录是把同一条旋律录两遍以上再叠起来，让一条人声听起来更厚，或者像几个人。它便宜、有效，也最容易做成塑料感。通常到第三层，问题已经不在唱得准不准，而在相位。真正的难点是让加厚的部分听起来仍然是一条旋律，而不是四条各唱各的。

## 背后的机制

两份几乎相同的波形叠在一起，时间差很小时会互相抵消，形成梳状滤波，高频先掉，声音变薄变尖。时间差拉到十五到三十毫秒，人耳才开始把它听成两个声源。失谐几音分也能帮上忙，因为共振峰错开之后，两份声音不再完全重合。和声堆叠是另一回事，它改变的是音高关系，三度、六度最稳，二度容易和旋律打架。

## 怎么调整

主唱单独居中，不做宽度处理。double 分到左右，各做五到十音分的失谐和十到二十五毫秒的延迟，音量低三到六分贝。和声先写三度和六度，检查有没有和旋律撞小二度，低声部优先写根音和三音。先决定厚度来自人数还是来自音色，两者不要同时加。用生成声音做 double 时，换一个相近但不同的音色，别用同一个模型同一个种子跑两遍。每加一层就按单声道听一次，塌了就减一层，而不是加更多层去补。

## 耳朵要抓的点

在蒙特威尔第的牧歌里听每个声部怎么保持独立，在韦尔克斯的四部颂歌里听和声块的厚度，在四部众赞歌里听最简单的堆叠怎么不糊，在贝多芬四重奏的慢乐章里听四条线怎么互相让位。叠录要往这三点看齐，而不是只把音量堆大。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["F3","A3","C4","F4","C4","A3","F3"],"label":"一个三和弦的叠法","label_en":"A triad stacked in thirds","hint":"同度叠录听厚度，三度和声听声部是否独立","hint_en":"Unison doubles add weight; thirds should still sound like separate parts"}
```
:::

::: en
## The threshold

Doubling records the same line two or more times and stacks the takes, making one voice thicker or making it sound like several. It is cheap, effective and very easy to turn plastic. By the third layer the problem is rarely the singing. It is phase. The harder task is keeping the thickened result sounding like one melody rather than four lines each doing its own thing.

## The mechanism

Two nearly identical waveforms summed with a very small offset cancel each other, producing comb filtering: the top end drops first and the sound turns thin and sharp. Once the offset reaches fifteen to thirty milliseconds, the ear begins to hear two sources. A few cents of detuning also helps, because the formants no longer coincide exactly. Harmony stacking is a different operation. It changes pitch relationships, where thirds and sixths are stable and seconds tend to collide with the melody.

## How to adjust

Keep the lead centred and leave it mono. Place doubles left and right, each detuned five to ten cents and delayed ten to twenty-five milliseconds, sitting three to six decibels lower. Write harmony in thirds and sixths first, check for minor seconds against the melody, and give the lower part the root and third. When a generated take is used as a double, choose a similar but different timbre rather than running the same model with the same seed twice. Check in mono after every added layer. If it collapses, remove a layer instead of adding more to compensate.

## What the ear catches

In Monteverdi's madrigal, listen to how each part stays independent. In Weelkes's four-part anthem, listen to where the thickness of the block comes from. In the four-part chorale, hear the simplest stack avoid mush. In the slow movement of Beethoven's quartet, listen to four lines making room for one another. Doubling should aim at these things, not just at a higher fader.

```audiolab
{"type": "instrument", "gm": "Choir Aahs", "synth": "vocal", "phrase": ["F3", "A3", "C4", "F4", "C4", "A3", "F3"], "label": "A triad stacked in thirds", "label_en": "A triad stacked in thirds", "hint": "同度叠录听厚度，三度和声听声部是否独立", "hint_en": "Unison doubles add weight; thirds should still sound like separate parts"}
```
:::
