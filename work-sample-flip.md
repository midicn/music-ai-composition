---
id: work-sample-flip
site: ai
cat: K
title: 采样再创作
title_en: A Sample Flip
summary: 先查许可再切片，采样包与老唱片是两套规则
summary_en: Clear the sample before chopping; packs and old records follow different rules.
level: standard
tags: [采样, 切片, 授权, 编曲]
tags_en: [sampling, chopping, clearance, beatmaking]
alias: [采样再创作, 采样翻转, sample flip, 切片]
order: 8
tool_kind: guide
tool_vendor: 本站
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [采样制作, 编曲, 授权确认]
tool_verified: 2026-10-30
links:
  - "[[glossary:rhythm]]"
  - "[[glossary:tempo]]"
  - "[[glossary:stems]]"
instances:
  - groove-000000 | 138 BPM 放克鼓组，军鼓落点决定切片位置（C1）
  - groove-000005 | 87 BPM 嘻哈鼓组，hi-hat 的 swing 最难生成（C1）
  - oga-000287 | 电子循环靠增减元素维持律动，听层间关系（C1）
sources:
  - 采样包许可与唱片清权的差别，依采样与发行公开规则核对，未抄原文
  - 切片与变调的做法，依采样器与鼓组编配通识归纳
updated: 2026-10-30
---

::: zh
## 需求长什么样

用一段采样做一首新 beat，采样来自免版税采样包，或来自一张老唱片。两种来源的授权完全不同：采样包允许你使用，通常不允许你把原始采样再分发；老唱片要同时清词曲与录音。客户要的是可发行版本，不是 loop 练习。交付里要能看出这段采样从哪来。

## 工具组合

切片与编曲在 Ableton Live 或 FL Studio 里做，按瞬态切、映射到键盘。清理用 iZotope RX，去嗡声与噪声。Demucs 可把老唱片分出人声或鼓，但它不解决授权。补充层用 Serum 或 Vital，需要氛围时用 Suno 或 Udio 生成一段。母带用 Ozone。

## 步骤

先查采样来源与许可条款，写下包名、作者与购买凭证。选一到两小节最有辨识度的片段，按军鼓或元音切点。把切片映射到键盘，重排成新节奏。变速时用切片模式，避免整段拉长变形。加鼓、贝斯与和声层。编成完整段落，留出 intro 与 breakdown。混音后母带。

## 验收标准

采样来源与许可写在交付文档里。可识别的老唱片样本已完成清权，或已替换。原始采样没有以单独文件形式再分发。切片点无咔哒，变调后共振峰自然。工程速度与切片速度一致，切片触发延迟低于 10 毫秒。成品 -14 LUFS，真峰值不高于 -1 dBTP。分轨与工程文件齐全。

## 常见返工原因

从流媒体抓的音频直接切，没有清权。采样包禁止再分发，却把原始 wav 一起交付。切片点落在噪声上，每次触发都带爆音。大幅变调后音色像玩具。鼓组盖住采样，辨识度没了。客户要求换采样，工程却已经混完。没记录来源，发行时无法证明授权。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":90,"label":"十六分切片的骨架","label_en":"A skeleton built from sixteenths","hint":"听每一刀落在哪，切点决定新节奏","hint_en":"Hear where each cut lands; the cut points write the new groove"}
```
:::

::: en
## What the brief looks like

A new beat is built from a sample, and the sample may come from a royalty-free pack or from an old record. The two clear differently: a pack lets you use the sound but usually forbids redistributing the raw sample, while an old record needs both the composition and the master cleared. The client wants a release-ready track, not a loop exercise, and the delivery has to show where the sample came from.

## Tool combination

Chop and arrange in Ableton Live or FL Studio, cutting on transients and mapping slices to keys. Clean with iZotope RX to remove hum and noise. Demucs can pull a vocal or drum layer from an old record, but it settles no rights. Add layers with Serum or Vital, and use Suno or Udio for an atmosphere if needed. Master with Ozone.

## Steps

Check the sample's source and terms first, and record the pack name, author and purchase receipt. Choose one or two bars with the strongest identity and cut on snares or vowels. Map the slices across the keyboard and resequence them into a new rhythm. Use slice mode when changing tempo so the whole phrase is not stretched. Add drums, bass and harmony. Arrange full sections with an intro and a breakdown. Mix, then master.

## Acceptance criteria

Source and licence are written into the delivery document. Any recognisable record sample is cleared or replaced. The raw sample is never redistributed as a standalone file. Slices trigger without clicks and pitch shifts keep a natural formant. Project tempo matches the slice playback and slice triggering stays under 10 ms. The master sits at -14 LUFS with true peak no higher than -1 dBTP. Stems and the session file are included.

## Common rework causes

Audio ripped from a streaming service is chopped with no clearance. A pack forbids redistribution and the raw wav ships with the project. Cuts land on noise and every trigger pops. Heavy pitch shifting turns the sample into a toy. Drums bury the sample and its identity disappears. The client asks for a different sample after the mix is finished. No source is recorded, so the licence cannot be proven at release.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":90,"label":"A skeleton built from sixteenths","label_en":"A skeleton built from sixteenths","hint":"Hear where each cut lands; the cut points write the new groove","hint_en":"Hear where each cut lands; the cut points write the new groove"}
```
:::
