---
id: model-riffusion
site: ai
cat: I
title: Riffusion（早期频谱模型）
title_en: Riffusion (early spectrogram model)
summary: 介绍早期riffusion-hobby的频谱扩散与音频还原
summary_en: This entry covers early riffusion-hobby spectrogram diffusion and audio reconstruction, not later online products.
level: standard
tags: [模型档案, 频谱生成, 循环, 低保真]
tags_en: [model profile, spectrogram, loops, lo-fi]
alias: [Riffusion, 频谱生成, 循环生成]
order: 5
model_vendor: Riffusion
model_form: 早期本地研究项目（riffusion-hobby）
model_form_en: Early local research project (riffusion-hobby)
model_input: [文本, 该实现支持的初始化频谱与采样设置]
model_input_en: [Text, Initialization spectrogram and sampling settings supported by that implementation]
model_output: [频谱表示, 还原音频]
model_output_en: [Spectrogram representations, Reconstructed audio]
model_licence: riffusion-hobby 代码为 MIT；模型权重许可及后续在线条款分别核对
model_licence_en: riffusion-hobby code is MIT; check model-weight licences and later online-service terms separately
model_verified: 2026-11-02
links:
  - "[[glossary:sampler]]"
  - "[[glossary:tempo]]"
  - "[[instrument:electronic-drums]]"
instances:
  - groove-000005 | 87 BPM 嘻哈鼓组，看循环的节奏骨架（C1） | An 87 BPM hip-hop kit, to hear a loop's rhythmic skeleton (C1)
  - groove-000002 | 86 BPM 灵魂乐鼓组，看低保真素材的松紧（C1） | An 86 BPM soul kit, to hear the looseness of lo-fi material (C1)
  - oga-000031 | 一段氛围循环，看可反复播放的短素材（C1） | An ambient loop, to hear a short repeating asset (C1)
  - groove-000007 | 65 BPM 摇滚鼓组，看慢速循环的呼吸（C1） | A 65 BPM rock kit, to hear the feel of a slow loop (C1)
sources:
  - "https://github.com/riffusion/riffusion-hobby"
  - 产品能力与生成方式（官方公开说明与条款页）。
  - 失败模式来自公开用户报告与创作实践，未引用具体评测数据。
updated: 2026-11-02
---

::: zh
## 用武之地

Riffusion 这个名称曾用于频谱图扩散生成音频的开源项目，也被用于后续在线音乐产品。讨论模型结构前，应先写清仓库或服务版本。早期 riffusion-hobby 适合研究文本、频谱与音频转换，不能据此推断当前在线产品只能生成短循环。

## 怎么给，给回什么

早期开源项目以文本条件生成频谱表示，再把它转换为音频。使用时保存仓库版本、模型权重、提示和采样参数；生成出来的声音是否能循环，需要另查首尾。后续在线产品的输入、分轨和导出能力应另按其当前文档核验，不能从旧模型结构直接推断。

## 最好用的地方

- 早期开源代码可用于研究频谱表示与音频转换。
- 对同一输入保留不同采样参数的结果，比较织体和瞬态。
- 将候选放进实际工程检验速度、长度和接缝，不因短片段生成成功就认定适合交付。

## 会翻车的地方

评估早期频谱模型时，分别检查频谱重建伪影、瞬态和循环接缝，保留具体模型与采样参数。评估在线产品时，则按当前官方说明另验结构、输出和下载条件。没有公开对照测试，不应写成“比多数模型更对味”或“人声完全不能用”等通用排名。

## 收费、授权与替代品

早期代码与模型的许可，以及后续在线服务的条款，应分别核对。先确定使用的是哪一个项目，再检查生成文件的下载、修改和再分发条件。工具选型应围绕可控输入、可用输出和工程接续，不沿用跨代产品的音质排名。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E2","E2","G2","A2","E2","D2","E2","G2"],"label":"短贝斯乐句","label_en":"Short bass phrase","hint":"这是固定音符的循环素材参照，没有经过 Riffusion 的频谱生成或还原流程。","hint_en":"This fixed-note bass phrase is a loop reference, not output from Riffusion spectrogram generation or reconstruction."}
```
:::

::: en
## Where it earns its place

Riffusion has named both an open-source spectrogram-diffusion audio project and later online music products. Identify the repository or service version before describing architecture. The earlier riffusion-hobby project is useful for studying text, spectrograms and audio conversion; it does not establish that a current online product is limited to short loops.

## How you feed it, what it returns

The earlier open-source project generates a spectrogram representation from text conditioning and converts it to audio. Preserve repository version, weights, prompt and sampling settings; test loop boundaries separately. Inputs, stems and exports of later online products need their current documentation rather than inference from the old model architecture.

## Where it shines

- The earlier open-source code can support study of spectrogram representation and audio conversion.
- Keep results from different sampling settings for one input and compare texture and transients.
- Test tempo, duration and joins inside the actual session rather than treating successful clip generation as proof of delivery suitability.

## Where it falls over

For an early spectrogram model, inspect reconstruction artifacts, transients and loop boundaries, retaining model and sampling settings. For an online product, separately verify structure, outputs and downloads against current official documentation. Without a published comparison, avoid general rankings or blanket claims that vocals are unusable.

## Cost, licence, alternatives

Check licences for earlier code and models separately from later online-service terms. Identify the actual project before checking download, modification and redistribution conditions. Select tools by controllable inputs, available outputs and session handoff rather than carrying sound-quality rankings across generations.

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E2","E2","G2","A2","E2","D2","E2","G2"],"label":"Short bass phrase","label_en":"Short bass phrase","hint":"This fixed-note bass phrase is a loop reference, not output from Riffusion spectrogram generation or reconstruction.","hint_en":"This fixed-note bass phrase is a loop reference, not output from Riffusion spectrogram generation or reconstruction."}
```
:::
