---
id: "tempo-key-and-form-in-prompts"
site: "ai"
cat: "B"
title: "速度、调性与曲式"
title_en: "Tempo, Key and Form"
summary: "速度写数字、调性写名称、曲式写段落，抽象的\"起伏\"换不来结构。"
summary_en: "Give tempo as a number, key by name and form as sections; \"flowing\" buys no structure."
level: "standard"
tags: ["速度", "调性", "曲式", "提示"]
tags_en: ["tempo", "key", "form", "prompt"]
alias: ["速度提示", "调性描述", "曲式描述", "tempo in prompts"]
order: 4
links: ["[[glossary:tempo]]", "[[glossary:key]]", "[[glossary:ternary-form]]"]
instances: []
sources: ["https://stability.ai/guides/stable-audio-3-prompt-guide", "https://help.suno.com/en/articles/6141505"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "提示中的速度、调性与曲式是待核验的控制目标，需结合平台字段及生成后分析；随意播放同速度曲目无法证明模型遵守了这些约束。"
---

::: zh
## 问题

提示里写"有起伏""有层次"，模型只能给出模糊的变化。速度、调性与曲式是可以写死的三个参数，写清楚它们，结构才有骨架。

## 怎么写

速度用数字加单位，如 86 BPM；要变速就写清在哪个段落变、变到多少。调性用调名，如 D 小调；需要无调性或调式色彩时说清楚。曲式用段落名，如"前奏八小节、主歌、副歌、间奏、副歌、尾奏"，并说明各段长度与重复关系。段落的情绪变化单独写，别和结构混在一起。

## 做法

先定曲式框架，再逐段写提示。段落之间要有明确的接入方式：直接进入、渐强过渡还是留白。需要回到主题时写明"回到第一段材料"。生成后检查段落是否真的出现，缺少哪段就单独补。变速段落最好分段生成，避免模型把速度平均掉。
:::

::: en
## The problem

Prompts that ask for "rise and fall" or "layers" leave the model guessing. Tempo, key and form are three parameters that can simply be stated, and stating them gives structure a skeleton.

## How to write them

Give tempo as a number and unit, such as 86 BPM; for changes, say which section moves and to what. Name the key, such as D minor, and state it when atonality or modal colour is wanted. Describe form with section names, such as intro of eight bars, verse, chorus, interlude, chorus, outro, plus lengths and repeats. Write emotional change separately from structure.

## Practice

Fix the form first, then prompt section by section. Say how sections connect: straight in, crescendo, or silence. When material returns, write "return to the first section's material". After generation, check whether the sections actually appear and add whichever is missing. Tempo changes are safer generated per section so the model does not average them away.
:::

