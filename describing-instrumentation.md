---
id: describing-instrumentation
site: ai
cat: B
title: 描述配器
title_en: Describing Instrumentation
summary: 说清谁在演奏、怎么演奏、占多大比重，比说"丰富"有用得多。
summary_en: Say who plays, how they play and how much space they take, which beats saying "rich".
level: standard
tags: [配器, 提示, 织体, 描述]
tags_en: [instrumentation, prompt, texture, description]
alias: [描述配器, 编制描述, instrumentation]
order: 3
links:
  - "[[glossary:timbre]]"
  - "[[glossary:register]]"
  - "[[instrument:violin]]"
instances:
  - musicnet-000067 | 弦乐四重奏，四件乐器的分工是配器描述的最好范例（C1）
  - atepp-005385 | 拉威尔《绞刑架》，钢琴织体的层次如何被语言还原（C1）
  - cyberhymnal-008729 | 管风琴赞美诗，单件乐器的多声部织体（C1）
sources:
  - 配器描述的常用维度，对照配器教材公开说明整理。
  - 织体密度与音区的关系（管弦乐法惯例）。
updated: 2026-10-30
---

::: zh
## 问题

"弦乐铺底，铜管加入，最后全奏"这种描述，人看得懂，模型不一定。它需要知道谁在演奏、在哪个音区、占多大比重、什么时候进出。配器描述的核心不是列乐器名单，而是画出一张织体图。

## 结构

三层就够：主奏声部、支撑声部、装饰或节奏层。每层写清乐器、音区、力度与进出时间。比重用相对说法，如"弦乐为主，钢琴点缀"。音区用具体说法，如"低音区的大提琴"比"低沉的弦乐"更可控。需要留白时明确说"前八小节只有钢琴"。

## 做法

先写骨架再写细节：先定几件乐器，再加演奏法与音区。避免同时列出十几件乐器，模型会平均分配导致没有重点。用"逐渐加入"描述层次推进。写完后自己读一遍，看能否在脑中听到大概的样子。生成后对照描述逐项检查，缺哪层补哪层。

## 听什么

在四重奏里听四件乐器如何分工，在《绞刑架》里听钢琴织体的层次，在管风琴里听单件乐器的多声部。配器描述越具体，生成结果越接近想象。

```audiolab
{"type":"instrument","gm":"String Ensemble 2","synth":"bowed","phrase":["A3","E4","A4","C5","B4","A4","E4","A3"],"label":"弦乐铺底与上方旋律","label_en":"A string bed with a line above","hint":"分层描述时，听底层与旋律层是否各占其位","hint_en":"With layered description, hear whether bed and melody each hold their place"}
```
:::

::: en
## The problem

"Strings underneath, brass enters, full tutti at the end" is clear to a person but not necessarily to a model. It needs to know who plays, in which register, taking how much space, entering when. Describing instrumentation is not listing instruments but drawing a texture map.

## Structure

Three layers are enough: lead, support, and decorative or rhythmic. For each, name the instrument, register, dynamic and entry time. Give weight relatively, as in "strings lead, piano punctuates". Be concrete about register: "cello in the low register" is more controllable than "dark strings". When space matters, say so: "piano alone for the first eight bars".

## Practice

Write the skeleton before detail: fix a few instruments, then add technique and register. Avoid listing a dozen instruments at once, since the model spreads them evenly and loses focus. Use "enters gradually" to describe layering. Read the prompt back and check whether you can hear roughly what you meant. After generation, compare layer by layer and add what is missing.

## What to listen for

In the quartet, how four instruments divide roles; in Le gibet, the layers of piano texture; in the organ, many voices from one instrument. The more concrete the description, the closer the result.

```audiolab
{"type":"instrument","gm":"String Ensemble 2","synth":"bowed","phrase":["A3","E4","A4","C5","B4","A4","E4","A3"],"label":"A string bed with a line above","label_en":"A string bed with a line above","hint":"With layered description, hear whether bed and melody each hold their place","hint_en":"With layered description, hear whether bed and melody each hold their place"}
```
:::
