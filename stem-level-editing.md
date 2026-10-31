---
id: stem-level-editing
site: ai
cat: C
title: 分轨级编辑
title_en: Stem-Level Editing
summary: 分轨不是干净的分轨，改动一条之前先想清楚总和会怎样
summary_en: Separated stems are approximations, so every change to one is a change to the sum.
level: standard
tags: [分轨, 分离, 平衡, 串音]
tags_en: [stems, separation, balance, bleed]
alias: [分轨处理, stem 编辑, stem editing]
order: 4
links:
  - "[[glossary:stems]]"
  - "[[glossary:stem-mastering]]"
  - "[[glossary:midi-protocol]]"
instances:
  - musicnet-000067 | 贝多芬第十五四重奏，四声部要能分开也要平衡（C1）
  - groove-000003 | 80 BPM soul 鼓组，底鼓与贝斯争同一段低频（C1）
  - giantmidi-002992 | 格里格钢琴协奏曲改编，主奏与伴奏压进一条 MIDI（C1）
sources:
  - 分轨分离的误差来源；分离工具公开文档是主要依据。
  - 分轨改动的平衡与相位问题——依据来自混音惯例。
updated: 2026-10-30
---

::: zh
## 卡住的地方

分轨工具给出的几条 stem 不是干净的分轨，而是近似。鼓里有贝斯，人声里有镲片，钢琴轨带着混响尾巴。直接在这上面做均衡或压缩，会把串音一起放大。改完一条，几条相加的平衡也变了，原来的混音参考就失效了。更麻烦的是，你无法知道漏进来的是原轨的哪一部分，只能靠听。

## 工作机制

分离是按频谱与统计特征猜的，频段重叠的地方必然互相漏。所以判断标准不是干不干净，而是这条轨上有没有这次要改的东西。改动一条轨会破坏总和的平衡，每次改完都要回到总和听一遍。分离还可能引入相位差，几条相加未必还原原始混音。分轨编辑因此该带着目的做，先写下要解决的一个问题，再动手。

## 从哪开始

先建一条总和校验轨，把几条 stem 相加，和原始混音做 A/B，确认响度与相位没被改变。修串音先用门限或动态均衡处理空档，再考虑频谱修复，后者容易伤到本来干净的部分。替换某一条时，把新素材对齐到原轨的起音时间，再匹配响度与混响。改完把监听音量降下来复听，平衡问题在低音量下更明显。处理顺序建议先从节奏轨到和声轨再到主奏，因为前者决定后者的掩蔽关系。

## 耳朵要抓的点

在贝多芬第十五弦乐四重奏里，听四个声部是否还能分别听清，分离干净不等于平衡正确。在 80 BPM 的 soul 鼓组里，听底鼓与贝斯在低频上互相掩蔽到什么程度。在格里格的钢琴协奏曲改编里，听主奏与伴奏被压进一条 MIDI 之后，还能不能重新拆成两层。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E2","E2","G2","A2","E2","E2","D2","E2"],"label":"低频上的两条轨","label_en":"Two parts sharing the low end","hint":"底鼓与贝斯抢同一段频率，听谁盖住谁","hint_en":"Kick and bass fight for the same band; hear which one covers the other"}
```
:::

::: en
## Where it snags

The stems a separator hands back are approximations, not clean tracks. The drums carry bass, the vocal carries cymbals, the piano keeps a reverb tail. Equalising or compressing them directly amplifies whatever bled in. Change one stem and the balance of the sum moves too, so the original mix stops being a valid reference. You also cannot see which part of the original leaked in, only hear it.

## The working mechanism

Separation guesses from spectrum and statistics, so overlapping bands leak into each other. The test is not cleanliness but whether the stem contains what you need to change this time. Editing one stem breaks the balance of the sum, so return to the sum after every change. Separation can also shift phase, and the stems added back may not reproduce the original mix. Work with one stated problem at a time rather than cleaning everything.

## Where to start

Build a sum check track by adding the stems and comparing it with the original mix, confirming level and phase are unchanged. Attack bleed with a gate or dynamic EQ in the gaps first, spectral repair second, since the latter damages the clean parts. When replacing a stem, align the new material to the original onsets and match level and reverb. Work from drums to harmony to lead, since masking runs in that direction. Then listen at low monitoring level, where balance problems show up first, and check the sum rather than the solo stems, which hide masking.

## What the ear catches

In Beethoven's String Quartet No. 15, whether four parts stay separately audible; a clean separation is not the same as a correct balance. In the 80 BPM soul kit, how far the kick and bass mask each other in the low end. In the Grieg concerto reduction, whether lead and accompaniment can be split into two layers again after sharing one MIDI part.

```audiolab
{"type": "instrument", "gm": "Electric Bass (finger)", "synth": "plucked", "phrase": ["E2", "E2", "G2", "A2", "E2", "E2", "D2", "E2"], "label": "Two parts sharing the low end", "label_en": "Two parts sharing the low end", "hint": "底鼓与贝斯抢同一段频率，听谁盖住谁", "hint_en": "Kick and bass fight for the same band; hear which one covers the other"}
```
:::
