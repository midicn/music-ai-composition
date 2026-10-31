---
id: text-to-music-models
site: ai
cat: A
title: 文本生成音乐模型
title_en: Text-to-Music Models
summary: 一句话生成一首歌，听起来神奇，实际是概率采样加人工筛选。
summary_en: A sentence in, a song out feels magical, but it is probabilistic sampling plus human selection.
level: standard
tags: [文本生成, 生成模型, 采样, AI]
tags_en: [text to music, generative model, sampling, AI]
alias: [文本生成音乐, 文生音乐, text to music, TTM]
order: 2
links:
  - "[[glossary:timbre]]"
  - "[[glossary:tempo]]"
  - "[[glossary:daw]]"
instances:
  - groove-000001 | 105 BPM 放克鼓组，看描述节奏时模型能否抓住律动（C1）
  - thesession-020649 | 里尔舞曲，看模型能否生成可循环的段落结构（C1）
  - cyberhymnal-008729 | 管风琴赞美诗，看持续音与和声铺陈能不能被稳定生成（C1）
sources:
  - 文本条件生成模型的基本原理（公开论文摘要）。
  - 生成结果的筛选与后期流程，参考创作实践惯例。
updated: 2026-10-30
---

::: zh
## 问题

输入"温暖的原声吉他，慢速，带一点弦乐"，几秒后得到一段音频。这个流程改变了素材的来源，但没有改变创作的核心：判断什么算好。模型给你的是大量候选，选哪个、怎么改，仍然是人的工作。

## 原理

模型从训练数据里学到音频与文本描述的统计关系，生成时从概率分布中采样。采样带来随机性，同一个提示每次结果不同；温度之类的参数控制随机程度。文本条件只是弱约束，模型对"和声""配器"这类结构信息的理解远不如对人声、情绪与风格的理解。长结构容易在中段松散，因为模型没有真正的曲式概念。

## 怎么用

把提示当成方向而不是指令，一次生成多个候选再挑。先定风格与情绪，再补乐器与速度，最后加排除项。需要精确控制的部分留给 MIDI 或后期。生成结果先听整体走向，再听细节，不要在明显不合适的候选上修。保留提示与种子，方便复现与微调。

## 听什么

在放克鼓组里听律动是否被理解，在里尔舞曲里听重复段落是否成立，在管风琴长音里听和声是否稳。模型擅长氛围与音色，薄弱处通常在结构与精确的和声进行。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["G3","B3","D4","G4","F#4","D4","B3","G3"],"label":"一段原声吉他","label_en":"An acoustic guitar figure","hint":"这类音色与情绪是文本模型最擅长的部分","hint_en":"This kind of timbre and mood is where text models do best"}
```
:::

::: en
## The problem

Type "warm acoustic guitar, slow, a touch of strings" and seconds later audio arrives. The pipeline changes where material comes from but not the core of the work: deciding what is good. The model supplies many candidates, and choosing and fixing them remains human labour.

## How it works

The model learns statistical relations between audio and text descriptions, then samples from a probability distribution at generation time. Sampling brings randomness, so the same prompt gives different results; parameters such as temperature set how random. Text is a weak constraint, and the model understands "harmony" or "orchestration" far less well than voice, mood and genre. Long forms tend to loosen in the middle because the model has no real sense of form.

## How to use it

Treat the prompt as a direction rather than an instruction, and generate several candidates before choosing. Fix style and mood first, add instruments and tempo next, then exclusions. Leave anything that needs precision to MIDI or later editing. Judge the overall arc before detail, and do not polish a candidate that is clearly wrong. Keep prompts and seeds so results can be reproduced and adjusted.

## What to listen for

On the funk kit, whether groove is understood; in the reel, whether repeated sections hold; on the organ, whether harmony stays stable. Models are strongest on atmosphere and timbre, weakest on structure and exact harmonic motion.

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["G3","B3","D4","G4","F#4","D4","B3","G3"],"label":"An acoustic guitar figure","label_en":"An acoustic guitar figure","hint":"This kind of timbre and mood is where text models do best","hint_en":"This kind of timbre and mood is where text models do best"}
```
:::
