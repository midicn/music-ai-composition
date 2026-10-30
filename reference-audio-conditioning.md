---
id: reference-audio-conditioning
site: ai
cat: B
title: 参考音频条件
title_en: Reference Audio Conditioning
summary: 给一段音频当参照，比写十句形容词更能定住音色与律动。
summary_en: One reference clip pins timbre and groove better than ten adjectives.
level: standard
tags: [参考音频, 条件生成, 风格迁移, 控制]
tags_en: [reference audio, conditioning, style transfer, control]
alias: [参考音频, 音频条件, reference audio, 风格迁移]
order: 7
links:
  - "[[glossary:timbre]]"
  - "[[glossary:tempo]]"
  - "[[glossary:stems]]"
instances:
  - groove-000002 | 86 BPM 灵魂乐鼓组，作为律动参照最直接（C1）
  - cyberhymnal-008729 | 管风琴赞美诗，作为音色与空间参照（C1）
  - thesession-005995 | 吉普赛风格曲调，作为演奏法参照（C1）
sources:
  - 音频条件生成的技术方式，依公开研究摘要核对，未抄原文
  - 参考素材的权利问题，依版权通识核对，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

文字描述音色总有隔阂，"温暖的模拟感"每个人理解不同。参考音频直接把目标声音放给模型听，音色、律动与空间感一次到位。代价是权利与可控性的问题。

## 原理

参考音频作为条件输入，模型从中提取音色、节奏密度与混音特征，再生成新的内容。相似度由参数控制，太高会接近复制，太低则等于没用。参考的时长、清晰度与代表性都会影响效果，一段干净的三秒循环常常比三十秒杂乱录音更有效。

## 做法

选代表作而不是整张专辑，选干净片段而不是现场嘈杂录音。明确参考的维度：只学音色，还是也学律动。控制相似度在自己能接受的范围，避免生成结果与原作难以区分。确认参考素材的使用权利，公开发行前尤其谨慎。把参考与提示结合，提示负责结构，参考负责质感。

## 听什么

在灵魂乐鼓组里听律动是否被抓住，在管风琴里听空间感是否保留，在吉普赛曲调里听演奏法是否接近。参考用得好，结果会像同一间屋子里录的。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":86,"label":"作为参照的律动","label_en":"A groove used as reference","hint":"参考音频先定住律动，再看生成结果跟得多近","hint_en":"The reference fixes the groove; hear how closely the result follows"}
```
:::

::: en
## The problem

Words for timbre always lose something; "warm analogue feel" means different things to different people. A reference clip plays the target sound to the model, fixing timbre, groove and space at once. The price is rights and control.

## How it works

The reference enters as conditioning, from which the model extracts timbre, rhythmic density and mix character before generating new material. A similarity parameter sets how close it stays: too high approaches copying, too low makes the reference useless. Length, clarity and typicality all matter, and a clean three-second loop often works better than thirty noisy seconds.

## Practice

Pick a representative passage rather than a whole album, and a clean fragment rather than a noisy live recording. State which dimension is being referenced: timbre only, or groove as well. Keep similarity where the result is clearly not the original. Confirm the right to use the reference, especially before public release. Combine reference with prompt so the prompt handles structure and the reference handles texture.

## What to listen for

On the soul kit, whether the groove is captured; on the organ, whether the space survives; on the gypsy tune, whether the playing style comes close. A good reference makes the result sound like it was recorded in the same room.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":86,"label":"A groove used as reference","label_en":"A groove used as reference","hint":"The reference fixes the groove; hear how closely the result follows","hint_en":"The reference fixes the groove; hear how closely the result follows"}
```
:::
