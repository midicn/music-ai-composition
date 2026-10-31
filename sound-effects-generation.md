---
id: sound-effects-generation
site: ai
cat: F
title: 音效生成
title_en: Sound Effects Generation
summary: 生成的音效像不等于能用，瞬态、尾巴、单声道都要查
summary_en: A generated sound that seems right may still fail on transients, tails and mono
level: standard
tags: [音效, 拟音, 品控, 单声道]
tags_en: [sound effects, foley, QC, mono]
alias: [音效设计, 拟音, sound design]
order: 6
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:timbre]]"
instances:
  - groove-000000 | 鼓的瞬态硬，对照生成音效的软起音（C1）
  - pdmx-002820 | 定音鼓滚奏的起音与衰减，判断尾巴长短（C1）
  - giantmidi-007947 | 噪声类素材的频段分布，检查生成音效的位置（C1）
  - atepp-000381 | 钟的泛音结构，检验高频是否被处理坏（C1）
sources:
  - 音效与拟音的可用性标准；后期制作惯例是主要依据。
  - Usability criteria for sound effects and foley — based on general post-production practice.
updated: 2026-10-30
---

::: zh
## 起点：一个问题

生成音效听起来"像"，但常常不能用。单声道折叠后变薄、尾巴太长盖住下一句、起音软、背景带一层生成噪声。放进游戏或片子，叠上对白就糊，最后还是要回头去录。

## 运行方式

音效的可用性由三件事决定，瞬态是否清楚、尾巴是否可控、频段是否留了位置。录音的 foley 有真实的房间和动作，起音带一个明确的接触点；生成音效是统计意义上的平均，起音往往偏软，尾音往往自带混响，折叠成单声道时相位问题明显。低频和高频也常超出需要，占了别的元素的位置。

## 具体做法

先分类。脚步、衣物、门、机械这类有明确动作的，优先录，几十条素材就能用很久。爆炸、魔法、科幻这类没有现实对应的，可以生成，但更适合做层次而不是主体。生成的素材一律检查单声道、尾巴长度、直流偏移和峰值。需要贴画面时，切掉生成混响，自己加房间。批量交付前做 QC，命名、采样率、电平、静音头统一，每条都听开头三秒和结尾三秒。同一个动作录三遍，比生成十条更像同一个世界。

## 耳朵要抓的点

在 funk-groove1 里听鼓的瞬态有多硬，这是生成音效最难保住的部分。在泰勒曼的三支小号与定音鼓协奏曲里听滚奏的起音和衰减，在布利茨坦的《打击乐音乐》里听噪声类素材的频段分布，在格里格的《钟声》里听钟的泛音结构。对比生成版本，差别通常在起音的前几毫秒。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s","bpm":60,"label":"一次起音和它的尾巴","label_en":"One attack and its tail","hint":"先听前几毫秒的接触点，再听尾巴有没有拖住下一个声音","hint_en":"Hear the contact in the first milliseconds, then whether the tail holds the next sound"}
```
:::

::: en
## Starting point: a problem

A generated sound effect can seem right and still be unusable. It thins out in mono, its tail covers the next line, the attack is soft, and a layer of generation noise sits underneath. Drop it into a game or a cut, put dialogue over it, and the mix turns to mud.

## How it runs

Usability comes down to three things, how clear the transient is, how controllable the tail is, and whether the spectrum leaves room for anything else. Recorded foley has a real room and a real action, so its attack carries a definite point of contact. A generated effect is a statistical average, with a soft attack, built-in reverb, and phase problems that show up when folded to mono. Low and high end often exceed what is needed and take space from other elements.

## In practice

Sort by type first. Footsteps, cloth, doors and machinery have a clear action, so record them; a few dozen files last a long time. Explosions, magic and science fiction have no real counterpart and can be generated, but they work better as layers than as the main event. Check every generated file for mono compatibility, tail length, DC offset and peak. When it has to sit on picture, cut the generated reverb and add your own room. Before batch delivery, run QC on naming, sample rate, level and silence at the head, and listen to the first and last three seconds of each file. Three takes of one action sound more like one world than ten generated variants.

## What the ear catches

In funk-groove1, how hard the drum transient is, which is the part generation struggles to keep. In Telemann's concerto for three trumpets and timpani, the attack and decay of the rolls; in Blitzstein's Percussion Music, where noise-based material sits in the spectrum; in Grieg's Bell Ringing, the overtone structure of a bell. Against a generated version, the difference is usually in the first few milliseconds.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s","bpm":60,"label":"One attack and its tail","label_en":"One attack and its tail","hint":"Hear the contact in the first milliseconds, then whether the tail holds the next sound","hint_en":"Hear the contact in the first milliseconds, then whether the tail holds the next sound"}
```
:::
