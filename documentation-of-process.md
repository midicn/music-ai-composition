---
id: documentation-of-process
site: ai
cat: H
title: 过程记录
title_en: Documenting the Process
summary: 把工具、版本、提示词、种子和改动写下来，结果才站得住
summary_en: Log tool, version, prompt, seed and edits so the result can be defended.
level: standard
tags: [记录, 提示词, 种子, 流程]
tags_en: [documentation, prompts, seeds, process]
alias: [过程记录, 制作日志, process log]
order: 8
links:
  - "[[glossary:diffusion]]"
  - "[[glossary:midi-protocol]]"
  - "[[glossary:daw]]"
instances:
  - atepp-001875 | 巴赫三声部创意曲，任何改动都会被听出来（C1）
  - groove-000000 | 一百三十八拍鼓循环，参数直接决定结果（C1）
  - atepp-001283 | 肖邦夜曲，自由速度与触键的决定需要文字记录（C1）
  - pdmx-000153 | 二十六分钟长曲，偏差按时间码累积（C1）
sources:
  - 制作日志与生成记录的最小字段集，依制作实务通识归纳，未抄原文
  - 工具版本与参数的记录方式，依公开工具文档核对，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

六周后客户问这条曲子怎么做的，或者权利方问有没有用某个模型，聊天记录已经没了，工具更新了，记忆也不可靠。没有记录，结果就无法辩护，也无法复现。过程记录不是给审计看的，它是给未来的自己和接手的人看的。

## 记什么

一条生成记一行，日期、操作人、工具与精确版本、模型、提示词原文、负面提示、种子、时长、速度、调性、参考音频及其授权、生成参数、候选数量、选中理由。后期也要记，替换了哪个音、谁改的、为什么。用到的采样、循环、人声，记来源与授权。最后记输出文件的校验值和存放位置。失败的尝试同样要记，它解释了为什么没走那条路，也防止下一个人重做。

## 怎么记

放在项目文件夹里，纯文本或 CSV，一行一条，生成完立刻写，不要凭记忆补。设置界面可以截图，但文字才能搜索。提示词存成与渲染同名的 txt，不要只留在网页里。团队项目加两列，谁改的、什么时候。记录不必好看，能查就行，字段固定比格式漂亮重要。判断标准很简单，另一个人拿到这份记录，能不能按步骤做出一个可辩护的结果，哪怕不是一模一样。

## 听什么

在巴赫三声部创意曲里听三个声部，任何一处改动都能被听出来，所以改动必须写清。在一百三十八拍的放克循环里听参数如何直接决定结果，速度、拍号、节奏型都该进记录。在肖邦夜曲里听自由速度与触键这些决定，文字不记就消失。在二十六分钟的托卡塔里听长曲目里偏差如何累积，记录要按时间码分段。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"e e e e e e e e","bpm":84,"label":"一份能重放的记录","label_en":"A record someone can replay","hint":"拍号、速度、节奏型写在文件里，别人才能照做","hint_en":"Metre, tempo and pattern written down let another person repeat it"}
```
:::

::: en
## The problem

Six weeks later a client asks how the track was made, or a rights holder asks whether a certain model was used. The chat log is gone, the tool has updated and memory is unreliable. Without a record the result cannot be defended or reproduced. Documentation is not for auditors; it is for your future self and whoever takes over.

## What to log

One row per generation, date, operator, tool and exact version, model, prompt verbatim, negative prompt, seed, duration, tempo, key, reference audio and its licence, settings, number of candidates and why one was chosen. Log post work too, which note was replaced, by whom and why. Log samples, loops and voices with source and licence. Log the hash and location of each output. Log failures as well; they explain why a path was abandoned and stop the next person from repeating it.

## How to log

Keep it in the project folder as plain text or CSV, one row per generation, written immediately rather than from memory. Screenshots of settings are acceptable, but text is searchable. Save the prompt as a txt file named after the render, not only in a web page. For teams add two columns, who changed it and when. The record need not be pretty, only searchable; fixed fields matter more than formatting. The test is simple, can another person follow the record and produce a defensible result, even if not an identical one.

## What to listen for

In Bach's three-part invention, every edit is audible because three voices expose it, so every edit must be written down. In the 138 BPM funk loop, parameters decide the result directly, so tempo, metre and pattern belong in the record. In the Chopin nocturne, rubato and touch are decisions that vanish without notes. In the twenty-six minute Toccata, drift accumulates, so the log needs timecodes.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "e e e e e e e e", "bpm": 84, "label": "A record someone can replay", "label_en": "A record someone can replay", "hint": "拍号、速度、节奏型写在文件里，别人才能照做", "hint_en": "Metre, tempo and pattern written down let another person repeat it"}
```
:::
