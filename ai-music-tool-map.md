---
id: "ai-music-tool-map"
site: "ai"
cat: "A"
title: "工具地图"
title_en: "A Map of the Tools"
summary: "AI 做音乐不是一个大工具，而是一串各管一段的小工具。"
summary_en: "AI music is not one big tool but a chain of small ones, each owning one stage."
level: "standard"
tags: ["工具地图", "工作流", "选型", "AI"]
tags_en: ["tool map", "workflow", "selection", "AI"]
alias: ["工具地图", "AI 工具", "tool map"]
order: 1
links: ["[[glossary:daw]]", "[[glossary:stems]]", "[[glossary:midi-protocol]]"]
instances: []
sources: ["https://github.com/facebookresearch/audiocraft", "https://elevenlabs.io/docs/overview/capabilities/music"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页区分符号生成、成品音频和在线服务，需要核对项目文档的能力与工作阶段；普通曲库试听不能证明工具分类或实际功能。"
---

::: zh
## 问题

"用 AI 做音乐"听起来像一件事，实际是一条链：想清楚要什么、写出描述、生成素材、拆分声部、修改细节、混音、母带、交付。每一段都有专门的工具，也有能一次做完但每段都不精的工具。先有地图，才谈得上选型。

## 工具地图

按输入输出分四类。文本到音频：给一段描述，直接出成品或片段。音频到音频：给参考音频，做风格迁移、续写或分轨。符号类：处理 MIDI 与乐谱，可控性最高，音色要靠采样库。辅助类：分轨分离、修音、母带、音效生成，不直接作曲但省时间。多数人的实际流程是几类混用，而不是只用一类。

## 怎么选

先问交付物是什么：一首完整的歌、一段配乐、一组可编辑的分轨，还是几个音效。完整的歌适合文本到音频再加人工修饰；要进 DAW 继续改，就要能导出分轨或 MIDI；影视与游戏要能对齐时间码。再问可控性要求：能接受抽卡式生成，还是必须指定和声与配器。最后问权利：输出能否商用，训练数据是否清楚。
:::

::: en
## The problem

"Making music with AI" sounds like one task but is a chain: decide what you want, describe it, generate material, split parts, fix details, mix, master, deliver. Each stage has dedicated tools, and there are all-in-one tools that do every stage adequately but none well. A map comes before a choice.

## The map

Four groups by input and output. Text to audio takes a description and returns a finished track or a fragment. Audio to audio takes reference audio for style transfer, continuation or separation. Symbolic tools work on MIDI and scores, offering the most control but relying on sample libraries for sound. Assistants handle stem separation, tuning, mastering and sound effects, saving time without composing. Most real workflows mix several groups rather than staying in one.

## Choosing

Ask what the deliverable is first: a finished song, a cue, editable stems, or a handful of sound effects. A finished song suits text to audio plus manual polish; anything going back into a DAW needs stems or MIDI; film and game work needs timecode alignment. Then ask how much control you need: is a slot-machine generation acceptable, or must harmony and orchestration be specified. Finally ask about rights: can the output be used commercially, and is the training data accounted for.
:::

