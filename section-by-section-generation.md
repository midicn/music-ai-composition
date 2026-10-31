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
  - 分段生成与拼接的常见做法，参考生成实践公开资料。
  - 段落边界的和声与节拍处理；曲式学惯例是主要依据。
updated: 2026-10-30
---

::: zh
## 卡在哪

一次要四分钟，模型通常给得出开头，守不住中段，结尾草草收。长结构需要计划，它没有计划。分段生成把控制权拿回来：四分钟按 8–12 段切，每段 16–32 小节，单独写提示、单独生成，再到边界上拼。

## 为什么会裂

接缝暴露的是三个参数：速度、调性、混响。两段差 2 BPM，三十秒后就能听出来；调性差一个全音，接上去像换了一首歌；前段尾巴混响 2.5 秒、后段 0.8 秒，交界处会突然变干。最稳的接法是边界落在主和弦上，前段收束、后段同调同速进入。

## 怎么接

先画段落表：每段的小节数、调性、配器、情绪。写提示时带上相邻段的信息，例如「90 BPM，D 小调，弦乐铺底，结尾停在 A 和弦」。拼接留 2 小节重叠，交叉淡化 200–500 毫秒；氛围段落可以放到 1 秒。硬切只用于明确对比，比如从室内乐切到电子鼓。

## 听什么

在变奏乐章里听段落性格的差异，在回旋曲里听主题与插部的边界，在里尔舞曲里听重复段落的接缝。分段做得好，听不出哪一段是单独生成的；做得不好，每次进副歌都像换台。

```audiolab
{"type":"progression","key":"C","chords":["C","Am","F","G"],"label":"段落边界的和声","label_en":"Harmony at a section boundary","hint":"边界落在稳定和弦上，接缝才不刺耳","hint_en":"A seam is quietest when it lands on a stable chord"}
```
:::

::: en
## Where it breaks

Ask for four minutes in one pass and the model gives you an opening, loses the middle and rushes the end. Long form needs a plan; it has none. Generate in sections instead: cut four minutes into 8–12 sections of 16–32 bars, prompt each one, then stitch at the boundaries.

## Why the seams show

Three parameters give a seam away: tempo, key and reverb. Two BPM of drift is audible after thirty seconds; a whole tone of key change sounds like another song; a 2.5-second tail meeting a 0.8-second tail goes abruptly dry. The safest join lands on the tonic chord, with the first section closing and the next entering in the same key and tempo.

## How to stitch

Draw a section table first: bars, key, instrumentation, mood. Include the neighbouring section in each prompt, for example "90 BPM, D minor, strings underneath, ending on an A chord". Overlap two bars at the join and crossfade 200–500 ms; atmospheric sections can take a full second. Save hard cuts for deliberate contrast, such as chamber music into electronic drums.

## What to listen for

In a variation movement, the change of character between sections; in a rondo, the boundaries of theme and episode; in a reel, the joins between repeats. Good section work leaves no clue about which part was generated alone. Bad section work sounds like changing stations at every chorus.

```audiolab
{"type":"progression","key":"C","chords":["C","Am","F","G"],"label":"段落边界的和声","label_en":"Harmony at a section boundary","hint":"边界落在稳定和弦上，接缝才不刺耳","hint_en":"A seam is quietest when it lands on a stable chord"}
```
:::
