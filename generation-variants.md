---
id: generation-variants
site: ai
cat: C
title: 生成变体
title_en: Generating Variants
summary: 批量生成再挑选，比一直改一版更快，也更容易看清方向
summary_en: Generate many, choose fast, then refine only the winner; the comparison is the real work.
level: standard
tags: [批量生成, 变体, 筛选, 判断]
tags_en: [variants, batch generation, selection, judgement]
alias: [批量出片, 多版本对比, variants]
order: 1
links:
  - "[[glossary:tempo]]"
  - "[[glossary:timbre]]"
  - "[[glossary:midi-protocol]]"
instances:
  - atepp-000591 | 舒伯特即兴曲主题加变奏，听同一乐思靠什么被认出来（C1）
  - atepp-000115 | 韦伯恩钢琴变奏曲，每个变奏只动一两个参数（C1）
  - groove-000005 | 87 BPM 嘻哈鼓组，同一鼓型多次生成的细微差别（C1）
  - giantmidi-002518 | 摇摆低音变奏曲，听装饰变奏与结构变奏的区别（C1）
sources:
  - 生成变体的筛选方法（设计迭代实践惯例）。
  - 批量生成与挑选的流程，参考制作实践惯例。
updated: 2026-10-30
---

::: zh
## 难在哪

先把一版改到完美，是很多人的默认做法，在生成工具上通常最慢。模型每次输出都带随机性，方向不对时，改细节只是在一个错的答案上打磨。另一种失败更隐蔽，第一版刚好不错，于是不敢再生成，后面所有修改都围着这一版打转。

## 背后的原理

变体把评价和修改拆开。同一提示跑多次，差别来自种子。改一个词再跑，差别来自那个词。两种要分开做，混在一起就分不清变化是谁带来的。判断也分层，先看段落结构和律动对不对，再看配器，最后才看音色细节，因为前两层不对时，后面的精修没有意义。数量也不是越多越好，超过自己能审听的上限，判断就会变糊。

## 具体做法

第一轮只跑六到八个，每个听完写一句结论，例如结构对、主音色太亮。记录提示原文、种子、时长和这句结论，缺了种子，下一轮就无法只在选中的方向附近微调。第二轮从最好的那一版出发，只改一个变量，再跑三到五个。每一批之内不要改提示，否则同批样本之间无法比较。停止的条件有两个，连续两轮没有出现新方向，或者当前最好的一版已经能满足交付。

## 耳朵要抓的点

在舒伯特即兴曲的主题与变奏里，听同一个乐思靠什么被认出来，变奏改的是织体、和声还是音区。在韦伯恩的钢琴变奏曲里，听每个变奏只动一两个参数时整体还成不成立。在 87 BPM 的嘻哈鼓组里，听同一鼓型多次生成后底鼓位置与镲片密度的细微差别，这类差别正是第一轮筛选要抓的东西。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"T s s s T s s s T s s s T s s s","bpm":87,"label":"用来比对的一版","label_en":"One take to compare against","hint":"先记住这一版，再听下一版差在哪里","hint_en":"Fix this take in memory, then hear what the next one changes"}
```
:::

::: en
## Where it gets hard

Perfecting one take first is the default habit and usually the slowest path with a generative tool. Every run carries randomness, so when the direction is wrong, refining detail is polishing a wrong answer. The other failure is quieter: the first take happens to be decent, so you stop generating and every later decision circles that one version. Both extremes waste the same resource, your attention.

## The principle

Variants separate judgement from revision. Running the same prompt repeatedly varies the seed; changing one word varies that word. Keep the two kinds in separate rounds or you cannot tell which change caused what. Judge in layers too: form and groove first, instrumentation next, timbre last, since polish on a wrong form is wasted effort. More takes is not automatically better; past the number you can actually audition, judgement blurs.

## In practice

Run six to eight takes in the first round and write one sentence on each, for example form right and lead too bright. Log the prompt text, seed, length and that sentence; without the seed you cannot refine around the winner. In the second round start from the best take, change one variable and run three to five more. Do not change the prompt inside one batch, or the samples stop being comparable. Stop when two rounds produce no new direction, or when the best take already meets the brief.

## What the ear catches

In Schubert's impromptu theme and variations, what keeps the idea recognisable, and whether each variation changes texture, harmony or register. In Webern's piano variations, how a variation that moves only one or two parameters still holds together. In the 87 BPM hip-hop kit, how kick placement and hi-hat density shift between takes of the same pattern, which is exactly what the first round is screening for, and which of those differences you would actually accept.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "T s s s T s s s T s s s T s s s", "bpm": 87, "label": "One take to compare against", "label_en": "One take to compare against", "hint": "先记住这一版，再听下一版差在哪里", "hint_en": "Fix this take in memory, then hear what the next one changes"}
```
:::
