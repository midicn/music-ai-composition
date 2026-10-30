---
id: fixing-artifacts
site: ai
cat: C
title: 修复伪影
title_en: Fixing Artefacts
summary: 先分清是生成伪影还是演奏处理，再决定修还是重生成
summary_en: Tell a generation artefact from a performance choice, then decide whether to repair or regenerate.
level: standard
tags: [伪影, 音质, 修复, 判断]
tags_en: [artefacts, audio quality, repair, judgement]
alias: [生成伪影, 音频伪影, fixing artefacts]
order: 7
links:
  - "[[glossary:reverb]]"
  - "[[glossary:noise-floor]]"
  - "[[glossary:stems]]"
instances:
  - groove-000000 | 放克鼓组循环，听底鼓与军鼓的起音是否干净（C1）
  - cyberhymnal-003101 | 管风琴赞美诗，长音多，尾音最容易糊成一片（C1）
  - atepp-005385 | 拉威尔《绞刑架》，听固定音型与和弦层是否分得开（C1）
  - openscore-000269 | 马勒艺术歌曲，人声长音与钢琴对照，辨音高晃动（C1）
sources:
  - 生成式音频常见伪影的类别与成因，依公开技术资料归纳，未抄原文
  - 修复与重生成的取舍，依后期制作通识核对，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

生成结果里出现咔哒声、尾音糊、音高飘、声部之间像隔着一层水，这些不一定是模型坏了，也可能是提示或参数把它逼到了边界。修之前先判断它是什么，再判断值不值得修。伪影不等于失败，它往往只是条件写得太满的证据。

## 原理

伪影有几类典型来源。起音处的爆音多来自拼接与包络，长音糊成一片来自混响尾与延音处理，音高不稳常见于人声与持续弦乐，声部发虚、分离感像水一样来自分离算法残留的串音。演奏本身也有类似现象，揉弦、滑音、踏板与房间声都会让声音不那么干净，这正是判断的难点。还有一类来自时长，一次生成过长的段落，模型在换气处拼接，接缝会以音量跳变的形式出现。

## 做法

先关掉混响与压缩听干声，把问题定位到某一层。剪掉起音前几毫秒、画一条短淡入、改掉个别音高就能解决的小问题，就地修。整段糊、声部互相渗透、节奏已经错位的，重生成比修便宜。重生成时只改一个条件，比如缩短时长、降低密度、换更简单的织体，不要一次改五个。修完放回整体，确认没有为了局部干净牺牲了乐句。导出干声，用频谱看那几个可疑频段是否还有尖峰，耳朵会疲劳，图不会。

## 听什么

在放克鼓组里听起音是否利落，在管风琴赞美诗里听长音尾是否糊成一片，在《绞刑架》里听固定音型与和弦是否分得开，在马勒歌曲里听人声长音有没有不该有的晃动。四处对照，伪影与演奏处理的界线会慢慢清楚。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":120,"label":"干净的起音","label_en":"Clean attacks","hint":"每一击的起始要清楚，糊成一片就是伪影","hint_en":"Each attack should be clear; a smear is an artefact"}
```
:::

::: en
## The problem

A generation returns clicks, blurred tails, drifting pitch and parts that sit behind a sheet of water. None of this proves the model failed. The prompt, the length, the density or the reference may simply have pushed it to an edge. Identify what the fault is before deciding whether it deserves repair.

## How it works

Artefacts have recognisable sources. A click at an attack usually comes from a splice, a short envelope or a cut sample. A blurred sustain comes from reverb tails, release handling or too much overlap between notes. Unstable pitch appears in voice and sustained strings, where the model has to invent vibrato and portamento. Watery separation comes from a separation model leaving bleed between parts. A long generation also risks seams where the model splices at a breath, and those seams show up as jumps in level. Performance produces similar effects, since vibrato, portamento, pedal and room sound all reduce cleanliness; that overlap is what makes the judgement hard.

## Practice

Mute reverb and compression and listen dry, then locate the fault in a single layer. Small faults yield to trimming a few milliseconds before an attack, drawing a short fade, or correcting one note. When a whole passage is blurred, parts bleed into each other, or the timing has slipped, regeneration is cheaper than repair. Change one condition per regeneration, such as a shorter clip, lower density or a simpler texture, never five at once. Keep the previous version until the new one has been compared against it, and put the fix back into the whole to check that the phrase still breathes.

## What to listen for

On the funk kit, whether attacks stay crisp; on the organ hymn, whether long tails blur; on Le gibet, whether the ostinato and the chords remain separate; on the Mahler song, whether the voice holds pitch without unintended wobble. Comparing the four slowly draws the line between artefact and performance.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":120,"label":"Clean attacks","label_en":"Clean attacks","hint":"Each attack should be clear; a smear is an artefact","hint_en":"Each attack should be clear; a smear is an artefact"}
```
:::
