---
id: seed-and-reproducibility
site: ai
cat: C
title: 种子与可复现
title_en: Seeds and Reproducibility
summary: 记下种子与全部参数，但别指望两次生成完全一样
summary_en: Log the seed and every parameter, but do not expect two runs to match exactly.
level: standard
tags: [种子, 复现, 参数记录, 版本]
tags_en: [seed, reproducibility, parameter log, versions]
alias: [可复现性, 随机种子, reproducibility]
order: 11
links:
  - "[[glossary:daw]]"
  - "[[glossary:midi-protocol]]"
  - "[[glossary:stems]]"
instances:
  - atepp-002443 | 《哥德堡变奏曲》咏叹调回归，同一材料再弹也不全同（C1）
  - giantmidi-000014 | 科普兰《帕萨卡利亚》，固定低音反复中保留身份（C1）
  - groove-000005 | 87 BPM 嘻哈鼓组，短循环里听每一遍是否有微差（C1）
  - thesession-015842 | 民歌《鸟儿已去》，AABB 反复，听第二遍的变化（C1）
sources:
  - 生成参数与随机种子的作用，参考公开模型文档。
  - 版本更新导致结果漂移的现象；制作实践是主要依据。
updated: 2026-10-30
---

::: zh
## 哪里不对

调出一个满意的结果，第二天想再要一版，参数照抄，结果却不一样。种子只是众多变量之一，把它当成唯一开关，复盘就会落空。更麻烦的是，有些服务根本不提供种子，只给一个重新生成的按钮。

## 机制上的解释

结果由模型版本、权重、采样设置、提示文本、参考音频与处理顺序共同决定。服务在后台更新后，旧种子指向的是新的分布。即使这些全部冻结，浮点运算在不同显卡上也可能给出微小差异，再经过多轮迭代放大成可听的不同。真正稳定的只有符号类输出，音符写下来就是写下来了。同一段提示放在不同长度的批次里，切分位置不同，结果也会不同。

## 怎么修

每次生成都记一份日志，写清日期、工具与版本、模型名、种子、步数、引导强度、时长、提示原文、参考文件与输出文件名。日志和被采纳的那一版音频放在一起，隔几个月还能对上。日志用纯文本写，和工程文件放在同一目录，交接时别人也能读懂。要长期复现，就把满意的结果导出成分轨或 MIDI，把生成物转成可编辑资产，别把可复现性押在服务上。重生成时一次只动一个变量，并保留对照版本，这样即使不能完全重复，也能说清是哪一步改变了结果。

## 耳朵要抓的点

在咏叹调回归里听同一材料再出现时的差异，在《帕萨卡利亚》里听固定低音反复中保留的身份，在嘻哈鼓组循环里听每一遍的微差，在民歌反复里听第二遍的变化。听过这些，就不会把不一样当成失败。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":87,"label":"同一循环再放一遍","label_en":"The same loop played again","hint":"差别常在几毫秒里，不在音符上","hint_en":"The difference lives in milliseconds, not in the notes"}
```
:::

::: en
## What is off

You tune a result you like, ask for another version the next day with the same settings copied across, and get something else. The seed is only one variable among many, and treating it as the single switch makes any later review collapse. Worse, some services offer no seed at all, only a regenerate button.

## The mechanism explains it

A result is decided by model version, weights, sampling settings, prompt text, reference audio and processing order together. Once a service updates in the background, an old seed points into a new distribution. Even with all of that frozen, floating-point arithmetic on different cards can yield small differences that repeat after repeat turns audible. Only symbolic output stays stable, because a written note stays written. The same prompt placed in batches of different length is also cut at different points and returns different results.

## How to fix it

Keep a log for every run, recording the date, tool and version, model name, seed, steps, guidance strength, duration, the prompt as written, any reference file and the output filename. Store the log beside the take you accepted so the pair still matches months later, and keep it in plain text beside the project file so a collaborator can read it. For long-term reproduction, export the accepted result as stems or MIDI and turn the generation into an editable asset, rather than staking reproducibility on the service. When regenerating, move one variable at a time and keep a control version, so that even without an exact repeat you can say which step changed the outcome.

## What the ear catches

In the aria's return, the difference when the same material comes back; in the Passacaglia, the identity kept through a repeating bass; on the hip-hop kit, the small wobble between one pass of the loop and the next; in the folk tune's repeats, how the second pass differs. After hearing these, an inexact match stops looking like failure, since an exact match is the exception and a documented approach is the rule.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":87,"label":"The same loop played again","label_en":"The same loop played again","hint":"The difference lives in milliseconds, not in the notes","hint_en":"The difference lives in milliseconds, not in the notes"}
```
:::
