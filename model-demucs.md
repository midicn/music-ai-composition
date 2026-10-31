---
id: model-demucs
site: ai
cat: I
title: Demucs 系分轨模型
title_en: "Demucs-Family Stem Separation"
summary: 开源分轨模型，离线批量拆出人声、鼓、贝斯与其他。
summary_en: An open-source separation family that splits vocals, drums, bass and other offline, in batches.
level: standard
tags: [模型档案, 分轨, 开源, 离线, 源分离]
tags_en: [model profile, stem separation, open source, offline, source separation]
alias: [Demucs, 开源分轨, 本地分轨, htdemucs, source separation model]
order: 11
model_vendor: Meta（Facebook Research）
model_form: 本地模型
model_input: [混音音频]
model_output: [分轨]
model_licence: 代码许可与预训练权重许可要分开核对，训练素材的授权范围以官方仓库与数据集说明为准
model_verified: 2026-10-30
links:
  - "[[glossary:stems]]"
  - "[[glossary:phase]]"
  - "[[instrument:drum-kit]]"
instances:
  - oga-000001 | 编制拥挤的游戏管弦，声部多、频段重叠，是分离最难的一类素材（C1） | A crowded game orchestral score with many parts sharing bands, among the hardest material to separate (C1)
  - pdmx-000087 | 手风琴与室内编制，中频密集，能听出哪条轨被削薄（C1） | Accordion and chamber parts packed into the midrange, to hear which stem thins (C1)
  - m21-000000 | 四声部众赞歌，人声之间只差音区，串音最容易听出来（C1） | A four-part chorale whose voices differ only by register, where bleed is easiest to hear (C1)
  - groove-000008 | 灵魂乐鼓组，底鼓与贝斯抢同一段低频，适合看分离后的低频（C1） | A soul kit where kick and bass share the low band, for checking the low end after separation (C1)
sources:
  - Demucs 的模型结构与推理方式，参考公开论文摘要与仓库说明。
  - 分离残渣与低频损失的处理；混音实践惯例是主要依据。
updated: 2026-10-30
---

::: zh
## 能替你做完什么

把一个文件夹里的混音批量拆成人声、鼓、贝斯与其他；给老歌做无伴奏草稿；从伴奏里截一段鼓或贝斯做采样；为训练别的模型准备对照素材；在没有网络的机器上处理不能上传的母带。

## 喂什么，拿什么

输入是混音音频文件，输出是每条分轨一个 wav，采样率与位深可设。模型内部会把音频重采样到自己的处理率再回到原率，长文件要留意起始对齐与延迟。命令行与 Python 接口都能调用，目录可以整批跑；有显卡时快，只有 CPU 时慢，但能跑完。

## 最好用的地方

- 完全离线，素材不出本机，适合未发行母带与客户保密项目。
- 可批量、可脚本化，结果与权重绑定，同一份输入重复跑能对齐。
- 人声与伴奏的分离在同级开源方案里稳定，够做草稿与采样。
- 一次输出多条轨，鼓、贝斯、人声、其他各自成文件，便于逐轨修。
- 不按分钟计费，成本是电与时间。

## 会翻车的地方

- 残渣：混响重、失真大、现场录音的素材，人声轨会带水声，伴奏轨会留人声影子。
- 低频：贝斯与底鼓共用频段，分离后低频常被削薄，或两条轨互相串。
- 鼓：镲片与军鼓的瞬态被抹圆，踩镲的金属感摊成一片噪声。
- 对齐：内部重采样带来毫秒级偏移，把分轨叠加回原轨会相位抵消，比较之前必须先对齐。
- 资源：长曲目吃显存，CPU 上跑一整张专辑要等很久，批量任务的排队要自己安排。
- 权重差异：不同权重的结果差别明显，换权重等于换工具，工程里要记下用了哪一版权重。

## 收费、授权与替代品

要确认的问题：代码许可与预训练权重许可是否一致？训练用的公开数据集是否允许商用？分离后的分轨仍受原录音版权约束，这一点有没有写进交付说明？拿分轨去训练自己的模型是否被允许？

价格：软件本身免费，成本是显卡与时间；他人搭好的托管版本按订阅或按量，以官方页面为准。

替代：LALAL.AI——不想装环境、要网页一键出结果时换它；UVR 一类带界面的工具——想试多种模型、不写命令时换它；iZotope RX——要在 DAW 里一边分离一边修的时候换它。

```audiolab
{"type":"instrument","gm":"Electric Bass (pick)","synth":"plucked","phrase":["E2","E2","G2","A2","A2","G2","E2","D2"],"label":"被拆出来的贝斯","label_en":"A bass part pulled from the mix","hint":"低频与底鼓共用一段频谱，分离后最先变薄的就是这里","hint_en":"Bass and kick share one band; this is where separation thins first"}
```
:::

::: en
## What it finishes for you

Batch-separate a folder of mixes into vocals, drums, bass and other; make an instrumental draft of an old song; cut a usable drum or bass fragment for sampling; prepare reference material for training another model; process a master that may not leave the machine.

## What goes in, what comes out

You input mixed audio files and get one wav per stem, with sample rate and bit depth set by you. Internally the model resamples to its own working rate and back, so on long files watch the start alignment and latency. Both a command line and a Python interface exist, and whole directories can be processed; a GPU is fast, a CPU is slow but finishes.

## Where it shines

- Fully offline, so unreleased masters and confidential client work stay on the machine.
- Batchable and scriptable, with results tied to a weight set; reruns of the same input align.
- Vocal and backing separation is steady among open-source options, enough for drafts and sampling.
- Several stems per run, each written as its own file for per-track repair.
- No per-minute billing; the cost is electricity and time.

## Where it falls over

- Residue: with heavy reverb, distortion or live recordings, the vocal stem turns watery and the backing keeps a vocal shadow.
- Low end: bass and kick share a band, so low end thins after separation or the two stems bleed into each other.
- Drums: cymbal and snare transients round off, and hi-hat metal smears into noise.
- Alignment: internal resampling shifts timing by milliseconds, so summing stems against the original cancels in phase unless you align first.
- Resources: long pieces eat video memory, and a whole album on CPU takes a long wait; batching is your own scheduling problem.
- Weight drift: results differ noticeably between weight sets, so swapping weights is swapping tools; record which set a project used.

## Cost, licence, alternatives

Questions to check: do the code licence and the pretrained weight licence agree? Does the public training dataset permit commercial use? Separated stems remain bound by the copyright of the original recording, so is that stated in your delivery notes? Is training your own model on the stems allowed?

Price: the software is free and the cost is hardware and time; hosted versions run by others are billed per subscription or per use, as stated on their official pages.

Alternatives: LALAL.AI when you do not want to install anything and need a one-click web result; a GUI tool in the UVR family when you want to try many models without commands; iZotope RX when separation and repair should happen in one place inside the DAW.

```audiolab
{"type":"instrument","gm":"Electric Bass (pick)","synth":"plucked","phrase":["E2","E2","G2","A2","A2","G2","E2","D2"],"label":"A bass part pulled from the mix","label_en":"A bass part pulled from the mix","hint":"Bass and kick share one band; this is where separation thins first","hint_en":"Bass and kick share one band; this is where separation thins first"}
```
:::
