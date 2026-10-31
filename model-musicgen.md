---
id: model-musicgen
site: ai
cat: I
title: MusicGen
title_en: MusicGen
summary: 开源权重，能本地跑，短片段加旋律条件。
summary_en: Open weights you can run locally, short clips steered by a melody.
level: standard
tags: [模型档案, 开源, 本地部署, 旋律条件]
tags_en: [model profile, open source, local, melody conditioning]
alias: [MusicGen, Meta MusicGen, 音乐生成模型]
order: 4
model_vendor: Meta
model_form: 本地模型
model_input: [文本, 旋律, 参考音频]
model_output: [音频]
model_licence: 代码与权重分别核对，权重的商用范围以模型卡与随附许可为准
model_verified: 2026-10-30
links:
  - "[[glossary:melody]]"
  - "[[glossary:midi-protocol]]"
  - "[[instrument:piano]]"
instances:
  - mutopia-000059 | 四十三秒的赞美诗旋律，看短片段的条件素材——这是该类产出的参照，不是本模型生成（C1） | A forty-three second hymn tune, to hear material for short conditioned clips; a reference for this kind of output, not a MusicGen generation (C1)
  - abcmisc-001329 | 里尔舞曲，看可循环的短旋律——这是该类产出的参照，不是本模型生成（C1） | A reel, to hear a short loopable melody; a reference for this kind of output, not a MusicGen generation (C1)
  - groove-000002 | 86 BPM 灵魂乐鼓组，看文本描述的节奏目标——这是该类产出的参照，不是本模型生成（C1） | An 86 BPM soul kit, to hear the rhythmic target a text prompt describes; a reference for this kind of output, not a MusicGen generation (C1)
  - oga-000005 | 三十八秒的战斗配乐片段，看短促的器乐提示——这是该类产出的参照，不是本模型生成（C1） | A thirty-eight second battle cue, to hear a short instrumental prompt; a reference for this kind of output, not a MusicGen generation (C1)
sources:
  - 模型能力、条件输入与权重发布形态，对照官方模型说明整理。
  - 失败模式来自公开用户报告与本地实测经验，未引用具体评测数据。
updated: 2026-10-30
---

::: zh
## 它接什么活

用文本描述生成一段几十秒的器乐，或者给一段旋律让它按指定音色与风格配器。权重可以下载到本机，断网也能跑，适合批量试听、做素材库、在自有数据上继续训练。它给的是片段，不是完整的歌；要整首结构得自己拼接或另找工具。

## 怎么给，给回什么

输入是文本，可选一段音频作为旋律条件，让生成的音乐跟着这条旋律走。输出是音频文件，没有分轨，也没有 MIDI。本地部署时采样参数、时长与随机种子都能控制，同一种子可以复现同一条结果。下面的试听与实例只是该类产出的参照，不是本模型生成。

## 最好用的地方

- 本地运行，素材不出机器，适合有保密要求的项目。
- 旋律条件好用：给一条哼唱或单音旋律，配器会围着它走，做编曲草稿省事。
- 可以在自己的音频上继续训练，做出接近自家曲库音色的版本。
- 批量生成便宜，一次跑几十条再挑，适合做素材筛选。

## 会翻车的地方

- 不唱。所有人声请求都会变成含混的类人声纹理，别拿它做歌。
- 片段短，超过半分钟后容易原地打转：同一动机反复，结尾没有收束。可复现的测法是同提示生成两次，都在相似位置开始重复。
- 旋律条件给得太具体时，配器会跟着旋律的每个音走，和声被压平，听起来像伴奏在爬音阶。
- 文本里的配器与风格描述常被忽略一半，写"弦乐加电钢琴"往往只出现其中一件。
- 输出电平与立体声像不稳定，同一批素材要逐条处理才能放进工程。
- 默认质量与在线服务有差距，糊、闷、镲片发虚是常见问题，后期要补。

## 收费、授权与替代品

要确认：代码许可与权重许可是两件事，权重能否商用、能否用于训练衍生模型，都要看模型卡与随附许可；训练数据来源以官方说明为准。本地运行没有按次费用，但算力成本要自己算。
替代：要开箱可用的音质与更长片段，换 Stable Audio；要人声，换 DiffSinger 或 ACE Studio。它适合当"能改、能训、能离线"的那一档。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["G4","A4","B4","D5","B4","A4","G4","E4"],"label":"一条可作条件的短旋律","label_en":"A short melody to condition on","hint":"这类单线条旋律正是它最擅长的条件输入，配器应当围着它转","hint_en":"A single-line melody like this is its natural conditioning input; the arrangement should follow it"}
```
:::

::: en
## The jobs it takes

Generate a few dozen seconds of instrumental audio from a text description, or hand it a melody and ask for a given timbre and style around that line. The weights can be downloaded and run offline, which suits batch auditioning, building a sample library, and further training on your own audio. It returns clips, not songs; whole-form structure is your job or another tool's.

## How you feed it, what it returns

Input is text, optionally with an audio clip as a melodic condition so the output follows that line. Output is an audio file with no stems and no MIDI. Running locally, you control sampling parameters, duration and seed, and one seed reproduces one result. The listening examples and instances below are references for this kind of output, not this model's generations.

## Where it shines

- Local execution keeps material on your machine, which suits confidential work.
- Melody conditioning works: give a hummed or single-note line and the arrangement follows it, which speeds up arrangement sketches.
- You can continue training on your own audio to approach the timbre of your own catalogue.
- Batch generation is cheap, so running dozens of candidates and selecting is practical.

## Where it falls over

- It does not sing. Vocal requests become indistinct vocal-like texture, so it is not a song tool.
- Clips are short and start circling past half a minute: one motif repeats and the ending does not close. A reproducible test is two runs from one prompt; both start repeating around a similar point.
- Over-specific melody conditioning makes the accompaniment track every note, flattening the harmony into a scale-following part.
- Text descriptions of instrumentation are half ignored; ask for strings and electric piano and often only one appears.
- Output level and stereo image vary, so a batch needs per-file work before it enters a session.
- Default quality trails hosted services: muffled highs and soft cymbals are common and need post work.

## Cost, licence, alternatives

Confirm: code licence and weight licence are separate questions, and whether weights may be used commercially or to train derivatives belongs to the model card and its accompanying licence; training data provenance follows the official statement. Local runs carry no per-use fee, but you pay in compute.
Alternatives: Stable Audio for out-of-the-box quality and longer clips; DiffSinger or ACE Studio when you need singing. This is the option that you can modify, retrain and run offline.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["G4","A4","B4","D5","B4","A4","G4","E4"],"label":"A short melody to condition on","label_en":"A short melody to condition on","hint":"A single-line melody like this is its natural conditioning input; the arrangement should follow it","hint_en":"A single-line melody like this is its natural conditioning input; the arrangement should follow it"}
```
:::
