---
id: "model-musicgen"
site: "ai"
cat: "I"
title: "MusicGen"
title_en: "MusicGen"
summary: "可本地运行的音乐生成模型；旋律条件需选对应检查点，官方权重为非商业许可。"
summary_en: "Locally runnable music generation; melody conditioning requires a supported checkpoint and official weights carry a non-commercial licence."
level: "standard"
tags: ["模型档案", "开源", "本地部署", "旋律条件"]
tags_en: ["model profile", "open source", "local", "melody conditioning"]
alias: ["MusicGen", "Meta MusicGen", "音乐生成模型"]
order: 4
model_vendor: "Meta"
model_form: "本地模型"
model_form_en: "Local model"
model_input: ["文本", "音频提示", "melody版本的旋律条件"]
model_input_en: ["Text", "Audio prompts", "Melody conditioning for the melody variant"]
model_output: ["音频"]
model_output_en: ["Audio"]
model_licence: "AudioCraft 代码为 MIT；官方 MusicGen 权重为 CC BY-NC 4.0，衍生权重另查"
model_licence_en: "AudioCraft code is MIT; official MusicGen weights are CC BY-NC 4.0; check derivatives separately"
model_verified: "2026-11-02"
links: ["[[glossary:melody]]", "[[glossary:midi-protocol]]", "[[instrument:piano]]"]
instances: ["mutopia-000059", "abcmisc-001329", "groove-000002", "oga-000005"]
sources: ["https://github.com/facebookresearch/audiocraft", "https://huggingface.co/facebook/musicgen-small", "模型能力、条件输入与权重发布形态，对照官方模型说明整理。", "失败模式来自公开用户报告与本地实测经验，未引用具体评测数据。"]
updated: "2026-11-03"
---

::: zh
## 它接什么活

用文本描述生成一段几十秒的器乐，或者给一段旋律让它按指定音色与风格配器。权重可以下载到本机，断网也能跑，适合批量试听、做素材库、在自有数据上继续训练。它给的是片段，不是完整的歌；要整首结构得自己拼接或另找工具。

## 怎么给，给回什么

MusicGen 有不同检查点，旋律条件需选支持该输入的 melody 版本，不能假定 small、medium、large 都接受同一种条件。输出是音频，不是现成分轨或 MIDI。固定种子有助于重复实验，但还需保留检查点、代码、依赖、硬件与采样设置；跨环境不应承诺逐位相同。

## 最好用的地方

- 在固定本地环境中保存检查点与推理设置，便于重复试验。
- 支持旋律条件的版本可比较输入旋律与生成音频的关系，仍需检查和声与结构。
- 批量处理可提高筛选效率，但安装、算力和维护仍有成本。
- 自有数据训练要另查数据和权重许可，不能由本地运行推导商业权限。

## 会翻车的地方

先用短片段验证提示和旋律条件是否起作用，再比较多次采样的结构、织体与结尾。长段生成、含人声结果和复杂配器的表现会随检查点与参数而变，不应把一次听感写成固定失败规律。所附 MIDI 是参照素材，不是 MusicGen 的生成结果或质量测试集。

## 收费、授权与替代品

官方 AudioCraft 代码和模型权重的许可要分开查：代码采用 MIT，官方 MusicGen 权重标注 CC BY-NC 4.0，不能把“可以下载到本地”理解为默认允许商业项目。衍生模型与数据也须核对各自条件。算力费用、安装维护和项目授权应分别评估。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["G4","A4","B4","D5","B4","A4","G4","E4"],"label":"单线条旋律","label_en":"Single-line melody","hint":"听旋律的音高与时值；这是条件素材的概念参照，没有把音频送入 MusicGen 生成伴奏。","hint_en":"Hear pitch and duration as a conceptual conditioning reference; this block does not send audio into MusicGen to generate accompaniment."}
```
:::

::: en
## The jobs it takes

Generate a few dozen seconds of instrumental audio from a text description, or hand it a melody and ask for a given timbre and style around that line. The weights can be downloaded and run offline, which suits batch auditioning, building a sample library, and further training on your own audio. It returns clips, not songs; whole-form structure is your job or another tool's.

## How you feed it, what it returns

MusicGen has distinct checkpoints: melody conditioning requires the supported melody variant, not an assumption that small, medium and large accept identical conditions. Output is audio rather than ready-made stems or MIDI. A seed helps repeat experiments, but checkpoint, code, dependencies, hardware and sampling settings must also be recorded; bit-identical output across environments is not guaranteed.

## Where it shines

- Preserve checkpoints and inference settings in a fixed local environment for repeat experiments.
- A melody-conditioned variant allows comparison with an input tune, while harmony and structure still need checking.
- Batch processing can aid selection but still incurs setup, compute and maintenance cost.
- Check data and weight permissions separately for training; local execution does not imply commercial permission.

## Where it falls over

Test prompt and melody conditioning on short clips before comparing structure, texture and endings across samples. Longer output, vocal-like material and complex instrumentation depend on checkpoint and settings rather than one fixed failure pattern. The linked MIDI is reference material, not MusicGen output or an evaluation set.

## Cost, licence, alternatives

Check AudioCraft code and model weights separately: the code uses MIT, while official MusicGen weights are labelled CC BY-NC 4.0. Being downloadable does not imply permission for commercial projects. Check conditions for derived models and data separately, and assess compute, maintenance and project permission as distinct questions.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["G4","A4","B4","D5","B4","A4","G4","E4"],"label":"Single-line melody","label_en":"Single-line melody","hint":"Hear pitch and duration as a conceptual conditioning reference; this block does not send audio into MusicGen to generate accompaniment.","hint_en":"Hear pitch and duration as a conceptual conditioning reference; this block does not send audio into MusicGen to generate accompaniment."}
```
:::

