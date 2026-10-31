---
id: model-stable-audio-open
site: ai
cat: I
title: Stable Audio Open
title_en: Stable Audio Open
summary: 开放权重的音效与循环模型，四十七秒，商用有门槛。
summary_en: Open-weight audio for effects and loops, forty-seven seconds, with a commercial threshold.
level: standard
tags: [模型档案, 开放权重, 音效, 本地部署]
tags_en: [model profile, open weights, sound design, local deployment]
alias: [Stable Audio Open, SAO, 稳定音频开放版]
order: 207
model_vendor: Stability AI
model_form: 本地模型
model_input: [文本, 音频]
model_output: [音频]
model_licence: Stability AI 社区许可：年收入低于门槛可商用，超过需企业许可；开放权重不等于无条件开源
model_verified: 2026-10-31
links:
  - "[[glossary:sampler]]"
  - "[[instrument:polysynth]]"
  - "[[glossary:sample-rate]]"
instances:
  - groove-000001 | 105 BPM 放克鼓组，看循环素材的瞬态（C1） | A 105 BPM funk kit, to hear the transients of loop material (C1)
  - oga-000009 | 三十一秒的海滩场景铺底，看环境声与器乐的混合（C1） | A thirty-one second beach bed, to hear ambience mixed with instruments (C1)
  - mutopia-000059 | 四十三秒的赞美诗旋律，看短素材的完整性（C1） | A forty-three second hymn tune, to hear whether a short asset feels complete (C1)
  - cyberhymnal-002209 | 十八秒的中国旋律，看极短片段能不能成立（C1） | An eighteen second Chinese melody, to see whether a very short clip holds up (C1)
sources:
  - Stability AI 的 Stable Audio Open 模型卡（训练数据、时长、采样率与许可）。
  - Stability AI 社区许可文本（商用门槛与企业授权）。
  - 公开用户报告中的循环接缝、低频不稳与人声缺失问题，只取现象，不引用具体评测数据。
updated: 2026-10-31
---

::: zh
## 开放权重，但不是随便用

Stable Audio Open 的权重能下载、能本地跑、能用 LoRA 微调，但许可不是 MIT 那种随便用。Stability AI 社区许可允许年收入低于门槛的组织商用，超过门槛要企业授权；再分发、托管服务、拿产出训练别的模型，另有约束。先读模型卡，再决定它能不能进你的交付链。它是 2024 年那一代开放权重，和后来的 Stable Audio 3.0 系列不是同一套规格。

## 文本到声音，四十七秒

输入是文字描述，也可以拿一段音频做音频到音频；输出是 44.1kHz 立体声，单段最长约四十七秒。它不做歌曲，不唱人声，强项是音效、环境声、鼓循环、器乐铺底。描述里写“温暖的模拟合成器铺底、轻微磁带噪声”，比写“悲伤”有用；具体时长与采样率以模型卡为准。

## 采样、循环与音效

它的训练数据来自 CC 授权的音频库，风格偏电子、氛围、实地录音，做采样包和游戏音效很合适。鼓循环的瞬态干净，环境铺底的空间感也够；但首尾不做无缝处理，直接循环会有接缝，要自己在 DAW 里切。低频量在不同批次间不稳，做一套素材要逐条归一。

| 用途 | 合适度 | 注意 |
|---|---|---|
| 环境铺底 | 高 | 首尾淡入淡出 |
| 鼓与打击循环 | 高 | 接缝与低频 |
| 器乐动机 | 中 | 结构弱、易重复 |
| 带人声的歌 | 低 | 不唱词 |

## 本地部署的硬件与质量

消费级显卡能跑，显存随批大小与采样步数变化；生成速度与长度成反比，四十七秒是硬上限，做长铺底要拼接。提示遵循度中等，具体乐器与风格常被“平均化”；同一提示的响度与音色漂移明显。它适合当素材机，不适合当终混的成品源。想在 DAW 里反复试，配一个固定种子与提示模板，能减少漂移。

## 许可门槛与替代品

要确认：年收入门槛、企业授权、产出能否再分发为采样库、能否用于托管服务、微调后的权重如何标注。具体以 Stability AI 社区许可与模型卡为准。替代：要更长、更新的开放权重，看 Stable Audio 3.0 系列；要整曲与人声，换 YuE 或 MiniMax Music；要本地音效，也可对比 MusicGen。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C3","G3","D4","E4","D4","G3","C3"],"label":"一段四十秒以内的铺底","label_en":"A bed that fits inside forty seconds","hint":"听首尾能不能接上，循环接缝比音色更先暴露问题","hint_en":"Hear whether the ends meet; the loop seam shows up before timbre does"}
```
:::

::: en
## Open weights, not a free-for-all

Stable Audio Open can be downloaded, run locally and fine-tuned with LoRA, but the licence is not MIT-style. The Stability AI Community License allows commercial use below a revenue threshold; above it you need an enterprise licence, and redistribution, hosted services and using output to train other models carry further limits. Read the model card before it enters your delivery chain. This is the 2024 open-weight generation, not the same specification as the later Stable Audio 3.0 family.

## Text to sound, forty-seven seconds

Input is a text description, optionally audio for audio-to-audio; output is 44.1kHz stereo, up to about forty-seven seconds per clip. It does not make songs or sing, and its strength is effects, ambience, drum loops and instrumental beds. "Warm analogue synth pad with light tape hiss" works better than "sad"; exact duration and sample rate belong to the model card.

## Samples, loops and effects

Training audio comes from CC-licensed libraries, with a tilt toward electronic, ambient and field recording, which suits sample packs and game sound. Drum transients are clean and ambient beds have depth, but the ends are not seam-matched, so looping the file as-is clicks and needs trimming in a DAW. Low-end level varies between batches, so a set of assets needs per-file normalisation.

| Use | Fit | Watch |
|---|---|---|
| Ambient beds | High | Fades at both ends |
| Drum and percussion loops | High | Seams and low end |
| Instrumental motifs | Medium | Weak structure, repetition |
| Songs with vocals | Low | No words |

## Local hardware and quality

A consumer GPU is enough, with VRAM depending on batch size and sampling steps; speed falls as length rises, and forty-seven seconds is a hard ceiling, so long beds need stitching. Prompt adherence is moderate and specific instruments and styles get averaged out; loudness and timbre drift between runs from one prompt. Treat it as a material generator, not a final source. For repeated DAW tests, fix a seed and a prompt template to reduce drift.

## Licence threshold and alternatives

Confirm: the revenue threshold, enterprise licensing, whether output may be redistributed as a sample library, whether hosted services are allowed, and how fine-tuned weights must be labelled. The Stability AI Community License and model card are the authority. Alternatives: the Stable Audio 3.0 family for longer, newer open weights; YuE or MiniMax Music for songs and vocals; MusicGen as another local sound option.
:::
