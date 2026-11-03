---
id: "model-diffrhythm"
site: "ai"
cat: "I"
title: "DiffRhythm"
title_en: "DiffRhythm"
summary: "十秒出整曲，快得能当草稿机，结构要自己盯。"
summary_en: "A full song in seconds, fast enough as a sketch machine; watch the structure yourself."
level: "standard"
tags: ["模型档案", "开源权重", "扩散模型", "整曲生成"]
tags_en: ["model profile", "open weights", "diffusion", "full-song generation"]
alias: ["DiffRhythm", "谛韵", "扩散整曲"]
order: 201
model_vendor: "ASLP Lab（西北工业大学）"
model_form: "本地模型"
model_input: ["歌词", "文本"]
model_output: ["音频"]
model_licence: "代码以 Apache 2.0 放出，权重与后续版本（含 DiffRhythm+）的商用范围另行标注，以仓库与模型卡为准"
model_verified: "2026-10-31"
links: ["[[glossary:diffusion]]", "[[glossary:tempo]]", "[[glossary:binary-form]]"]
instances: []
sources: ["https://github.com/ASLP-lab/DiffRhythm", "https://arxiv.org/abs/2503.01183"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页介绍DiffRhythm研究模型，应对照官方仓库与论文的具体版本、输入和运行条件；普通MIDI不是模型生成结果，不能用来验证整曲时长、速度或歌词对齐。"
---

::: zh
## 十秒与五分钟

DiffRhythm 把整首歌压进一次扩散：歌词加风格提示，十秒左右出四分钟上下的成品，人声与伴奏一起。它不追求逐句精修，卖点是速度与完整度。做短视频配乐、给客户三个方向、批量试风格，这种速度很有用；要抠咬字和混音，它给不了。官方标称最长可到四分四十五秒，实际长度受歌词行数与版本影响。

## 两样输入，一段成品

歌词按行写，段落可以用标记分开；风格提示写曲风、情绪、配器，越具体越稳。输出是混好的立体声，没有分轨。模型对歌词的排布有自己的判断，句子太长会被压缩，段落标记也不总被照做。想控制结构，先把每段行数写匀，再在提示里点明主副歌的对比。

| 你写的 | 它常给的 | 要盯的地方 |
|---|---|---|
| 四行主歌、四行副歌 | 结构大致对，副歌会抬高 | 第二次副歌是否原样重复 |
| 一句风格描述 | 配器与情绪接近 | 低频与鼓的密度 |
| 长句、多音节词 | 咬字被压扁 | 句尾与高音区 |

## 快，适合放在流程前段

一首歌十秒，意味着一个下午能试几十版。把歌词、风格、段落拆成几组变量，固定其他项，能快速找到可用的方向。后续版本也能做续写和局部改，但改动的边界不清，常常一动就换掉整段配器。适合当草稿机，不适合当终稿；真正的混音、修音、分轨，仍要回到 DAW 或别的工具。

## 重复、漏句与结构失控

- 副歌第二次出现时原样复制，连鼓的过门都一样。
- 长歌词漏句，尤其是句尾的虚词。
- 段落标记被忽略，桥段直接消失。
- 人声与伴奏的响度不齐，批量出歌要逐条归一。
- 中文声调在快句里糊，英文连读反而更稳。

## 本地跑与替代

8GB 显存能跑基础版，生成速度快，适合反复试。权重与代码的许可分开看，后续版本与 DiffRhythm+ 的商用范围不同，发行前确认模型卡。替代：要更长、更稳的整曲，换 YuE；要网页端省事，换 Suno；要分轨与后期，换腾讯音乐天琴这类平台工具。
:::

::: en
## Ten seconds and five minutes

DiffRhythm compresses a whole song into one diffusion pass: lyrics plus a style prompt, and about ten seconds later a finished track of roughly four minutes with vocals and backing together. It does not chase line-by-line polish; speed and completeness are the product. That suits short-video beds, three directions for a client, or a quick style sweep. It will not give you precise diction or a finished mix. The official ceiling is four minutes forty-five seconds, and actual length depends on lyric length and version.

## Two inputs, one finished track

Lyrics go in by line, with tags to separate sections; the style prompt names genre, mood and instrumentation, and specificity helps. Output is a mixed stereo file with no stems. The model makes its own decisions about lyric placement, compresses long lines and does not always honour section tags. To steer form, even out the line count per section first, then state the verse-chorus contrast in the prompt.

| What you write | What often comes back | What to check |
|---|---|---|
| Four verse lines, four chorus lines | Roughly right, chorus lifts | Whether the second chorus is copied |
| One style sentence | Close instrumentation and mood | Low end and drum density |
| Long lines, polysyllables | Diction flattened | Line endings and high notes |

## Speed belongs early in the process

Ten seconds a song means dozens of tries in an afternoon. Split lyrics, style and structure into variables, hold the rest fixed, and a usable direction appears quickly. Later versions can continue or edit a section, but the boundary of the edit is unclear and one move can replace the whole arrangement. Treat it as a sketch machine, not a final master; mixing, repair and stems still belong in a DAW or another tool.

## Repetition, dropped lines, lost structure

- The second chorus is copied exactly, down to the drum fill.
- Long lyrics lose lines, especially final particles.
- Section tags are ignored and the bridge disappears.
- Vocal and backing levels do not match, so a batch needs per-file normalisation.
- Mandarin tones blur on fast lines; English legato is steadier.

## Local runs and alternatives

The base model runs in 8GB of VRAM and generates quickly, which suits repeated trials. Code and weights are licensed separately, and later versions and DiffRhythm+ carry different commercial terms; check the model card before release. Alternatives: YuE for longer, steadier full songs; Suno for a browser service; TME Tianqin or a similar platform for stems and post-production.
:::

