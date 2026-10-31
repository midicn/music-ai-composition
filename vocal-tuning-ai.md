---
id: vocal-tuning-ai
site: ai
cat: E
title: 人声修音
title_en: Tuning Vocals
summary: 修音修的是音高与时间，修过头先丢颤音，再丢人味
summary_en: Tuning corrects pitch and timing; overdone, it removes vibrato first and humanity second.
level: standard
tags: [修音, 音高, 颤音, 时间]
tags_en: [tuning, pitch, vibrato, timing]
alias: [修音, 音准修正, pitch correction]
order: 3
links:
  - "[[glossary:pitch]]"
  - "[[glossary:vibrato]]"
  - "[[instrument:auto-tune]]"
instances:
  - openscore-000084 | 长音多的舒伯特歌曲，听修音是否把颤音压平（C1）
  - openscore-000039 | 德彪西快速法语歌曲，听时间修正会否切碎音节（C1）
  - openscore-000014 | 奎尔特英语宣叙，听修正后重音是否还在原位（C1）
sources:
  - 音高与时间修正的处理方式（数字音频工作站说明）。
  - , with reference to Pitch and timing correction practice.
updated: 2026-10-30
---

::: zh
## 难在哪

修音的目的不是把每个音钉在格子上，而是让音高和时间回到该在的位置。人声的音高是连续的，颤音、滑音、辅音前的上滑都是表达的一部分。修过头，先失去颤音，再失去情绪，最后连字都变得一样重。修音师的工作有一半是判断哪些音不该动。

## 机制

音高修正比较每个音与目标音高的偏差，再决定移动多少。时间修正对齐音节的起点。颤音大约是每秒五到七次的调制，如果修正窗口比一个颤音周期还短，算法会把波峰和波谷当成两次跑调，一路压平。滑音同理，修得越快，越容易变成阶梯。共振峰不随音高移动，移调过度会改变元音。生成人声的音高曲线通常更规整，反而更容易被修成一条直线。

## 具体做法

先修时间再修音高，顺序反了会重复劳动。修正速度放慢到三十到五十毫秒，保留滑音。长音允许十到二十音分的自然漂移，不要归零。同一条唱段分三段处理，主歌轻、副歌中等、尾句最轻。对生成人声，先把音高曲线导成 MIDI 看一眼，再决定修哪几个音，别整段套用。把处理前后的音高曲线截图留档，方便回头比较。每次改完和干声 A/B，注意齿音、换气和辅音有没有被一起拉平。

## 耳朵要抓的点

在 Du bist die Ruh 的长音上听颤音的宽度，在 Mandoline 的快速音节里听音准有没有被切碎，在 Come Away, Death 的宣叙句里听时间修正有没有把重音挪走。修得好的版本，听不出修过。修音好不好，听的是这些地方还在不在，而不是音高表上有多整齐。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["A3","A3","A3","A3","G3","A3","B3","A3"],"label":"同音反复最考验音准","label_en":"Repeated notes expose tuning","hint":"把颤音修平，长音就只剩一条直线","hint_en":"Flatten the vibrato and a long note becomes a straight line"}
```
:::

::: en
## Where it gets hard

Tuning is not meant to nail every note to a grid. It puts pitch and timing back where they belong. A voice moves continuously; vibrato, portamento and the slide into a consonant are part of the expression. Correct too hard and vibrato goes first, then emotion, and finally every syllable weighs the same.

## The mechanism

Pitch correction compares each note with a target and decides how far to move it. Timing correction aligns syllable onsets. Vibrato is a modulation of roughly five to seven cycles per second. If the correction window is shorter than one vibrato cycle, the algorithm reads each peak and trough as a separate error and flattens the whole thing. Portamento behaves the same way: the faster the correction, the more it turns into steps. Generated vocals often arrive with a tidier pitch curve, which makes them easier to iron into a straight line.

## In practice

Fix timing before pitch; the reverse order means doing the work twice. Slow the correction to thirty or fifty milliseconds so slides survive. Allow ten to twenty cents of natural drift on long notes instead of forcing zero. Process a take in three passes, light on the verse, medium on the chorus, lightest on the last line. For a generated vocal, export its pitch curve as MIDI first and choose the notes to fix rather than treating the whole take. Compare with the dry signal after every change, watching sibilance, breath and consonants.

## What the ear catches

On the long notes of Du bist die Ruh, listen to the width of the vibrato. In the fast syllables of Mandoline, listen for tuning chopped into steps. In the declamation of Come Away, Death, listen for accents moved off their syllables. Good tuning is heard in what survives, not in how straight the pitch graph looks.

```audiolab
{"type": "instrument", "gm": "Voice Oohs", "synth": "vocal", "phrase": ["A3", "A3", "A3", "A3", "G3", "A3", "B3", "A3"], "label": "Repeated notes expose tuning", "label_en": "Repeated notes expose tuning", "hint": "把颤音修平，长音就只剩一条直线", "hint_en": "Flatten the vibrato and a long note becomes a straight line"}
```
:::
