---
id: reproducibility
site: ai
cat: H
title: 可复现
title_en: Reproducibility
summary: 能复现的是流程与决策，不是波形
summary_en: What reproduces is the process and the decisions, not the waveform.
level: standard
tags: [复现, 种子, 模型版本, 配方]
tags_en: [reproducibility, seeds, model version, recipe]
alias: [可复现, 复现测试, reproducibility]
order: 9
links:
  - "[[glossary:diffusion]]"
  - "[[glossary:sample-rate]]"
instances:
  - pdmx-000153 | 二十六分钟长文件，微小偏差会累积成结构差异（C1）
  - atepp-002965 | 巴赫 D 大调托卡塔，自由段落难以从参数还原（C1）
  - groove-000000 | 一百三十八拍鼓循环，参数确定但音色未必复现（C1）
  - atepp-000075 | 斯克里亚宾第二奏鸣曲，自由速度无法被配方穷尽（C1）
sources:
  - 生成式模型的随机性与版本漂移，依机器学习公开资料核对，未抄原文
  - 复现测试的容差与记录方式，依工程实践通识归纳，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

同样的提示词、同样的种子，应该得到同样的结果，这句话在 AI 音乐里经常不成立。采样有随机性，模型会更新，服务端的前处理看不见，参考音频换一个文件就全变。追求逐位相同的音频，多数时候是浪费时间；但完全不可复现，又会让修改和授权都失去依据。

## 为什么复现不了

三个原因。第一，生成过程本身带随机采样，种子只固定一部分。第二，模型和推理服务会升级，同一个名字背后已经是另一套权重。第三，输入不止提示词，还有参考音频、时长、隐藏参数，任何一项变了，结果就分叉。所以能复现的是流程与决策，不是波形。把这两件事分开，才谈得上方法。

## 配方与测试

一份有用的配方包含工具与版本、模型、提示词原文、负面提示、种子、时长、速度、调性、参考音频的校验值与授权、输入 MIDI 或音频、候选数量、筛选标准、后期链，再加一行已知的未知项。每个项目做一次复现测试，同一配方连跑三次，比较时长、段落边界、频谱差异与盲听结果，把容差写下来，比如结构一致、音色有浮动。客户项目优先选能固定种子的工具；存档时冻结输出文件，不要指望冻结服务。如果三次结果差异很大，就把这条工具从客户项目的候选里去掉。

## 听什么

在二十六分钟的托卡塔里听长文件如何让微小偏差累积成结构差异。在巴赫 D 大调托卡塔里听自由段落，哪些决定根本无法从参数还原。在一百三十八拍的放克循环里听参数确定的部分，节奏型与速度可以照做，音色未必。在斯克里亚宾第二奏鸣曲里听自由速度，演奏本身就不能被配方穷尽。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":120,"label":"同样的参数，未必同样的结果","label_en":"Same settings, not always the same result","hint":"节奏型与速度可以复现，模型的采样未必","hint_en":"Pattern and tempo repeat; the model's sampling may not"}
```
:::

::: en
## The problem

The same prompt and the same seed should give the same result, except in AI music they often do not. Sampling is stochastic, models update, server-side preprocessing is invisible, and changing one reference file changes everything. Chasing a bit-identical waveform is usually wasted time, but a result that cannot be reproduced at all cannot be revised or defended.

## Why it fails

Three reasons. The generation process samples randomly, and a seed fixes only part of it. Models and inference services are upgraded, so the same name now hides different weights. Inputs include more than the prompt, namely reference audio, duration and hidden settings, and changing any one forks the result. What can be reproduced is the process and the decisions, not the waveform. Separating the two is the whole method.

## Recipe and testing

A useful recipe lists tool and version, model, prompt verbatim, negative prompt, seed, duration, tempo, key, hash and licence of the reference audio, input MIDI or audio, number of candidates, selection criteria, post chain, and a line of known unknowns. Test once per project, run the same recipe three times and compare duration, section boundaries, spectral difference and a blind listen, then write down the tolerance, for example same structure with timbral drift. Prefer tools that expose seeds for client work; for archives, freeze the output rather than trusting the service. If three runs differ wildly, drop that tool from the candidate list for client work.

## What to listen for

In the twenty-six minute Toccata, how small deviations accumulate into structural differences over a long file. In Bach's Toccata in D major, free passages whose decisions cannot be recovered from parameters. In the 138 BPM funk loop, the part that is determined, since pattern and tempo can be repeated but timbre may not. In Scriabin's Second Sonata, rubato that no recipe can exhaust.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "s s s s s s s s s s s s s s s s", "bpm": 120, "label": "Same settings, not always the same result", "label_en": "Same settings, not always the same result", "hint": "节奏型与速度可以复现，模型的采样未必", "hint_en": "Pattern and tempo repeat; the model's sampling may not"}
```
:::
