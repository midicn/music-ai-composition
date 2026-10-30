---
id: iterative-refinement
site: ai
cat: B
title: 迭代修改
title_en: Iterative Refinement
summary: 一次生成靠运气，迭代靠方法：每次只改一个变量，并保留上一版。
summary_en: One generation is luck; iteration is method, changing one variable at a time and keeping the last version.
level: standard
tags: [迭代, 修改, 版本, 工作流]
tags_en: [iteration, revision, versioning, workflow]
alias: [迭代, 往复修改, iteration]
order: 6
links:
  - "[[glossary:timbre]]"
  - "[[glossary:tempo]]"
  - "[[glossary:daw]]"
instances:
  - atepp-001115 | 肖邦叙事曲，主题需要逐步打磨才成形（C1）
  - groove-000004 | 84 BPM 放克鼓组，鼓型可以通过逐次微调逼近目标（C1）
  - thesession-006629 | 爱尔兰曲调，装饰音的加入需要反复试（C1）
sources:
  - 迭代式创作的常见流程，依设计实践公开资料核对，未抄原文
  - 版本管理的基本方法，依工程实践通识核对，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

第一次生成往往"差一点"，于是改提示再生成，结果又偏到另一个方向。没有方法的迭代会陷入来回摆荡：修好了高频，低频又不对；换回旧参数，问题全回来。

## 原理

生成是多参数耦合的，改一句话可能同时影响音色、结构与情绪。控制变量的办法是一次只改一项，改完立刻对比。保留每一版的提示、种子与输出，才有回退的可能。判断也要分层：先定结构，再定配器，最后修音色，顺序反了会白费工夫。

## 做法

建立一个简单的版本表，记录编号、改动与结论。每次只改一个变量，听完再决定保留还是回退。结构问题用重新生成解决，音色问题用后期处理解决，别混在一起。连续三次没有改善就停下来，重新审视需求而不是继续抽卡。

## 听什么

在叙事曲里听主题如何逐版成形，在鼓组里听每次微调带来的变化，在传统曲调里听装饰音加入的时机。迭代的价值在于每一步都可解释。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","F4","G4","F4","E4","D4"],"label":"逐版微调的旋律","label_en":"A line refined version by version","hint":"每次只改一个音或一处力度，听差别是否朝目标靠近","hint_en":"Change one note or dynamic per pass, and hear whether it moves toward the target"}
```
:::

::: en
## The problem

The first generation is usually "almost right", so you edit the prompt and generate again, and it swings somewhere else. Iteration without method oscillates: fix the top end and the low end goes wrong; restore the old settings and every problem returns.

## How it works

Generation couples many parameters, so one changed sentence can alter timbre, structure and mood at once. Control variables by changing one thing per pass and comparing immediately. Keep prompt, seed and output for every version so you can go back. Judge in layers: structure first, instrumentation next, timbre last, since the reverse order wastes effort.

## Practice

Keep a simple version table recording number, change and conclusion. Change one variable per pass and decide whether to keep or revert after listening. Solve structural problems by regenerating and timbral problems in post, never mixed together. After three passes without improvement, stop and re-examine the brief instead of drawing more samples.

## What to listen for

In the ballade, how a theme takes shape across versions; in the kit, what each nudge changes; in the folk tune, when ornaments enter. Iteration is worth it when every step can be explained.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","F4","G4","F4","E4","D4"],"label":"A line refined version by version","label_en":"A line refined version by version","hint":"Change one note or dynamic per pass, and hear whether it moves toward the target","hint_en":"Change one note or dynamic per pass, and hear whether it moves toward the target"}
```
:::
