---
id: prompt-anatomy
site: ai
cat: B
title: 提示词结构
title_en: The Anatomy of a Prompt
summary: 好的提示像编曲说明：风格、编制、速度、情绪、结构，缺一不可。
summary_en: A good prompt reads like an arrangement brief: style, instrumentation, tempo, mood and form.
level: standard
tags: [提示词, 结构, 生成, 工作流]
tags_en: [prompt, structure, generation, workflow]
alias: [提示词, prompt, 提示结构]
order: 1
links:
  - "[[glossary:tempo]]"
  - "[[glossary:timbre]]"
  - "[[glossary:daw]]"
instances:
  - thesession-006629 | 爱尔兰曲调，简短提示能否抓住风格与乐器（C1）
  - atepp-000124 | 德彪西三度练习曲，和声色彩的描述难度（C1）
  - groove-000002 | 86 BPM 灵魂乐鼓组，速度与律动的描述方式（C1）
sources:
  - 文本条件的表达方式，依生成模型公开说明核对，未抄原文
  - 编曲说明的常见要素，依制作实践通识核对，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

"写一首好听的歌"这样的提示，模型只能猜。提示词的作用是把模糊的想象压缩成可执行的方向。写得太短，结果随机；写得太长，约束互相矛盾，模型只能挑一部分执行。

## 结构

一个可用的提示通常包含五层：风格与年代、编制与乐器、速度与节拍、情绪与力度、结构与长度。先写前两层确定骨架，再补后三层确定细节。参考曲目是有效的手段，但要说明参考的是哪一方面：音色、节奏还是编排。排除项单独写，别混在正面描述里。

## 做法

一次只改一个变量，才能知道是哪一句起了作用。把有效提示存成模板，按项目复用。结构复杂的曲子分段生成，每段单独写提示。提示里少用抽象形容词，多用具体的乐器与节奏描述。生成后记录提示与结果的对应关系，积累自己的词表。

## 听什么

在传统曲调里听简短提示的成败，在德彪西练习曲里听和声色彩能否被语言描述，在灵魂乐鼓组里听速度与律动的关系。提示写得好，结果的可预期性会明显提高。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":86,"label":"提示里的速度","label_en":"Tempo inside a prompt","hint":"速度写清楚，生成结果才不会忽快忽慢","hint_en":"State the tempo and generations stop drifting in speed"}
```
:::

::: en
## The problem

A prompt like "write a good song" leaves the model guessing. A prompt compresses a vague idea into an executable direction. Too short and results are random; too long and constraints contradict, so the model follows only some of them.

## Structure

A workable prompt carries five layers: style and era, instrumentation, tempo and metre, mood and dynamics, form and length. Write the first two to fix the skeleton, then the rest to fix detail. Reference tracks help, but say which aspect you mean: timbre, rhythm or arrangement. Keep exclusions separate from positive description.

## Practice

Change one variable at a time so you learn which sentence did the work. Save working prompts as templates and reuse them across projects. Generate complex pieces section by section with a prompt for each. Prefer concrete instrument and rhythm words over abstract adjectives. Record prompt and result pairs to build your own vocabulary.

## What to listen for

In the traditional tune, whether a short prompt lands; in the Debussy étude, whether harmonic colour can be described in words; in the soul kit, how tempo and feel interact. Better prompts make results noticeably more predictable.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":86,"label":"Tempo inside a prompt","label_en":"Tempo inside a prompt","hint":"State the tempo and generations stop drifting in speed","hint_en":"State the tempo and generations stop drifting in speed"}
```
:::
