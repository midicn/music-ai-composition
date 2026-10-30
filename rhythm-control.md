---
id: rhythm-control
site: ai
cat: C
title: 节奏控制
title_en: Controlling Rhythm
summary: 律动靠重音与微差，量化网格会把它压成直尺
summary_en: Groove lives in accents and micro-timing; a quantised grid flattens it into a ruler.
level: standard
tags: [律动, 摇摆, 切分, 量化]
tags_en: [groove, swing, syncopation, quantisation]
alias: [节奏控制, 律动控制, rhythm control]
order: 10
links:
  - "[[glossary:syncopation]]"
  - "[[glossary:tempo]]"
  - "[[glossary:midi-protocol]]"
instances:
  - groove-000000 | 138 BPM 放克鼓组，听十六分里的重音与鬼音（C1）
  - groove-000002 | 86 BPM 灵魂乐鼓组，听军鼓落在拍后那一点（C1）
  - abcmisc-000288 | 凯什吉格舞曲，复合拍的顿挫，量化到四四会散（C1）
  - abcmisc-001334 | 《第十二街拉格》，切分旋律压在稳定低音上（C1）
sources:
  - 律动的构成要素，依流行音乐制作通识核对，未抄文本
  - 量化与人性化的取舍，依编曲实践归纳，未抄原文
updated: 2026-10-30
---

::: zh
## 问题

提示里写"有律动""稍微摇摆"，结果不是死板就是散。节奏是模型最容易交差、也最容易被网格毁掉的维度，因为听起来没错，只是没有风格。这不是模型不懂节奏，而是描述没有落点。

## 原理

律动由三样东西构成。重音位置，十六分音符被切成有重有轻的组；时值微差，长一点短一点决定松弛还是紧张；相对节拍的前后偏移，灵魂乐的军鼓习惯压在拍后。拉格的切分要靠在低音保持稳定时才成立。量化把所有音符吸到格子上，微差被抹平，风格也随之消失。同一份 MIDI 换一套音色，律动评价会立刻改变，起音快慢和尾音长短都会改写重音。

## 做法

先写骨架，标出每小节哪些位置必须发声，再标哪些位置只能轻轻带过。摇摆量用百分比写，六成到七成通常够用。需要人味就在量化后手动挪动几个音，军鼓晚几毫秒，踩镲提前几毫秒，只挪打击点，不要整轨随机。复合拍子不要硬塞进四四，直接写明拍号与分组。有参考鼓组时，把参考与生成结果对齐到同一小节，逐个乐器比对落点，而不是整体循环着听。最后只保留一版继续做，别在两版之间反复。把人味参数记下来，下次才有参照，否则每次都在重新猜。

## 听什么

在放克鼓组里听十六分的重音与鬼音是否成形，在灵魂乐鼓组里听军鼓是否落在拍后，在吉格舞曲里听复合拍的顿挫，在拉格舞曲里听切分旋律怎样压在稳定低音上。网格留下的痕迹，在这四处都听得见。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":96,"label":"直的十六分","label_en":"Straight sixteenths","hint":"先听直的，再想把同样的型前后挪几毫秒会怎样","hint_en":"Hear it straight, then imagine the same pattern shifted a few milliseconds"}
```
:::

::: en
## The problem

Ask for groove, or a touch of swing, and the result is either stiff or loose in the wrong way. Rhythm is the dimension a model satisfies most easily and a grid destroys most thoroughly, because nothing sounds wrong, only unstyled. The model is not ignorant of rhythm; the description simply has no landing point.

## How it works

Groove is built from three things. Accent placement, where sixteenths group into strong and weak positions. Small differences in note length, which decide whether the feel is relaxed or tense. Offsets against the beat, since a soul drummer places the snare slightly late. Ragtime syncopation only works when the bass stays steady underneath. Quantisation pulls every note onto the grid, erases those differences and takes the style with them. Swap the sound library on the same MIDI and the judgement of groove changes at once, because attack speed and tail length rewrite the accents.

## Practice

Write the skeleton first, marking which positions in each bar must sound and which may only be brushed. State swing as a percentage, where sixty to seventy percent is usually enough. For human feel, move a few notes by hand after quantising, the snare a few milliseconds late and the hi-hat a few early, and move only the strikes rather than randomising a whole track. Do not force a compound metre into 4/4; name the time signature and the grouping instead. With a reference kit, align reference and result to the same bar and compare placement instrument by instrument rather than looping the whole thing. Keep one version to continue from instead of switching back and forth, and write the humanising values down, otherwise every session starts by guessing again.

## What to listen for

On the funk kit, whether sixteenth accents and ghost notes take shape; on the soul kit, whether the snare sits behind the beat; in the jig, the lilt of compound time; in the rag, how the syncopated melody rides a steady bass. The marks of the grid are audible in all four.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":96,"label":"Straight sixteenths","label_en":"Straight sixteenths","hint":"Hear it straight, then imagine the same pattern shifted a few milliseconds","hint_en":"Hear it straight, then imagine the same pattern shifted a few milliseconds"}
```
:::
