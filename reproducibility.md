---
id: "reproducibility"
site: "ai"
cat: "H"
title: "可复现"
title_en: "Reproducibility"
summary: "能复现的是流程与决策，不是波形"
summary_en: "What reproduces is the process and the decisions, not the waveform."
level: "standard"
tags: ["复现", "种子", "模型版本", "配方"]
tags_en: ["reproducibility", "seeds", "model version", "recipe"]
alias: ["可复现", "复现测试", "reproducibility"]
order: 9
links: ["[[glossary:diffusion]]", "[[glossary:sample-rate]]"]
instances: ["pdmx-000153", "atepp-002965", "groove-000000", "atepp-000075"]
sources: ["https://docs.pytorch.org/docs/2.15/notes/randomness.html", "生成式模型的随机性与版本漂移（机器学习公开资料）。", "复现测试的容差与记录方式，参考工程实践惯例。"]
updated: "2026-11-03"
---

::: zh
## 问题

AI 音乐的复现要求应先写清：是输出文件完全相同、同一环境中可重复生成，还是足够相近以便继续编辑。在线服务可能更新模型或隐藏设置，本地流程则可能固定更多条件。无论采用哪种方式，输出音频都应独立保存，不能只留下提示词。

## 为什么复现不了

种子控制随机数起点，不会自动固定模型权重、预处理、运算精度和非确定性算子。本地流程有时可以配置为确定性计算；在线服务没有暴露的设置，应写成未知。跨版本或硬件是否仍可复现，需要单独验证，不应一概说“只能复现流程，不能复现波形”。

## 配方与测试

记录工具版本、检查点、完整输入、可见参数、参考素材校验值与后期步骤，并保存每次输出。为任务预先确定接受条件：研究试验可能要求文件校验一致，配乐修改可能只要求旋律、长度和段落可重建。重复生成差异较大时，可改用已冻结音频继续编辑，或选择控制能力更适合任务的流程。

## 听什么

选一段有明确输入和设置的生成任务，保留三次输出，再比较文件校验值、长度、段落边界和听感。若文件不同，先确定任务需要逐位一致还是可继续编辑的近似版本。原有托卡塔、奏鸣曲和鼓组 MIDI 不是同一模型重复推理的结果，不能用它们验证随机种子或生成漂移。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":120,"label":"固定节奏参照","label_en":"Fixed-pattern reference","hint":"重复播放同一节奏只说明播放器再次读取固定数据，不等于模型重复推理得到了同一输出。","hint_en":"Repeating a fixed pattern shows playback of fixed data, not identical output from repeated model inference."}
```
:::

::: en
## The problem

Define reproduction first: identical output files, repeatable generation in one environment, or a result similar enough for further editing. Online services may update models or hide settings; local pipelines may expose more controls. In every case, preserve output audio rather than prompts alone.

## Why it fails

A seed fixes a random-number starting point, not weights, preprocessing, precision or nondeterministic operations. Local pipelines can sometimes use deterministic computation; unexposed service settings should be recorded as unknown. Reproduction across versions or hardware needs a separate test rather than a blanket claim that waveforms cannot be reproduced.

## Recipe and testing

Record tool version, checkpoint, complete inputs, visible settings, reference checksums and later processing, retaining every output. Set acceptance conditions for the task: research may need identical checksums, while score revision may need reconstructable melody, duration and sections. If regeneration varies too much, edit frozen audio or choose a workflow with more suitable controls.

## What to listen for

Run one clearly specified generation task three times, retain the files, and compare checksums, length, section boundaries and listening results. If files differ, decide whether the job needs bit identity or a sufficiently similar editable version. The linked toccatas, sonata and drum MIDI are not repeated outputs from one model and cannot test seeds or generation drift.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":120,"label":"Fixed-pattern reference","label_en":"Fixed-pattern reference","hint":"Repeating a fixed pattern shows playback of fixed data, not identical output from repeated model inference.","hint_en":"Repeating a fixed pattern shows playback of fixed data, not identical output from repeated model inference."}
```
:::

