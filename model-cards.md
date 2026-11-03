---
id: "model-cards"
site: "ai"
cat: "G"
title: "模型卡怎么读"
title_en: "Reading a Model Card"
summary: "先看限制与训练数据，再看分数是谁评的"
summary_en: "Read the limitations and training data before the scores"
level: "standard"
tags: ["模型卡", "训练数据", "评测口径", "能力边界"]
tags_en: ["model cards", "training data", "evaluation", "limitations"]
alias: ["模型卡", "model card", "模型说明"]
order: 160
links: ["[[glossary:timbre]]", "[[glossary:midi-protocol]]", "[[instrument:voice]]"]
instances: []
sources: ["https://arxiv.org/abs/1810.03993", "https://arxiv.org/abs/1803.09010"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页介绍模型卡与数据说明的阅读方式，需要核对研究原文对用途、数据及局限的定义；普通曲目试听不能验证某模型训练信息、许可或评测口径。"
---

::: zh
## 一张卡最有用的部分

两张模型卡，一张写“综合评测第一”，另一张写“中文长句容易漂、超过三分钟结构会散”。后者更能帮你决定要不要用。模型卡的价值不在排名，而在它敢写出哪些输入会坏。

## 四个字段，四种追问

| 字段 | 卡上常见写法 | 要追问的 |
|---|---|---|
| 训练数据 | 公开音频与授权曲库 | 覆盖哪些语种、年代、录音类型；有没有退出机制 |
| 限制 | 可能产生伪影 | 哪种编制、多长、什么人声会坏 |
| 评测 | 主观评分四点二 | 谁评的、几人、是否盲听、参考是什么 |
| 许可 | 可商用、需署名 | 权重、输出、训练三件事分别怎么规定 |

训练数据那一行最容易被一句“数百万首”带过。要问的是构成，不是数量：里面有没有你需要的语言与传统，录音多还是 MIDI 多，人声占多少。限制那一行也一样，写“可能有伪影”等于没写，写“超过两分钟的器乐会重复”才有用。

## 评测数字的三种口径

同一句“优于上一代”，可能来自内部听测、众包偏好或盲听 AB。内部听测样本小，众包偏好测的是第一印象，盲听 AB 只回答两个片段里更喜欢哪个。三种都不能直接推到你手上的任务。看卡时先找评测集：用什么素材、多长、有没有覆盖你的语言与编制。找不到，就把分数当广告。

## 模型卡管不到的地方

“未评估”不是缺陷，是提示。拿五到十条自己的素材做小基准，固定提示、固定种子、固定听辨人，记录坏在哪。模型卡是筛选器，不是验收单；它帮你排除明显不合适的模型，剩下的必须用自己的材料试。读完卡再试听，顺序反了，耳朵会替分数找理由。
:::

::: en
## The most useful part of a card

Two model cards: one says it ranks first on an overall benchmark, the other says long Chinese sentences drift and structure collapses past three minutes. The second one helps you decide. A model card earns its keep by naming the inputs that break, not by winning a table.

## Four fields, four follow-up questions

| Field | Usual wording | What to ask |
|---|---|---|
| Training data | Public audio and licensed catalogues | Which languages, eras and recording types; is there an opt-out route |
| Limitations | May contain artefacts | Which ensemble, what length, which vocal style fails |
| Evaluation | Subjective score of 4.2 | Who rated, how many, was it blind, against what reference |
| Licence | Commercial use, credit required | What is said separately about weights, outputs and training |

The training-data row is usually dispatched with "millions of tracks". Ask about composition instead of count: does it include the languages and traditions you need, is it mostly recordings or MIDI, how much of it is voice. The limitations row has the same problem. "May contain artefacts" says nothing; "instrumental pieces over two minutes start repeating" is useful.

## Three kinds of evaluation numbers

The same claim of beating the previous version can come from an internal listening panel, a crowd preference test or a blind AB. An internal panel is small, a crowd test measures first impressions, and blind AB only says which of two clips someone preferred. None transfers directly to your task. Find the evaluation set first: which material, what length, does it cover your language and ensemble. If that is missing, read the score as advertising.

## Where the model card stops

"Not evaluated" is a prompt, not a defect. Build a small benchmark from five to ten of your own pieces, with fixed prompts, fixed seeds and a fixed listener, and write down how each one fails. A model card is a filter, not an acceptance test. It removes clearly unsuitable models; the rest has to be tried on your own material. Listen after reading the card, not before, or your ears will start arguing for the score.
:::

