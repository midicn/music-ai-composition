---
id: ai-for-film-scoring
site: ai
cat: F
title: 影视配乐
title_en: AI for Film Scoring
summary: AI 能出 temp 和短 cue，长片的结构与主题仍要人来写
summary_en: AI can draft temp scores and short cues; long arcs and themes still need a composer
level: standard
tags: [影视配乐, 临时音轨, 主题发展, 导演沟通]
tags_en: [film scoring, temp score, thematic development, director notes]
alias: [影视配乐, 电影配乐, film scoring]
order: 1
links:
  - "[[glossary:cue]]"
  - "[[glossary:stems]]"
instances:
  - pdmx-000160 | 固定音型加独奏小提琴写场面，临时音轨常用的方向参考（C1）
  - pdmx-000180 | 四音动机贯穿全曲，生成工具给不出这种长线（C1）
  - pdmx-001524 | 同一材料靠速度与配器推进，短 cue 的范本（C1）
  - pdmx-001010 | 一个乐章铺十分钟情绪，AI 很难维持这种长弧（C1）
sources:
  - 影视配乐流程的阶段划分，依公开的配乐访谈与制作通识核对，未抄原文
  - Film scoring workflow stages, checked against public interviews and general practice, not copied
updated: 2026-10-30
---

::: zh
## 问题

导演丢来三段别的电影的音乐，说"要这种感觉"。真正要写的是四十分钟的片子，情绪要随剧情转向，主题要在结尾回来。让 AI 生成一段音乐很快，难的是这些段落之间的关系。

## 原理

生成模型擅长在给定描述下产出一段自洽的两三分钟音乐，配器合理、情绪明确、结尾能收。它不擅长三件事，跨场景的主题发展、按画面长度精确伸缩、以及和导演来回修改时保持一致。原因是每次生成都是独立的，模型没有贯穿全片的记忆，也没法记住上一版里那个被否掉的低音。

## 做法

把工作拆开。每场的入点、出点和大致长度先标在时间线上，再决定哪一段交给生成。前期用 AI 做 temp score，一场戏生成三五个方向，用来和导演对齐语言，这些文件不进最终版。定稿阶段把配乐拆成主题、织体、节奏三层，主题自己写或自己改，AI 只负责铺底、变奏草稿和过渡段。十秒到一分钟的短 cue 可以整段生成再修，长段落必须有人搭结构。导演给的参考要翻译成具体参数，配器、音区、密度、有没有打击，而不是继续用形容词来回猜。

## 听什么

在《骷髅之舞》里听一个固定音型怎样撑住整段画面，在贝多芬第五开头听四音动机怎样被压缩和扩展，在格里格的《在山妖的洞窟中》里听同一材料靠速度和配器完成短 cue 的推进，在马勒第五里听一个乐章怎样把情绪铺到十分钟以上。前三个方向 AI 能给出可用的草稿，最后一个只能人来搭。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","A4","G4","E4","D4","C4"],"label":"一个动机的骨架","label_en":"The skeleton of a motif","hint":"问这四个音能不能撑四十分钟，而不是四小节","hint_en":"Ask whether these four notes can carry forty minutes, not four bars"}
```
:::

::: en
## The problem

A director sends three cues from other films and says "that feeling". What has to be written is forty minutes of film, with the mood turning as the plot turns and the theme returning at the end. Generating one cue with AI is quick; what is hard is the relationship between cues.

## How it works

Generation models are good at producing two or three self-consistent minutes from a description, with sensible orchestration, a clear mood and an ending that closes. They are bad at three things, thematic development across scenes, stretching or compressing to picture length, and staying consistent through rounds of director notes. Each generation is independent; the model carries no memory of the whole film and cannot remember the bass line that was rejected two versions ago.

## Practice

Split the work. Mark each scene's in point, out point and rough length on the timeline before deciding which part goes to generation. Use AI for temp scores early, generating three or four directions per scene to align vocabulary with the director, and keep those files out of the final. At the final stage separate the score into theme, texture and rhythm; write or rewrite the theme yourself and let AI supply beds, variation drafts and transitions. A short cue of ten seconds to a minute can be generated whole and then fixed. A long sequence needs someone to build its structure. Translate the director's references into concrete parameters, instrumentation, register, density, whether there is percussion, instead of trading adjectives.

## What to listen for

In Danse macabre, how one ostinato holds a whole scene together; in the opening of Beethoven's Fifth, how a four-note cell is compressed and extended; in Grieg's In the Hall of the Mountain King, how a single idea is pushed by tempo and orchestration through a short cue; in Mahler's Fifth, how one movement sustains a mood past ten minutes. AI can draft the first three. The last one has to be built by a person.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","A4","G4","E4","D4","C4"],"label":"The skeleton of a motif","label_en":"The skeleton of a motif","hint":"Ask whether these four notes can carry forty minutes, not four bars","hint_en":"Ask whether these four notes can carry forty minutes, not four bars"}
```
:::
