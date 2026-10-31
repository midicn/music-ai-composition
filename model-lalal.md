---
id: model-lalal
site: ai
cat: I
title: LALAL.AI 在线分轨
title_en: "LALAL.AI Online Stem Separation"
summary: 上传即拆的在线分轨服务，人声、伴奏与多种乐器分开。
summary_en: A web separation service that splits a track into vocals, backing and individual instruments after upload.
level: standard
tags: [模型档案, 分轨, 在线服务, 人声分离, 翻唱]
tags_en: [model profile, stem separation, web service, vocal isolation, cover]
alias: [LALAL, LALAL.AI, 在线分轨, 人声分离服务, lalal ai]
order: 12
model_vendor: LALAL.AI
model_form: 网页服务
model_input: [音频, 视频]
model_output: [分轨, 人声]
model_licence: 上传内容的保留与使用、产出商用、各档位差异需按官方条款核对，训练数据未公开
model_verified: 2026-10-30
links:
  - "[[glossary:stems]]"
  - "[[glossary:sample-clearance]]"
  - "[[instrument:popular-voice]]"
instances:
  - pdmx-000048 | 波萨诺瓦编制，人声与吉他、贝斯贴得近，适合看人声轨的残渣——这是该类产出的参照，不是本模型生成（C1） | A bossa arrangement with the voice close to guitar and bass, for checking residue in the vocal stem; a reference for this kind of output, not a generation by this model (C1)
  - pdmx-000135 | 小编制歌曲，乐器少但混响多，人声轨容易留住空间感——这是该类产出的参照，不是本模型生成（C1） | A small-ensemble song, few instruments but plenty of reverb, where the vocal stem keeps its space; a reference for this kind of output, not a generation by this model (C1)
  - pdmx-000107 | 手风琴与弦乐为主的舞曲，中频拥挤，适合看乐器分离——这是该类产出的参照，不是本模型生成（C1） | A dance piece led by accordion and strings with a crowded midrange, for checking instrument separation; a reference for this kind of output, not a generation by this model (C1)
  - oga-000006 | 游戏战斗配乐，鼓与铜管密集，适合看瞬态是否被保留——这是该类产出的参照，不是本模型生成（C1） | Dense game battle music with drums and brass, for checking whether transients survive; a reference for this kind of output, not a generation by this model (C1)
sources:
  - 在线分轨的输入输出与档位（服务官方页面）。
  - 上传素材的隐私与版权处理，参考服务条款与惯例。
updated: 2026-10-30
---

::: zh
## 能替你做完什么

把一首成品歌拆成人声与伴奏，再按需分出鼓、贝斯、钢琴、吉他等声部；给翻唱做无人声伴奏；给采样找一段干净的鼓或贝斯；把现场录像里的对白或演唱单独拎出来；在不装软件的情况下处理客户的急件。

## 输入与产出

输入是音频或视频文件，上传后选择要拆的声部，服务返回可试听、可下载的分轨，格式与位深在下载时选。视频会先取音轨再处理。免费档能处理多长、能下载什么，以官方页面为准；付费按分钟或按文件计。上传文件保留多久、是否用于改进模型，写在条款里，用前要读。

## 最好用的地方

- 零安装，浏览器里几步出结果，不碰命令行。
- 声部选项多，除了人声与伴奏，还能单独取鼓、贝斯、钢琴等。
- 处理整首歌，前奏、间奏、尾奏一起拆，不用自己切段。
- 附带的人声清洁功能，对去回声与降噪有帮助，具体项目以官方页面为准。
- 结果直接下载进 DAW，适合非技术岗位与临时需求。

## 会翻车的地方

- 排队与时长：免费档限制多，长节目或批量任务要反复上传，进度不受自己控制。
- 隐私：上传意味着素材离开本机，未发行作品与保密对白不适合走这条路径。
- 残渣：混响重的人声会带空间感，密集混音的低频会被削，鼓的瞬态变圆。
- 不可复现：服务端模型会更新，同一素材隔一段时间再处理，结果可能不同，工程复现要保留当次分轨。
- 转码损失：上传压缩格式再拆分，等于在已经损失过的素材上做第二次处理，齿音与高频最先坏。
- 计费方式：按分钟计费时，反复试参数会直接增加成本，先想清楚要哪几轨再一次处理。

## 收费、授权与替代品

要确认的问题：上传内容的所有权是否仍归你？服务是否拿上传素材训练模型？文件保留多久、能否手动删除？产出用于商业发行是否要额外授权？把分轨再分发给第三方是否允许？

价格按分钟包或套餐计，档位差别在时长、声部数量与下载格式；地区可用性以官方页面为准。

替代：Demucs——要离线、批量、可复现时换它；iZotope RX——要把分离与修复放在同一个工程里时换它；Adobe Enhance——只需要把对白修干净、不拆音乐时换它。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["C4","E4","G4","A4","G4","E4","D4","C4"],"label":"从混音里留下的人声","label_en":"The vocal left after separation","hint":"听混响尾音是否跟着人声一起被留下","hint_en":"Hear whether the reverb tail comes along with the voice"}
```
:::

::: en
## What it finishes for you

Split a finished song into vocals and backing, then take drums, bass, piano or guitar separately; make an instrumental for a cover; pull a clean drum or bass fragment for sampling; lift a vocal or a line of dialogue out of a live video; handle a client's rush job without installing anything.

## Input and output

You upload audio or video, choose the parts to take, and the service returns stems you can preview and download, with format and bit depth chosen at download. Video is stripped to its audio first. What the free tier accepts and lets you download is as stated on the official pages, and paid use is metered by minute or by file. How long uploads are kept and whether they feed model improvement are stated in the terms and should be read before use.

## Where it shines

- No install: a few steps in a browser, no command line.
- Many part options beyond vocals and backing, including drums, bass and piano.
- Works on a whole song, intros, breaks and endings included, without manual cutting.
- Built-in voice cleanup helps make a stem usable; the exact options are listed on the official pages.
- Results download straight into a DAW, which suits non-technical roles and one-off jobs.

## Where it falls over

- Queues and limits: free use is restricted, so long programmes and batches mean repeated uploads with no control over timing.
- Privacy: uploading sends material off the machine, which rules out unreleased work and confidential dialogue.
- Residue: wet vocals keep their space, dense mixes lose low end, and drum transients round off.
- Reproducibility: the server-side model changes, so the same material processed months apart may differ; keep the stems from the run you used.
- Transcoding: uploading a lossy file means a second pass of loss, and sibilance and highs suffer first.
- Metering: when billing is by the minute, repeated attempts cost money, so decide which parts you need and process once.

## Cost, licence, alternatives

Questions to check: do you still own what you upload? Is uploaded material used to train models? How long are files kept, and can you delete them? Does commercial release need extra permission? May you redistribute the stems to third parties?

Pricing runs on minute packages or plans, differing in length, number of parts and download formats; regional availability is as stated on the official pages.

Alternatives: Demucs when you need offline, batch and reproducible runs; iZotope RX when separation and repair belong in one project; Adobe Enhance when you only need dialogue cleaned and no music split.

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["C4","E4","G4","A4","G4","E4","D4","C4"],"label":"The vocal left after separation","label_en":"The vocal left after separation","hint":"Hear whether the reverb tail comes along with the voice","hint_en":"Hear whether the reverb tail comes along with the voice"}
```
:::
