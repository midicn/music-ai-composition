---
id: "text-to-music-models"
site: "ai"
cat: "A"
title: "文本生成音乐模型"
title_en: "Text-to-Music Models"
summary: "一句话生成一首歌，听起来神奇，实际是概率采样加人工筛选。"
summary_en: "A sentence in, a song out feels magical, but it is probabilistic sampling plus human selection."
level: "standard"
tags: ["文本生成", "生成模型", "采样", "AI"]
tags_en: ["text to music", "generative model", "sampling", "AI"]
alias: ["文本生成音乐", "文生音乐", "text to music", "TTM"]
order: 2
links: ["[[glossary:timbre]]", "[[glossary:tempo]]", "[[glossary:daw]]"]
instances: []
sources: ["https://arxiv.org/abs/2306.05284", "https://facebookresearch.github.io/audiocraft/api_docs/audiocraft/models/musicgen.html"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "文本生成音乐模型应以研究原文和参数接口解释条件输入与采样过程；曲库音乐的播放不能证明模型架构、训练数据来源或输出控制能力。"
---

::: zh
## 问题

输入"温暖的原声吉他，慢速，带一点弦乐"，几秒后得到一段音频。这个流程改变了素材的来源，但没有改变创作的核心：判断什么算好。模型给你的是大量候选，选哪个、怎么改，仍然是人的工作。

## 原理

模型从训练数据里学到音频与文本描述的统计关系，生成时从概率分布中采样。采样带来随机性，同一个提示每次结果不同；温度之类的参数控制随机程度。文本条件只是弱约束，模型对"和声""配器"这类结构信息的理解远不如对人声、情绪与风格的理解。长结构容易在中段松散，因为模型没有真正的曲式概念。

## 怎么用

把提示当成方向而不是指令，一次生成多个候选再挑。先定风格与情绪，再补乐器与速度，最后加排除项。需要精确控制的部分留给 MIDI 或后期。生成结果先听整体走向，再听细节，不要在明显不合适的候选上修。保留提示与种子，方便复现与微调。
:::

::: en
## The problem

Type "warm acoustic guitar, slow, a touch of strings" and seconds later audio arrives. The pipeline changes where material comes from but not the core of the work: deciding what is good. The model supplies many candidates, and choosing and fixing them remains human labour.

## How it works

The model learns statistical relations between audio and text descriptions, then samples from a probability distribution at generation time. Sampling brings randomness, so the same prompt gives different results; parameters such as temperature set how random. Text is a weak constraint, and the model understands "harmony" or "orchestration" far less well than voice, mood and genre. Long forms tend to loosen in the middle because the model has no real sense of form.

## How to use it

Treat the prompt as a direction rather than an instruction, and generate several candidates before choosing. Fix style and mood first, add instruments and tempo next, then exclusions. Leave anything that needs precision to MIDI or later editing. Judge the overall arc before detail, and do not polish a candidate that is clearly wrong. Keep prompts and seeds so results can be reproduced and adjusted.
:::

