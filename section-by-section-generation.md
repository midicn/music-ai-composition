---
id: section-by-section-generation
site: ai
cat: B
title: 分段生成
title_en: Section-by-Section Generation
summary: 长曲难以一次生成，分段写提示、再缝合，结构才守得住。
summary_en: Long pieces rarely survive one generation; prompt section by section and stitch, or the form collapses.
level: standard
tags: [分段, 结构, 拼接, 工作流]
tags_en: [sections, form, stitching, workflow]
alias: [分段生成, 分段提示, section generation]
order: 8
links:
  - "[[glossary:tempo]]"
  - "[[glossary:key]]"
  - "[[glossary:ternary-form]]"
instances:
  - mutopia-000498 | 贝多芬第五第二乐章，变奏段落各不相同，整曲一次性生成难以稳住（C1）
  - atepp-007103 | 莫扎特回旋曲，主题与插部交替，段落边界清楚（C1）
  - thesession-020649 | 里尔舞曲，短小重复的段落适合逐段生成再拼（C1）
sources:
  - 分段生成与拼接的常见做法，依生成实践公开资料核对，未抄原文
  - 段落边界的和声与节拍处理，依曲式学通识核对，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

让模型一次生成四分钟，常见结果是开头像样、中段松散、结尾草率收场。长结构需要计划，而模型没有计划。分段生成把控制权拿回来：每段单独写提示，分别生成，再按段落边界拼接。

## 原理

拼接的难点在边界。两段的速度、调性、配器与混响必须一致，否则接缝立刻暴露。最稳的接法是让边界落在和声稳定处，并在前段末尾留出自然的收束，后段从同调同速进入。硬切适合段落对比明显的场合，交叉淡化适合氛围连续的音乐。长度不必相等，但要在节拍上对齐。

## 做法

先画出段落表：每段的长度、调性、配器、情绪与功能。逐段生成时把相邻段落的信息写进提示，减少风格漂移。生成后先单独听每段是否成立，再听接缝。接缝问题优先重生成后段，而不是修前段。拼接完成后统一做响度与音色匹配，最后整体听一遍结构是否讲得通。

## 听什么

在变奏乐章里听段落之间的性格差异，在回旋曲里听主题与插部的边界，在里尔舞曲里听重复段落的接缝。分段做得好的曲子，听不出哪一段是单独生成的。

```audiolab
{"type":"progression","key":"C","chords":["C","Am","F","G"],"label":"段落边界的和声","label_en":"Harmony at a section boundary","hint":"边界落在稳定和弦上，接缝才不刺耳","hint_en":"A seam is quietest when it lands on a stable chord"}
```
:::

::: en
## The problem

Ask for four minutes in one pass and the usual result starts well, loosens in the middle and ends abruptly. Long forms need a plan and the model has none. Section-by-section generation takes control back: a prompt per section, generated separately, stitched at the boundaries.

## How it works

The difficulty is the seam. Tempo, key, instrumentation and reverb must match across the join or it shows at once. The safest join lands on stable harmony, with the first section closing naturally and the next entering in the same key and tempo. A hard cut suits strong contrast, crossfades suit continuous atmosphere. Sections need not be equal, but they must align on the beat.

## Practice

Draw a section table first: length, key, instrumentation, mood and function. Include neighbouring section information in each prompt to reduce drift. After generating, audition each section alone before the seams. Fix a seam by regenerating the later section rather than patching the earlier one. Match loudness and tone after stitching, then listen through for whether the form makes sense.

## What to listen for

In the variation movement, the change of character between sections; in the rondo, the boundaries of theme and episode; in the reel, the joins between repeats. Good section work leaves no audible clue about which part was generated alone.

```audiolab
{"type":"progression","key":"C","chords":["C","Am","F","G"],"label":"Harmony at a section boundary","label_en":"Harmony at a section boundary","hint":"A seam is quietest when it lands on a stable chord","hint_en":"A seam is quietest when it lands on a stable chord"}
```
:::
