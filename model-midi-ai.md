---
id: model-midi-ai
site: ai
cat: I
title: MIDI 生成模型
title_en: "Symbolic MIDI Generation"
summary: 生成音符而不是音频，能改能移调，但结构要人来收。
summary_en: It writes notes rather than audio, editable and transposable, but the structure is yours to finish.
level: standard
tags: [模型档案, MIDI, 符号生成, 动机, 编曲]
tags_en: [model profile, MIDI, symbolic generation, motif, arrangement]
alias: [MuseNet, Magenta, Music Transformer, MIDI 生成, 符号音乐生成]
order: 16
model_vendor: OpenAI · Google Magenta
model_form: 本地模型
model_input: [MIDI, 风格提示, 乐器组合]
model_output: [MIDI]
model_licence: 各项目的代码与权重许可不同，训练 MIDI 的来源与商用范围需按仓库说明核对
model_verified: 2026-10-30
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:phrase]]"
  - "[[instrument:piano]]"
instances:
  - giantmidi-000004 | 主题与变奏，结构与重复关系清楚，适合看模型能不能接住动机——这是该类产出的参照，不是本模型生成（C1） | A theme and variations with clear repetition, to see whether a model can catch the motif; a reference for this kind of output, not a generation by this model (C1)
  - m21-000003 | 四声部众赞歌，声部进行与和声约束密集，生成的错误最容易听出——这是该类产出的参照，不是本模型生成（C1） | A four-part chorale dense with voice-leading and harmonic constraints, where generated errors are audible; a reference for this kind of output, not a generation by this model (C1)
  - oga-000005 | 游戏战斗配乐，多轨 MIDI 结构典型，适合做续写与配器试验——这是该类产出的参照，不是本模型生成（C1） | Typical multi-track game battle MIDI, useful for continuation and orchestration trials; a reference for this kind of output, not a generation by this model (C1)
  - giantmidi-000001 | 沙龙风格小品，句法与终止式规整，便于判断生成段是否跑题——这是该类产出的参照，不是本模型生成（C1） | A salon-style miniature with regular phrasing and cadences, for judging whether generated bars wander; a reference for this kind of output, not a generation by this model (C1)
sources:
  - 符号音乐生成的代表项目与输出形态，依公开仓库与论文摘要核对，未抄原文
  - MIDI 生成结果的后期修剪，依编曲实践通识核对，未抄文本
updated: 2026-10-30
---

::: zh
## 它能做什么

续写四到八小节，给你一个能往下改的开头；给一条旋律配和声、低音或鼓；把一段材料"翻译"成另一种乐器组合；批量生成几十个动机供挑选；给教学做风格示例；输出多轨 MIDI，进 DAW 后自己分配音色。

## 输入与输出

输入是 MIDI 片段、风格与乐器标签，部分模型还接受温度一类采样参数；输出是 MIDI 文件或实时音符流，通常多轨、已量化。它不输出音频，音色、力度与演奏法要你在 DAW 或音源里补。生成长度按小节计，长曲要分段续写再拼。

## 强项

- 结果是音符，改一个音不用重新生成，编辑成本低。
- 文件小，可进版本管理，也能直接进记谱软件。
- 能生成多声部，适合看声部关系而不是只听音色。
- 适合做动机、低音线与鼓的草案，铺开速度比手写快。
- 训练与推理成本低，本地跑不依赖网络。
- 与 DAW、记谱软件衔接顺，量化后的片段可以直接拖进工程。

## 弱项与翻车点

- 长结构：超过几十秒就开始重复或跑题，段落之间的过渡靠人补。
- 和声：平行五度、声部交叉、越界音域都会出现，尤其是四声部写作。
- 节奏：输出被量化到网格，切分与摇摆的细微前后被抹平，鼓听起来发硬。
- 表情：力度、连奏与踏板大多缺失，同一段音符听上去像打字。
- 风格：学到的是统计相似，不是写作规则，模仿到细节时容易露馅。
- 返工率：能直接用的段落比例低，筛选与修剪的时间常被低估。

## 条款、价格与替代

要确认的问题：权重是否公开、许可是什么？训练用的 MIDI 是否包含受版权保护的作品？生成 MIDI 的版权归属如何约定？商用是否要求署名？把生成片段再分发给客户是否受限？

价格：开源项目免费，算力自备；托管服务按订阅或按量，以官方页面为准。

替代：AIVA——要成品音频与配器、不想自己写声部时换它；Scaler 一类和声工具——要可控的和弦进行而不是生成时换它；MuseNet 一类演示——只想试听风格走向时用它。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","A4","G4","E4","D4","G3"],"label":"一段可继续写的动机","label_en":"A motif to continue","hint":"先听它停在哪里，续写常从这个位置开始重复","hint_en":"Hear where it stops; continuation often starts repeating from there"}
```
:::

::: en
## What it lets you finish

Continue four to eight bars and hand you an opening worth editing; add harmony, a bass line or drums under a melody; translate a passage into another instrument group; generate dozens of motifs to choose from; produce style examples for teaching; export multi-track MIDI and assign sounds yourself in the DAW.

## Inputs and outputs

You input a MIDI fragment plus style and instrument tags, and some models accept sampling parameters such as temperature; the output is a MIDI file or a live note stream, usually multi-track and quantised. No audio comes out: sounds, velocities and articulation are added in the DAW or a sample library. Length is counted in bars, so longer pieces are continued in sections and joined.

## Strengths

- The result is notes, so changing one costs nothing and editing stays cheap.
- Small files fit version control and open directly in notation software.
- It writes several parts at once, which lets you judge voice leading rather than timbre alone.
- Good for motifs, bass lines and drum drafts, faster to spread out than writing by hand.
- Low training and inference cost, and local runs need no network.
- Fits DAWs and notation tools; quantised fragments drop straight into a project.

## Weaknesses and failure modes

- Long form: after a few dozen seconds it repeats or wanders, and transitions between sections are yours to write.
- Harmony: parallel fifths, voice crossing and out-of-range notes appear, especially in four-part writing.
- Rhythm: output is snapped to the grid, so the small push and pull of syncopation and swing is flattened and drums sound stiff.
- Expression: velocity, legato and pedalling are mostly missing, and the same notes read like typing.
- Style: it learns statistical resemblance, not the rules of writing, and imitation shows at the details.
- Rework: the share of usable bars is low, and the time spent auditioning and trimming is routinely underestimated.

## Terms, price and alternatives

Questions to check: are the weights public, and under what licence? Does the training MIDI include copyrighted works? How is copyright in generated MIDI assigned? Is credit required for commercial use? Are there limits on passing generated fragments to clients?

Price: open projects are free with your own compute; hosted services bill per subscription or per use, as stated on the official pages.

Alternatives: AIVA when you want finished audio and orchestration without writing parts; a harmony tool such as Scaler when you want a controlled chord progression rather than generation; a demo such as MuseNet when you only want to hear where a style goes.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","A4","G4","E4","D4","G3"],"label":"A motif to continue","label_en":"A motif to continue","hint":"Hear where it stops; continuation often starts repeating from there","hint_en":"Hear where it stops; continuation often starts repeating from there"}
```
:::
