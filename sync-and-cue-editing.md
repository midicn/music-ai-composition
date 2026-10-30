---
id: sync-and-cue-editing
site: ai
cat: F
title: 同步与 cue 剪辑
title_en: Sync and Cue Editing
summary: 切点要落在乐句收尾，不要切在重音和混响里
summary_en: Cut at the end of a phrase, never on an accent or inside a reverb tail
level: standard
tags: [同步, 剪辑, 乐句, 速度映射]
tags_en: [sync, cue editing, phrasing, tempo map]
alias: [对画面, cue 剪辑, sync editing]
order: 5
links:
  - "[[glossary:tempo]]"
  - "[[glossary:cue]]"
instances:
  - atepp-001283 | rubato 让网格失效，必须先做 tempo map（C1）
  - atepp-002718 | 四小节乐句规整，切点落在句尾（C1）
  - m21-001918 | 无前奏直接进主题，切点自由度更大（C1）
sources:
  - 音画同步的切点与速度映射做法，依剪辑与配乐通识核对，未抄原文
  - Cutting and tempo mapping practice for picture, checked against general editing knowledge, not copied
updated: 2026-10-30
---

::: zh
## 问题

把生成音乐贴到画面上，最容易犯的错是按画面长度硬切，切在乐句中间、重音上或者混响尾巴里。观众说不清哪里不对，只觉得廉价。改一版再切一次，问题往往挪到别处，因为素材本身没有给切点留位置。

## 原理

音乐有句法，四小节、八小节为一个单位，重音落在强拍，收尾落在终止。切点如果落在句尾最后一拍之后，听感是"说完"；落在句中，听感是被打断。速度稳定的素材可以直接对网格，带 rubato 的演奏必须先做 tempo map，否则越到后面偏得越多。生成的素材常常没有明确终止，段落之间是渐变的，这就是难切的原因。

## 做法

先数清素材的乐句，标出所有可能的落点，再回头改画面或改音乐。优先伸缩音乐，其次才是裁画面。需要缩短时，删掉一个完整乐句比截掉两秒好。需要延长时，复制一段并做配器变化，不要拉长最后一个音。切点避开镲、定音鼓和混响长的音符，宁可早半拍收在干声上。给每条素材做 tempo map，把重音对齐到画面上，再检查整段有没有漂移。对白盖住的段落可以粗切，音乐露出来的地方才值得精切。

## 听什么

在肖邦夜曲里听 rubato 怎样让节拍器网格失效，在巴赫的小步舞曲里听四小节乐句怎样规律收束，在 7thRegimentReel 里听没有前奏的曲调怎样直接从第一拍开始。前两个告诉你切点在哪，第三个告诉你素材一旦没有前奏，剪辑的自由度反而更大。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":96,"label":"句尾的落点","label_en":"The landing at the phrase end","hint":"把切点放在最后一拍之后，听句子有没有说完","hint_en":"Put the cut after the last beat and hear whether the phrase closes"}
```
:::

::: en
## The problem

The commonest mistake when fitting generated music to picture is cutting to the exact length of the shot, which puts the cut inside a phrase, on an accent, or in a reverb tail. Viewers cannot name the problem, they just find it cheap. Re-cut a new version and the fault moves somewhere else, because the material never left room for a cut.

## How it works

Music has syntax, in units of four or eight bars, with accents on strong beats and endings on cadences. A cut placed after the last beat of a phrase feels finished; a cut inside the phrase feels interrupted. Material at a steady tempo can be cut against the grid, while a performance with rubato needs a tempo map first, or the drift grows with every bar. Generated cues often lack a clear cadence and change gradually between sections, which is exactly why they are hard to cut.

## Practice

Count the phrases and mark every possible landing before changing picture or music. Stretch the music first and trim the picture second. To shorten, remove a whole phrase rather than chop two seconds. To lengthen, repeat a section with a change of orchestration instead of stretching the last note. Keep cuts away from cymbals, timpani and long reverb, and prefer ending half a beat early on dry sound. Map the tempo of every cue, land the accents on picture, then check the whole sequence for drift. Cuts only matter where the music is exposed; under dialogue they can be rough.

## What to listen for

In the Chopin nocturne, how rubato defeats a metronome grid; in the Bach minuet, how four-bar phrases close regularly; in 7thRegimentReel, how a tune with no intro starts on the first beat. The first two show where cuts belong, the third shows that material without an intro leaves the editor more freedom, not less.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":96,"label":"The landing at the phrase end","label_en":"The landing at the phrase end","hint":"Put the cut after the last beat and hear whether the phrase closes","hint_en":"Put the cut after the last beat and hear whether the phrase closes"}
```
:::
