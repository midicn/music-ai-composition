---
id: midi-generation-tools
site: ai
cat: A
title: MIDI 生成工具
title_en: MIDI Generation Tools
summary: 出 MIDI 而不是音频，意味着每个音都能改，也意味着音色要自己找。
summary_en: Getting MIDI rather than audio means every note is editable, and every sound is your problem.
level: standard
tags: [MIDI, 生成, 可控性, 编曲]
tags_en: [MIDI, generation, control, arranging]
alias: [MIDI 生成, 符号生成, MIDI generation]
order: 4
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:velocity]]"
  - "[[glossary:daw]]"
instances:
  - atepp-007103 | 莫扎特回旋曲，看生成工具能否写出清晰的主题与伴奏分工（C1）
  - musicnet-000090 | 贝多芬四重奏，四声部写作对符号生成是硬考验（C1）
  - thesession-006629 | 爱尔兰曲调，单声部旋律与装饰音的生成空间（C1）
sources:
  - 符号音乐生成的表示方式——依据来自公开研究摘要。
  - MIDI 生成与音频生成的取舍，对照制作实践惯例整理。
updated: 2026-10-30
---

::: zh
## 问题

直接用文本生成音频，得到的是成品，改一个和弦要重来。生成 MIDI 则相反：得到的是音符，每个音都能拖、能换音色、能拆给不同乐器。代价是声音要自己解决，而且生成结果常常太"正确"，缺少演奏的呼吸。

## 原理

符号生成模型在音符、时值、力度这些离散事件上工作，可以用文本、和弦符号或前几小节作为条件。因为不涉及音频，模型可以把注意力放在声部进行与节奏结构上。但 MIDI 没有音色，也没有演奏的细微起伏，量化到网格后容易显得机械。模型对配器的理解也有限，常把旋律与伴奏写成同一种密度。

## 怎么用

把它当成写草稿的助手：生成主题、和声骨架或鼓型，再自己改。生成后先修力度与微时序，让演奏有呼吸。换音色时要重新评估音区与密度，别把钢琴织体直接给弦乐。多声部生成要检查声部是否打架。得到的 MIDI 可以进 DAW 继续编辑，也可以导进记谱软件排版。

## 听什么

在回旋曲里听主题与伴奏是否分得开，在四重奏里听四个声部是否各说各话，在民谣里听装饰音是否自然。MIDI 生成的好坏，听的是结构与演奏感，而不是音色。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4","E4","D4","C4","G3"],"label":"一段可编辑的音符","label_en":"Notes you can still edit","hint":"每个音都能改，听的是结构与力度，而不是音色","hint_en":"Every note stays editable; judge structure and dynamics, not tone"}
```
:::

::: en
## The problem

Text to audio hands you a finished track, and changing one chord means starting over. MIDI generation is the opposite: you get notes that can be dragged, re-voiced and split across instruments. The price is that the sound is your job, and results often feel too correct, missing a performer's breath.

## How it works

Symbolic models work on discrete events such as pitch, duration and velocity, conditioned on text, chord symbols or previous bars. Because audio is not involved, the model can concentrate on voice leading and rhythmic structure. But MIDI carries no timbre and no performance nuance, and quantised to a grid it easily sounds mechanical. Models also understand orchestration poorly, often writing melody and accompaniment at the same density.

## How to use it

Treat it as a sketching assistant: generate a theme, a harmonic skeleton or a drum pattern, then edit. Fix velocity and microtiming afterwards so the part breathes. When changing instruments, reassess register and density instead of handing piano figuration to strings. Check generated parts for collisions. The MIDI can go into a DAW for further work or into notation software for engraving.

## What to listen for

In the rondo, whether theme and accompaniment separate; in the quartet, whether four voices each speak; in the folk tune, whether ornaments feel natural. Judging MIDI means judging structure and performance, not tone.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4","E4","D4","C4","G3"],"label":"Notes you can still edit","label_en":"Notes you can still edit","hint":"Every note stays editable; judge structure and dynamics, not tone","hint_en":"Every note stays editable; judge structure and dynamics, not tone"}
```
:::
