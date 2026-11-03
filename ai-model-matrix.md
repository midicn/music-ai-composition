---
id: "ai-model-matrix"
site: "ai"
cat: "A"
title: "模型横向对照"
title_en: "A Model Comparison Matrix"
summary: "按输入、输出、可控性、授权四轴比较，先排除不合格再谈音质。"
summary_en: "Compare inputs, outputs, control and licensing before sound quality; a matrix narrows the field, it does not crown a winner."
level: "standard"
tags: ["模型对照", "选型", "可控性", "授权"]
tags_en: ["model comparison", "selection", "control", "licensing"]
alias: ["模型矩阵", "横向对照", "model matrix"]
order: 121
links: ["[[glossary:timbre]]", "[[glossary:stems]]", "[[glossary:midi-protocol]]"]
instances: []
sources: ["https://huggingface.co/facebook/musicgen-small", "https://elevenlabs.io/docs/overview/capabilities/music"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页比较不同产品的输入、输出、许可和控制，应以对应版本模型卡与接口说明填写；本站固定MIDI不是这些服务的共同测试结果。"
---

::: zh
## 四轴先过筛，再听音质

榜单第一的模型，放进你的工程里可能连分轨都导不出。选型不是找最强的，而是找在交付物、输入素材、控制深度和授权四项上都过关的。四项里有一项不合格，音质再好也只能放弃。

## 四类形态的差别

| 形态 | 典型输入 | 输出 | 可控性 | 授权要看 |
|---|---|---|---|---|
| 整曲生成 | 文字、歌词、哼唱 | 立体声成品，偶有分轨 | 段落与风格可控，细节弱 | 商用范围、发行权、训练来源 |
| 编辑与分轨 | 已有音频、时间码 | 分轨、补段、替换 | 局部强，整体结构弱 | 上传素材的处理条款 |
| 符号与 MIDI | 乐谱、MIDI、和弦 | MIDI、乐谱、渲染音频 | 音高节奏精确，音色靠采样 | 输出与采样库分别授权 |
| 开源本地 | 权重、代码、自有素材 | 音频或符号，取决于部署 | 可改可微调，门槛在算力 | 权重许可、训练集合规 |

表里没有名次。整曲生成在“从零到能听”上最快，符号工具在“改一个声部”上最稳，本地部署在“数据不出门”上最省心。它们解决的是不同问题，放在一张表里是为了看清代价，不是为了选冠军。

## 选型流程

1. 写下交付物：成品、分轨、MIDI，还是几个可替换的版本。
2. 标出必须保留的输入：歌词、参考音频、已有编曲。
3. 定控制下限：哪些参数必须精确，哪些可以接受抽卡。
4. 查授权：输出能否商用，上传素材会不会被留存。
5. 用同一段真实素材试两次，比较可复现性与返工量。

顺序不能倒。先试听再查授权，常常白做；先定控制下限，也不会被演示曲带偏。

## 矩阵会失效的地方

演示曲挑的是模型最擅长的片段；版本更新会悄悄改掉旧行为；授权条款按地区与档位分叉。把矩阵当排除工具，用自己的一小段素材复测，结论才站得住。真正需要精确和声或长结构时，矩阵只能告诉你哪类工具值得试，不能替你完成验收。
:::

::: en
## Filter on four axes, then listen

The top name on a leaderboard may not export a single stem into your session. Selection is not about the strongest model but the one that clears four gates: deliverable, required input, control depth and licensing. Fail one gate and the finest sound is irrelevant.

## Four shapes, different costs

| Shape | Typical input | Output | Control | Licensing focus |
|---|---|---|---|---|
| Whole-song generation | Text, lyrics, humming | Stereo master, sometimes stems | Sections and style yes, detail no | Commercial scope, release rights, training source |
| Editing and separation | Existing audio, timecode | Stems, patched sections, replacements | Strong locally, weak globally | Terms for uploaded material |
| Symbolic and MIDI | Scores, MIDI, chords | MIDI, scores, rendered audio | Exact pitch and rhythm, sampled tone | Output and sample library licensed separately |
| Open local | Weights, code, own material | Audio or symbols, depends on setup | Modifiable and tunable, costly in hardware | Weight licence, dataset compliance |

No ranking is implied. Whole-song tools are fastest from nothing to listenable, symbolic tools are steadiest when one part must change, and local setups are safest when material cannot leave the building. They solve different problems; the table exposes the price of each.

## A selection sequence

1. Write down the deliverable: master, stems, MIDI, or several alternate versions.
2. Mark the inputs that must survive: lyrics, reference audio, an existing arrangement.
3. Set a control floor: which parameters must be exact and which may be left to chance.
4. Check licensing: commercial use, and what happens to uploaded material.
5. Run the same short real-world asset twice and compare repeatability and repair time.

Do not reverse the order. Listening before checking rights wastes work, and skipping the control floor lets a demo pull you off course.

## Where the matrix breaks

Demos showcase a model's best fragments, updates change old behaviour without notice, and licence terms split by region and tier. Treat the matrix as an exclusion tool. Retest with a small piece of your own material before trusting the conclusion. When exact harmony or long-form structure matters, the matrix can only point to a category worth trying; acceptance still belongs to you.
:::

