---
id: inpainting-and-editing
site: ai
cat: C
title: 局部重绘与编辑
title_en: Inpainting and Editing
summary: 只重做一小节而不是整段，难的不是生成，是把接缝藏好
summary_en: Regenerating one bar instead of everything is easy to ask for and hard to make seamless.
level: standard
tags: [局部重绘, 接缝, 编辑, 上下文]
tags_en: [inpainting, seams, editing, context]
alias: [局部重生成, 选区重绘, inpainting]
order: 2
links:
  - "[[glossary:daw]]"
  - "[[glossary:phrase]]"
  - "[[glossary:midi-protocol]]"
instances:
  - atepp-000459 | 海顿回旋曲，主题每次回来都近乎同一句，接缝好辨认（C1）
  - cyberhymnal-003456 | 四声部众赞歌，被替换的和弦是否还顺声部进行（C1）
  - abcmisc-000288 | Kesh 吉格舞曲，替换半句后重音还落不落原位（C1）
  - groove-000015 | 116 BPM 爵士放克 fill，听接缝处镲片是否突然变亮（C1）
sources:
  - 局部重绘的边界选择；音频编辑实践惯例是主要依据。
  - 交叉淡化与增益匹配的做法——依据来自混音惯例。
updated: 2026-10-30
---

::: zh
## 起点：一个问题

整段重生成，等于把已经满意的部分一起换掉。局部重绘只让一小段变，其余保持不动。做起来不难，难在接缝。新片段和前后素材往往不是同一次演奏，响度、混响、力度曲线都可能对不上，接缝处会听见一个换人的瞬间。选区越大，越接近整段重生成，代价也越大。

## 背后的原理

边界落在音乐上说得通的位置，接缝才不明显。小节线、乐句尾、和弦切换点比小节中间安全。给工具的上下文要大于选区，前后各留一小节，它才知道该往哪里接。音频重绘会连尾音和混响一起换，MIDI 重绘只换音符，前者的接缝在频谱上，后者的接缝在时值与力度上。选区最好包含一个完整的和声进行，只换半个和弦，前后都会别扭。

## 具体做法

先在 DAW 里把选区对齐到小节线，前后各留一拍做交叠。生成后先独听新片段，判断它是否解决了原来的问题，再听接缝前后两秒。响度不一致就做增益匹配，相位或音色不一致就做短交叉淡化。连续三次出现同一种接缝问题，说明上下文给少了，扩大范围重来比继续微调更省时间。记录每次的选区范围与上下文长度，下次遇到同类问题可以直接复用。

## 耳朵要抓的点

在海顿的回旋曲里，主题每次回来都是同一句，换掉其中一小节最容易听出接缝。在四声部众赞歌里，听被替换的和弦是否还顺着同一条声部进行，还是突然平行了。在 Kesh 吉格舞曲里，听替换半句之后重音是否还落在原来的位置。在 116 BPM 的爵士放克 fill 里，听接缝处镲片是否突然变亮。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","B4","A4","G4","E4"],"label":"被替换的一小节","label_en":"One bar that was replaced","hint":"听这一句与前后是否像同一次演奏","hint_en":"Hear whether this phrase belongs to the same performance as its neighbours"}
```
:::

::: en
## Starting point: a problem

Regenerating the whole thing throws away the parts you already approved. Inpainting changes one short region and leaves the rest alone. Asking is easy; the seam is hard. The new fragment usually comes from a different performance, so level, reverb and dynamics may not match, and the join sounds like a player swap. The larger the selection, the closer you are to regenerating everything.

## The principle

A seam hides when the boundary lands somewhere musical. Bar lines, phrase ends and chord changes are safer than the middle of a bar. Give the tool more context than the selection, a bar on each side, so it knows what it is joining. Audio inpainting replaces tails and reverb along with the notes, MIDI inpainting replaces only notes, so the first seam lives in the spectrum and the second in timing and dynamics. A selection that contains one whole harmonic progression behaves better than half a chord.

## In practice

Align the selection to bar lines in the DAW and leave a beat of overlap on each side. After generating, listen to the new fragment alone to see whether it solved the problem, then listen to two seconds across the join. Match level with gain, and fix phase or tone with a short crossfade. If the same seam problem appears three times, the context was too small; widening the range saves more time than more nudging. Log the selection and context length so the next repair starts from a known point.

## What the ear catches

In Haydn's rondo, the theme returns almost identically each time, so replacing one bar exposes the seam at once. In the four-part chorale, whether the substituted chord still follows the same voice leading or suddenly moves in parallel. In the Kesh jig, whether accents land where they did before half a phrase was replaced. In the 116 BPM jazz-funk fill, whether the cymbals turn bright at the join.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5", "B4", "A4", "G4", "E4"], "label": "One bar that was replaced", "label_en": "One bar that was replaced", "hint": "听这一句与前后是否像同一次演奏", "hint_en": "Hear whether this phrase belongs to the same performance as its neighbours"}
```
:::
