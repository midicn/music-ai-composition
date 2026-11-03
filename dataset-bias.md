---
id: "dataset-bias"
site: "ai"
cat: "G"
title: "数据偏差"
title_en: "Dataset Bias"
summary: "语料偏向英语世界的流行与欧洲古典，输出会把偏向当成常识"
summary_en: "Corpora lean toward Anglophone pop and European classical, and output treats the lean as normal"
level: "standard"
tags: ["数据偏差", "传统音乐", "代表性", "符号化"]
tags_en: ["dataset bias", "traditional music", "representation", "notation"]
alias: ["数据偏差", "语料偏差", "dataset bias"]
order: 7
links: ["[[glossary:timbre]]", "[[instrument:voice]]"]
instances: []
sources: ["https://huggingface.co/facebook/musicgen-small", "https://arxiv.org/abs/2301.11325"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论训练语料构成与适用范围，需要依据模型卡及研究的数据说明核对；普通曲库MIDI不是训练数据统计，也不能证明模型在某传统或语言上的偏差。"
---

::: zh
## 起点：一个问题

让模型写"非洲节奏"或"亚洲旋律"，结果往往是英美流行乐的骨架加上五声音阶。这不是模型笨，是语料结构造成的。训练数据里，英语世界的流行、摇滚与欧洲古典占多数，其他传统要么样本少，要么被简化成单声部旋律或鼓循环。用这样的工具做跨文化项目，输出的"平均味"会被当成默认。

## 它怎么工作

语料偏差有三个来源。覆盖偏差，某些传统没有被录下来，或没有数字化。表示偏差，MIDI 与 ABC 这类格式只能记音高、时值与力度，微分音、滑音、装饰、非平均律都会丢失。标注偏差，许多曲种被塞进一个 world 标签，内部差异被抹平。模型学的是统计规律，样本少的方向会被邻近的多数样本拉过去。结果是，越冷门的传统，输出越像主流风格的变体。

## 具体做法

先承认工具的能力边界，别把"能生成"当成"懂这个传统"。做跨文化项目时，请该传统的演奏者参与并付费，请他们校对，而不是让模型代替。准备参考音频，用条件生成而不是纯文本描述。把输出当草稿，逐条检查音律、装饰、句法与乐器编制。记录模型版本与提示词，便于复现问题。对外说明哪些部分由工具生成、哪些由顾问修订。若项目涉及特定社群，提前沟通用途与署名，有些素材有使用禁忌，不在公开条款里。
:::

::: en
## Starting point: a problem

Ask a model for African rhythms or Asian melodies and you often get an Anglophone pop skeleton with a pentatonic scale on top. This is not stupidity, it is corpus structure. Training data leans heavily on English-language pop, rock and European classical, while other traditions are either thinly sampled or reduced to a single melodic line or a drum loop. Use such tools for cross-cultural work and the average becomes the default.

## How it works

Bias enters at three points. Coverage, since some traditions were never recorded or digitised. Representation, because MIDI and ABC carry pitch, duration and velocity but drop microtones, slides, ornaments and non-equal temperaments. Labelling, since many traditions are filed under one world tag that erases internal difference. A model learns statistical regularity, so thinly sampled directions get pulled toward the neighbouring majority. The rarer the tradition, the more the output resembles a variant of the mainstream.

## In practice

Acknowledge the tool's limits, and do not confuse generating with understanding a tradition. On cross-cultural projects, hire players from that tradition and pay them to review, rather than letting the model stand in. Prepare reference audio and use conditioned generation instead of text alone. Treat output as a draft and check tuning, ornament, phrasing and instrumentation line by line. Log model version and prompts so problems can be reproduced. State externally which parts were generated and which were revised by a consultant. Where a specific community is involved, discuss use and credit in advance, since some material carries restrictions that never appear in public terms.
:::

