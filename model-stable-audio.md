---
id: model-stable-audio
site: ai
cat: I
title: Stable Audio
title_en: Stable Audio
summary: 涵盖音乐、音效与编辑的模型系列；输入、时长和部署方式按具体版本核对。
summary_en: A family for music, effects and editing; verify input, duration and deployment for the specific version.
level: standard
tags: [模型档案, 文本生成, 器乐, 音效]
tags_en: [model profile, text to music, instrumental, sound design]
alias: [Stable Audio, 稳定音频, 器乐生成]
order: 3
model_vendor: Stability AI
model_form: 网页、API及可下载权重（按模型）
model_form_en: Web, API and downloadable weights depending on model
model_input: [文本, 支持版本的音频条件与编辑素材]
model_input_en: [Text, Audio conditioning and editing material for supported variants]
model_output: [音频（时长及编辑功能按版本）]
model_output_en: [Audio with version-specific duration and editing features]
model_licence: 托管服务、开放权重和企业合同分别核对许可；以具体模型和入口为准
model_licence_en: Check hosted-service, open-weight and enterprise terms separately for the exact model and interface
model_verified: 2026-11-02
links:
  - "[[glossary:sampler]]"
  - "[[instrument:polysynth]]"
  - "[[glossary:reverb]]"
instances:
  - oga-000031 | 一段氛围循环，看铺底类素材的层次（C1） | An ambient loop, to hear the layering of bed material (C1)
  - groove-000001 | 105 BPM 放克鼓组，看循环的律动密度（C1） | A 105 BPM funk kit, to hear the density of a loop (C1)
  - oga-000009 | 海滩场景的短铺底，看环境声与器乐怎么混（C1） | A short beach cue, to hear ambience mixed with instruments (C1)
  - mutopia-000059 | 赞美诗旋律，看两小节就能成立的短动机（C1） | A hymn tune, to hear a motif that works in two bars (C1)
sources:
  - "https://stability.ai/stable-audio"
  - 产品能力、时长设置与导出形态（官方公开说明与条款页）。
  - 失败模式来自公开用户报告与创作实践，未引用具体评测数据。
updated: 2026-11-02
---

::: zh
## 具体的产出

Stable Audio 是包含不同代际与用途的模型/服务系列，不能把早期短片段模型的限制套到整个系列。截至 2026-11-02，官网介绍 Stable Audio 3.0，列出最长六分钟的完整曲目生成，以及片段修改、重做和延长等编辑用途。实际可用功能须对应具体模型与使用入口。

## 怎么给，给回什么

输入和输出按具体模型、网页或 API 文档核对：文本生成、音频条件和编辑不是每个版本都相同。需要固定时长、立体声、分轨或可编辑音符时，先做一次导出试验并检查文件属性。生成段落可用，不等于首尾已无缝或符合目标画面的节奏。

## 最好用的地方

- 先确认任务要完整曲目、音效还是局部修改，选择相应模型。
- 固定一条参考素材和目标时长，检查结构、音色与结束方式是否适用。
- 循环素材应另验首尾衔接，不能因生成时长合适就假定无缝。
- 需要分轨、可编辑音符或指定演唱时，先验证入口是否提供相应输出。

## 会翻车的地方

检查授权输入是否被正确处理、关键音符和段落是否保留、结尾是否需要补剪。不要把某次结果的金属声、混响或低频量写成整个产品的恒定特性。本站 MIDI 可提供节奏或织体参照，但不是该模型生成的音频，也不证明它的控制能力。

## 收费、授权与替代品

核对所用模型与服务的许可、输入材料权利、输出再分发和当前账号能力。开源权重、托管服务与企业合同可能适用不同条件，不能用产品系列名称替代许可判断。先验证项目所需的下载和交付格式，再比较本地维护与在线服务的成本。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["D3","A3","F4","E4","D4","A3"],"label":"持续织体参照","label_en":"Sustained-texture reference","hint":"这段合成织体可用于描述编制与密度，不是 Stable Audio 的输出或稳定度测试。","hint_en":"Use this synthesized texture to describe instrumentation and density; it is not Stable Audio output or a stability test."}
```
:::

::: en
## Concrete output

Stable Audio covers models and services from different generations and for different uses; early short-clip limitations do not describe the entire family. Checked on 2026-11-02, the official Stable Audio 3.0 page lists full tracks up to six minutes and segment modification, reworking and extension. Match capabilities to the specific model and interface being used.

## How you feed it, what it returns

Check inputs and outputs against the specific model, web interface or API documentation: text generation, audio conditioning and editing differ by version. Test export and file properties before relying on duration, stereo, stems or editable notes. A usable generated passage does not imply seamless looping or suitable picture timing.

## Where it shines

- Decide whether the task is a full track, sound effect or local edit and select the relevant model.
- Use one reference and target duration to assess structure, timbre and ending.
- Test loop boundaries separately; a suitable duration does not guarantee seamless looping.
- Verify stem, editable-note or vocal outputs before relying on them.

## Where it falls over

Check treatment of authorised inputs, retention of important notes and sections, and whether the ending needs editing. Artifacts, reverb or bass level in one result are not permanent properties of the whole product. The MIDI examples supply rhythmic or textural references; they are not outputs from this model and do not prove its controllability.

## Cost, licence, alternatives

Check the model and service licence, input rights, output redistribution and current account capabilities. Open weights, hosted services and enterprise agreements may have different conditions; a family name is not a permission check. Verify required downloads and delivery formats before comparing local maintenance with hosted cost.

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["D3","A3","F4","E4","D4","A3"],"label":"Sustained-texture reference","label_en":"Sustained-texture reference","hint":"Use this synthesized texture to describe instrumentation and density; it is not Stable Audio output or a stability test.","hint_en":"Use this synthesized texture to describe instrumentation and density; it is not Stable Audio output or a stability test."}
```
:::
