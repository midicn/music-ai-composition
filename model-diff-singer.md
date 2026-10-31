---
id: model-diff-singer
site: ai
cat: I
title: DiffSinger 系（开源歌声合成）
title_en: DiffSinger
summary: 开源歌声合成，靠自建声库与音素标注。
summary_en: Open-source singing synthesis built on your own voicebanks and phoneme labels.
level: standard
tags: [模型档案, 开源, 歌声合成, 本地部署]
tags_en: [model profile, open source, singing synthesis, local]
alias: [DiffSinger, 开源歌声合成, 扩散歌声合成]
order: 9
model_vendor: DiffSinger 社区
model_form: 本地模型
model_input: [歌词, MIDI, 参考音频]
model_output: [人声轨, 音频]
model_licence: 代码许可与声库、训练数据许可分开核对，自建声库需演唱者同意
model_verified: 2026-10-30
links:
  - "[[instrument:voice]]"
  - "[[glossary:pitch]]"
  - "[[glossary:vibrato]]"
instances:
  - cyberhymnal-003336 | 中文歌词的赞美诗，看字与音的对应（C1） | A hymn with Chinese words, to hear syllables mapped to notes (C1)
  - mutopia-000546 | 艺术歌曲的人声线条，看连音与换气（C1） | An art-song vocal line, to hear legato and breath (C1)
  - mutopia-000527 | 通俗歌曲的人声与钢琴，看近麦吐字（C1） | A popular song for voice and piano, to hear close diction (C1)
  - cyberhymnal-002209 | 短小的赞美诗旋律，看短句的音高轮廓（C1） | A short hymn tune, to hear the pitch contour of a brief phrase (C1)
sources:
  - 项目结构、训练流程与输入形式，参考公开仓库说明。
  - 失败模式来自公开用户报告与自建声库经验，未引用具体评测数据。
updated: 2026-10-30
---

::: zh
## 用武之地

把歌词、MIDI 旋律与音素标注喂给它，得到一条唱出来的人声。可以只用社区已有的声库，也可以用自己的录音训练一套专属声库。适合要完全离线、要长期复用同一音色、或者要针对某种语言与唱法做定制的项目。它给的是人声轨，编曲与混音仍要自己做。

## 喂什么，拿什么

输入是歌词、MIDI 与时值，训练阶段还需要带音素标注的录音数据。输出是人声轨，可导出干声。整个流程在本地跑，模型文件与声库都要自己管理。可用的语言取决于音素词典与声库，不是所有语种都有现成方案。下面的试听与实例取自同类产出，供对照。

## 最好用的地方

- 完全本地，素材与声库不出机器，适合长期项目与保密内容。
- 音高与时值直接来自 MIDI，节奏与音准可以做到很精确，不靠提示词猜。
- 能用自己的录音训练声库，音色专属，不会被别人的声库限制。
- 开源，可以改模型结构、改前端处理，接进自己的批量流程。

## 会翻车的地方

- 上手门槛高：环境、依赖、声库与音素词典要自己配，初次跑通往往要花一整天。可复现的测法是拿一份新环境从零安装，看卡在哪一步。
- 中文多音字与儿化、轻声靠词典规则判断，错读要手动改音素；一句话里错一个字就得回头修。
- 声库质量差异极大，社区声库的录音条件与标注质量参差，同一个模型换声库像换了一套系统。
- 表情与换气要手画，默认输出偏平，长音尤其明显。
- 训练需要干净的录音与正确的标注，数据不够时会出现音色漂移与吞音。
- 只出人声，混响、压缩、齿音处理都要在编曲软件里补。

## 收费、授权与替代品

要确认：代码许可与声库许可分开看，社区声库能否商用各有权属声明；用真人录音训练声库要取得演唱者同意，训练数据来源也要能说明。软件本身开源，成本在算力与时间。
替代：要开箱可用、带技术支持，换 ACE Studio；只要器乐、不要人声，换 MusicGen。它适合"要离线、要专属音色、能自己维护"的团队。

```audiolab
{"type":"instrument","gm":"Synth Choir","synth":"vocal","phrase":["A3","C4","D4","E4","D4","C4","A3","G3"],"label":"一条按音高轮廓唱出的线","label_en":"A line sung to a pitch contour","hint":"这里用合成合唱代替声库，听的是音高落点与连音是否干净","hint_en":"A synthetic choir stands in for a voicebank; listen for pitch landing and clean legato"}
```
:::

::: en
## Where it earns its place

Feed it lyrics, a MIDI melody and phoneme labels and get a sung vocal. You can use an existing community voicebank or train a private one from your own recordings. It suits fully offline work, long-term reuse of one timbre, and custom projects for a particular language or delivery. It returns a vocal track; arrangement and mixing stay with you.

## What goes in, what comes out

Input is lyrics, MIDI and note lengths; training also needs recorded data with phoneme labels. Output is a vocal track, exportable dry. The whole pipeline runs locally, and you manage model files and voicebanks yourself. Language coverage depends on the phoneme dictionary and the voicebank, and not every language has a ready route. The listening examples and instances below are references for this kind of output, not this model's generations.

## Where it shines

- Fully local, so material and voicebanks stay on your machine, which suits long projects and confidential content.
- Pitch and duration come straight from MIDI, so rhythm and intonation can be exact rather than guessed from a prompt.
- You can train a voicebank on your own recordings for a timbre nobody else has.
- Open source, so the model and front end can be modified and wired into your own batch pipeline.

## Where it falls over

- The entry cost is high: environment, dependencies, voicebank and phoneme dictionary are yours to set up, and a first successful run often takes a full day. A reproducible test is a clean install from scratch, noting where it stalls.
- Mandarin polyphones, erhua and neutral tones depend on dictionary rules, and misreadings need manual phoneme edits; one wrong character sends you back into the line.
- Voicebank quality varies enormously, and community banks differ in recording and labelling, so swapping banks feels like swapping systems.
- Expression and breath are hand-drawn, and default output is flat, especially on long notes.
- Training needs clean recordings and correct labels; with too little data, timbre drifts and syllables drop.
- It produces voice only, so reverb, compression and sibilance work happen in the DAW.

## Cost, licence, alternatives

Confirm: code licence and voicebank licence are separate, and each community bank carries its own terms on commercial use; training on a real singer needs that singer's consent, and data provenance must be explainable. The software is open source, with cost in compute and time.
Alternatives: ACE Studio for something that works out of the box with support; MusicGen when you need instruments and no voice. This suits teams that need offline operation, a private timbre, and the ability to maintain it themselves.

```audiolab
{"type":"instrument","gm":"Synth Choir","synth":"vocal","phrase":["A3","C4","D4","E4","D4","C4","A3","G3"],"label":"A line sung to a pitch contour","label_en":"A line sung to a pitch contour","hint":"A synthetic choir stands in for a voicebank; listen for pitch landing and clean legato","hint_en":"A synthetic choir stands in for a voicebank; listen for pitch landing and clean legato"}
```
:::
