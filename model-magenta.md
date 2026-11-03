---
id: "model-magenta"
site: "ai"
cat: "I"
title: "Magenta"
title_en: "Magenta"
summary: "研究工具箱：MIDI 与音频都能碰，产出可复现。"
summary_en: "A research toolkit for MIDI and audio, built for reproducible experiments."
level: "standard"
tags: ["模型档案", "开源工具", "符号音乐", "研究"]
tags_en: ["model profile", "open tools", "symbolic music", "research"]
alias: ["Magenta", "Magenta Studio", "DDSP"]
order: 202
model_vendor: "Google Magenta"
model_form: "开源工具集"
model_input: ["MIDI", "音频", "文本"]
model_output: ["MIDI", "音频"]
model_licence: "代码以 Apache 2.0 为主，各模型与预训练权重分别标注，商用前看具体仓库"
model_verified: "2026-10-31"
links: ["[[glossary:midi-protocol]]", "[[instrument:piano]]", "[[glossary:ternary-form]]"]
instances: []
sources: ["https://github.com/magenta/magenta", "https://magenta.tensorflow.org/studio/"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页介绍Magenta代码和Studio工具，需要核对官方项目文档、输入输出与维护状态；普通曲库MIDI不是该工具推理结果，不能用来测评插值、续写或可复现性。"
---

::: zh
## 它是工具箱，不是一首歌

Magenta 是 Google 的研究项目，不是“输入一句话出歌”的产品。它给的是一组模型与工具：MusicVAE 做旋律插值与重组，Melody RNN 续写，Drums RNN 生成鼓，Performance RNN 学演奏力度，DDSP 做可微分音频合成，NSynth 做音色。每一项都小，合起来能搭出一套自己的生成流程。

## MIDI 进，MIDI 出

多数工具吃 MIDI、吐 MIDI：音高、时值、力度都是显式的，改起来像改谱，不像改音频。DDSP 与 NSynth 是例外，输出音频，音色可调，但不唱词。它不处理歌词，也不做人声；要唱歌，得接别的模型。这个分工让它在编曲、动机发展、鼓轨变奏上很顺手。

| 工具 | 输入 | 输出 | 适合 |
|---|---|---|---|
| MusicVAE | MIDI 片段 | MIDI | 插值、接续 |
| Melody RNN | 旋律 | MIDI | 续写 |
| Drums RNN | 风格或片段 | MIDI 鼓轨 | 变奏 |
| DDSP | 音频或 MIDI | 音频 | 音色迁移 |

## 可复现实验的价值

同一段 MIDI、同一个检查点、同一个随机种子，结果能重跑。做研究或做教学，这比“听起来不错”重要：可以只改一个变量，比较旋律的走向、鼓的密度、音色的亮度。Magenta Studio 把这些模型包成 Ableton 的插件，不写代码也能试；要批量跑，就用 Python 包。它的产出容易进 DAW，继续编曲或做音源。

## 归档后的维护风险

主仓库已转为只读，部分工具迁到独立仓库，安装说明与依赖版本对不上是常事。TensorFlow 版本、预训练检查点、Python 依赖，任何一处变了都可能跑不起来。它没有客服，也没有稳定 API；把它放进生产流程，先准备一个能长期冻结的环境。新项目还在出，但节奏不再像维护中的产品。

## 许可、维护与替代

代码以 Apache 2.0 为主，模型与预训练权重各自标注，商用前看仓库。替代：要开箱出歌，换 Suno 或 YuE；要音频纹理与音效，换 Stable Audio Open；要符号级但维护更勤的工具，考虑 ACE-Step 这类新项目。Magenta 的优势是透明与可改，不是音质。
:::

::: en
## A toolbox, not a song

Magenta is a Google research project, not a one-line-to-song product. It provides a set of models and tools: MusicVAE for melody interpolation and recombination, Melody RNN for continuation, Drums RNN for drum parts, Performance RNN for performance dynamics, DDSP for differentiable audio synthesis and NSynth for timbre. Each piece is small; together they let you assemble your own generation pipeline.

## MIDI in, MIDI out

Most tools take MIDI and return MIDI: pitch, duration and velocity stay explicit, so editing feels like editing a score rather than audio. DDSP and NSynth are the exceptions, returning audio with adjustable timbre but no words. Magenta does not handle lyrics or singing; that needs another model. The division of labour makes it handy for arranging, motif development and drum variation.

| Tool | Input | Output | Good for |
|---|---|---|---|
| MusicVAE | MIDI fragment | MIDI | Interpolation, continuation |
| Melody RNN | Melody | MIDI | Continuation |
| Drums RNN | Style or fragment | MIDI drums | Variation |
| DDSP | Audio or MIDI | Audio | Timbre transfer |

## The value is reproducibility

The same MIDI, checkpoint and random seed can be run again. For research or teaching that matters more than "sounds good": change one variable and compare melodic direction, drum density or timbral brightness. Magenta Studio wraps these models as Ableton plugins for people who do not code; for batch work, use the Python package. Output drops into a DAW for further arranging or as a sound source.

## Maintenance risk after archiving

The main repository is now read-only and some tools have moved to separate repositories, so install notes and dependency versions often disagree. A changed TensorFlow version, checkpoint or Python dependency can stop the whole thing. There is no support desk and no stable API; to put it into production, freeze an environment you can keep. New work still appears, but not at the pace of a maintained product.

## Licence, maintenance and alternatives

Code is mostly Apache 2.0; models and pretrained weights are labelled separately, so read the repository before commercial use. Alternatives: Suno or YuE for finished songs; Stable Audio Open for textures and effects; newer symbolic projects such as ACE-Step if you need active maintenance. Magenta's advantage is transparency and modifiability, not audio quality.
:::

