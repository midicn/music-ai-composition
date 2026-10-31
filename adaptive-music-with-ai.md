---
id: adaptive-music-with-ai
site: ai
cat: F
title: 自适应音乐
title_en: Adaptive Music with AI
summary: 分层与重排的前提是共享速度、调性和小节边界
summary_en: Layering and resequencing only work when tempo, key and bar lines are shared
level: standard
tags: [自适应音乐, 分层, 重排, 过渡]
tags_en: [adaptive music, layering, resequencing, transitions]
alias: [自适应配乐, 动态音乐, adaptive music]
order: 3
links:
  - "[[glossary:stems]]"
  - "[[glossary:tempo]]"
instances:
  - pdmx-000031 | 一件件乐器加入，纵向分层的教科书（C1）
  - m21-000000 | 四声部终止式清楚，水平重排的切点参考（C1）
  - mutopia-001630 | 三拍子乐句规整，层切换落在小节线上（C1）
  - oga-000088 | 循环素材的分层方式，听各层如何独立成立（C1）
sources:
  - 自适应音乐的纵向分层与横向重排——依据来自游戏音频惯例。
  - Vertical layering and horizontal resequencing, following general game audio practice.
updated: 2026-10-30
---

::: zh
## 哪里不对

自适应音乐要回答两个问题，同一时刻听哪几层，下一段从哪里接进来。用 AI 生成四条"同一首曲子的不同强度版本"往往对不上，速度差两拍、调差半音、和声进行不一样，引擎一交叉淡化就露馅。

## 原因在哪

纵向分层靠共享速度、调性与和声网格，各层只改变密度和音区。横向重排靠小节边界，切换点必须落在乐句结束或强拍上，最好提前半小节准备。生成模型不会自动满足这些约束，它按自己的和声逻辑走，所以约束要写进每一次生成，或者事后用 MIDI 修。层数越多，共享的骨架越要简单，否则每加一层都要重新对齐。

## 怎么修

先做一个四到八小节的和声与节奏骨架，确定调、速度、每小节的和弦。以骨架为条件生成各层，或者干脆用同一段 MIDI 换配器。每层导出时标清 BPM 与起始小节。在引擎里把重排量化到小节，淡入淡出不超过半拍。测试时把所有层同时打开再逐层关掉，听有没有相位或调性冲突。转场单独做两小节，别指望淡入淡出解决所有问题。每次生成前先确认骨架没有被改动。

## 耳朵要抓的点

在《波莱罗》里听一件件乐器加入怎样在不改变和声的情况下加厚，在巴赫众赞歌里听四声部怎样在终止式处给出干净的切换点，在《蓝色多瑙河》里听三拍子的乐句怎样每四小节收一次，在 loop-house-in-a-forest 里听循环素材的分层方式。这些结构就是自适应系统要复制的东西。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q q q q q","bpm":100,"label":"共享的小节网格","label_en":"A shared bar grid","hint":"所有层落在同一网格上，切换才不会错拍","hint_en":"With every layer on one grid, switches land on the beat"}
```
:::

::: en
## What is off

Adaptive music has to answer two questions at once, which layers are heard now, and where the next section enters. Ask AI for four intensity versions of one piece and they usually disagree, two beats apart in tempo, a semitone apart in key, built on different chord changes, and the crossfade exposes all of it.

## Where the cause is

Vertical layering depends on a shared tempo, key and harmonic grid, with each layer changing only density and register. Horizontal resequencing depends on bar lines, so switches must land at the end of a phrase or on a strong beat, ideally prepared half a bar early. Generation models do not respect these constraints on their own; they follow their own harmonic logic, so the constraints go into every prompt or into MIDI edits afterwards. The more layers there are, the simpler the shared skeleton must be, or each addition has to be realigned.

## How to fix it

Build a four to eight bar skeleton of harmony and rhythm first, fixing key, tempo and the chord per bar. Generate each layer against that skeleton, or simply reuse one MIDI part with different orchestration. Label BPM and start bar on every export. Quantize resequencing to the bar in the engine and keep fades under half a beat. Test by opening all layers together and then muting them one at a time, listening for phase or key clashes. Write transitions as their own two bars instead of expecting a fade to fix everything. Check the skeleton is unchanged before each pass.

## What the ear catches

In Bolero, how instruments enter one by one and thicken the texture without changing the harmony; in the Bach chorale, how four voices give clean switch points at cadences; in The Blue Danube, how the three-beat phrases close every four bars; in loop-house-in-a-forest, how a loop is built in layers. These are the structures an adaptive system has to reproduce.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q q q q q","bpm":100,"label":"A shared bar grid","label_en":"A shared bar grid","hint":"With every layer on one grid, switches land on the beat","hint_en":"With every layer on one grid, switches land on the beat"}
```
:::
