---
id: stem-separation-tools
site: ai
cat: A
title: 分轨分离工具
title_en: Stem Separation Tools
summary: 从混音里拆出人声、鼓、贝斯，是二次创作与学习的入口，也是残渣的来源。
summary_en: Pulling vocals, drums and bass out of a mix opens up rework and study, and leaves residue behind.
level: standard
tags: [分轨, 分离, 采样, 二次创作]
tags_en: [stem separation, source separation, sampling, rework]
alias: [分轨分离, 人声分离, 拆轨, stem separation]
order: 3
links:
  - "[[glossary:stems]]"
  - "[[glossary:timbre]]"
  - "[[glossary:monitoring]]"
instances:
  - musicnet-000067 | 弦乐四重奏，声部相近时分离最难，听串音有多少（C1）
  - groove-000002 | 86 BPM 灵魂乐鼓组，鼓与贝斯频段重叠，分离后低频常被削（C1）
  - cyberhymnal-000003 | 管风琴赞美诗，持续和声分离后容易留下水声（C1）
sources:
  - 源分离的模型思路，对照公开研究摘要整理。
  - 分离残渣与二次创作的关系（混音实践惯例）。
updated: 2026-10-30
---

::: zh
## 问题

想给老歌做一个无伴奏版，想把一段鼓采样用在自己的曲子里，或者想听清某首歌的贝斯线。分轨分离工具可以把混音拆成人声、鼓、贝斯与其他，但它不是无损解混，分离出来的是估计值。

## 原理

源分离模型在训练中学会把混合频谱分配到不同声源。频段重叠、相位关系复杂的部分无法完美分开，人声与军鼓的中频、贝斯与底鼓的低频最容易互相污染。分离后的轨道常带有"水声"或"空洞感"，因为模型把一部分能量判给了别的声源。分离质量取决于原始混音的复杂度与模型训练的素材。

## 怎么用

先明确用途：学习听辨、做采样、还是做正式发行。学习与草稿用分离轨足够；正式发行要考虑串音与残渣。分离后对每条轨做细化处理：门限去残响、均衡补回被削的频段、用瞬态整形修复鼓的攻击。需要采样时挑干净的片段，别把整段分离轨直接当素材。注意权利，分离不改变原录音的版权状态。

## 听什么

在四重奏里听声部之间的串音，在灵魂乐鼓组里听分离后低频是否变薄，在管风琴长音里听是否出现水声。分离工具的能力边界，在声部频谱重叠时最明显。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E2","G2","A2","B2","A2","G2","E2","D2"],"label":"被分离出的贝斯线","label_en":"A separated bass line","hint":"听低频是否完整，分离常在这里留下空洞","hint_en":"Listen for whether the low end is intact; separation often leaves a hole here"}
```
:::

::: en
## The problem

You want an instrumental of an old song, a drum sample for your own track, or a clearer listen to a bass line. Stem separation splits a mix into vocals, drums, bass and other, but it is not lossless unmixing; what comes out is an estimate.

## How it works

Source separation models learn to distribute a mixed spectrum among sources. Where bands overlap and phases interact, perfect separation is impossible: vocals and snare share the midrange, bass and kick share the low end. Separated tracks often carry a watery or hollow quality because the model assigned some energy to another source. Quality depends on the complexity of the original mix and the material the model trained on.

## How to use it

Decide the purpose first: ear training, sampling, or a commercial release. Separated tracks are fine for study and drafts; releases need attention to bleed and residue. Refine each stem afterwards with gating for reverb tails, EQ to restore scooped bands, and transient shaping to repair drum attacks. When sampling, choose clean fragments instead of dropping a whole separated track in. Mind the rights, since separation does not change the copyright status of the original recording.

## What to listen for

In the quartet, bleed between parts; in the soul kit, whether the low end thins after separation; on the organ, whether wateriness appears. The limits of separation show most clearly where sources share a spectrum.

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E2","G2","A2","B2","A2","G2","E2","D2"],"label":"A separated bass line","label_en":"A separated bass line","hint":"Listen for whether the low end is intact; separation often leaves a hole here","hint_en":"Listen for whether the low end is intact; separation often leaves a hole here"}
```
:::
