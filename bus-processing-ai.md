---
id: bus-processing-ai
site: ai
cat: D
title: 总线处理
title_en: Bus Processing
summary: 总线胶合对 AI 素材是双刃，已经压平的东西再压只会更死
summary_en: Glue and saturation can flatter AI material, but compressing an already flat mix only makes it flatter.
level: standard
tags: [总线, 胶合, 饱和, 压缩]
tags_en: [bus, glue, saturation, compression]
alias: [总线压缩, 胶合, bus glue]
order: 3
links:
  - "[[glossary:bus]]"
  - "[[glossary:compressor]]"
  - "[[glossary:parallel-compression]]"
instances:
  - groove-000007 | 65 BPM 摇滚鼓组，慢启动压缩是否放过起音，一听便知（C1）
  - atepp-001114 | 肖邦第一叙事曲，听弱到强的弧线有没有被总线压成斜线（C1）
  - cyberhymnal-003612 | 管风琴赞美诗，持续和弦没有瞬态，饱和只会加厚中频（C1）
sources:
  - 总线胶合与并联压缩的判断，参考混音惯例与听感实践。
  - Bus glue and parallel compression, with reference to general mixing practice.
updated: 2026-10-30
---

::: zh
## 难在哪

总线压缩和饱和是混音里最容易上瘾的两件事。挂上之后整体立刻像一首歌，鼓更紧，人声更贴。AI 素材本来就偏平，压缩器能做的只是把已经不多的起伏再削一层，饱和则把中高频填满。结果不是胶合，是发闷、抽吸和瞬态丢失。

## 它怎么运转

胶合靠共享的增益衰减，让各声部在同一时间轻微起伏，产生微动态。素材本身没有微动态时，压缩器只能跟着最强的瞬态走，弱段被抬、强段被压，听感更平。饱和加入谐波，能增加密度与存在感，但也会抬高表头响度，让人误以为更好。AI 输出的素材往往已经过一层限幅与饱和，再叠一次就是重复处理，谐波堆积在 1 到 3 kHz，听久了刺。

## 从哪开始

先看表。把总线压缩旁通，比较开启前后的峰均比，差距小于 1 dB 就说明它没在做事，只是染色。要用就用 30 ms 左右的慢启动、自动或 200 到 400 ms 释放，增益衰减控制在 1 到 2 dB。更稳的做法是并联，把压过的信号垫在下面，保留原始瞬态。饱和只放在鼓组或高频层，混入比例 10% 到 20%，每次对比都把电平对齐。素材已经很平就跳过总线压缩，把动态留给音量自动化，别指望一个插件把平的素材变活。

## 耳朵要抓的点

在 65 BPM 的摇滚鼓组里，听底鼓与军鼓的起音是否还在，慢启动压缩应该放过它们。在肖邦第一叙事曲里，听从弱到强的整个过程有没有被压成一条斜线，胶合过度会毁掉这条弧。在管风琴赞美诗里，听持续和弦本来就没有瞬态，饱和只会让中频更厚。三处都先对齐电平，再判断插件到底做了好事还是只是变响。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","C4","E4","G4","E4","C4","G3"],"label":"总线胶合前后","label_en":"Before and after bus glue","hint":"注意起音是否还在，慢启动压缩会先放过瞬态","hint_en":"Listen for whether the attacks survive; a slow attack lets transients through first"}
```
:::

::: en
## Where it gets hard

Bus compression and saturation are the two most addictive moves in mixing. Engaged, the mix immediately sounds like a record, drums tighter, vocal closer. AI material is already flat, so a compressor can only shave the little variation that remains while saturation fills the upper midrange. The result is not glue but dullness, pumping and lost transients.

## How it runs

Glue comes from shared gain reduction, which makes parts rise and fall together by a small amount and creates micro-dynamics. When the source has none, the compressor follows the loudest transient, lifting weak passages and pressing strong ones, so the mix reads flatter. Saturation adds harmonics, density and presence, but also raises indicated loudness, which flatters the ear. AI output often arrives after one round of limiting and saturation, so a second round is repeated processing, with harmonics piling up between 1 and 3 kHz.

## Where to start

Look at the meters first. Bypass the bus compressor and compare crest factor; a difference under 1 dB means it is colouring, not working. If you use it, try a 30 ms attack with auto or 200 to 400 ms release and keep gain reduction at 1 to 2 dB. Parallel compression is safer, placing the compressed signal under the clean one so transients survive. Put saturation only on drums or a high layer, blend 10 to 20 percent, and level-match every comparison. If the material is already flat, skip bus compression and spend the dynamics on volume automation instead of asking one plugin to revive a flat mix.

## What the ear catches

In the 65 BPM rock groove, hear whether kick and snare attacks survive; a slow attack should let them through. In Chopin's Ballade No. 1, hear whether the climb from soft to loud has been pressed into a straight line, since too much glue destroys that arc. In the organ hymn, hear that sustained chords have no transients to grab, so saturation only thickens the midrange. Level-match all three before deciding whether the plugin helped or merely got louder.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","C4","E4","G4","E4","C4","G3"],"label":"Before and after bus glue","label_en":"Before and after bus glue","hint":"Listen for whether the attacks survive; a slow attack lets transients through first","hint_en":"Listen for whether the attacks survive; a slow attack lets transients through first"}
```
:::
