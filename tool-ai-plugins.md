---
id: tool-ai-plugins
site: ai
cat: J
title: AI 插件（分离/修音/母带）
title_en: AI Plug-ins for Separation, Tuning and Mastering
summary: 把分离、修音与母带助手装进宿主，换来速度，也换来格式与授权约束。
summary_en: Separation, tuning and mastering assistants inside the host buy speed, at the price of format and licence constraints.
level: standard
tags: [插件, 分离, 修音, 母带]
tags_en: [plug-in, separation, tuning, mastering]
alias: [AI 插件, 智能插件]
order: 2
links:
  - "[[glossary:plugin]]"
  - "[[glossary:stems]]"
  - "[[glossary:latency]]"
tool_kind: plugin
tool_vendor: 插件厂商
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [混音, 母带, 人声制作]
tool_verified: 2026-10-30
instances:
  - openscore-000443 | 弗朗茨艺术歌曲，人声与钢琴分离后是否还能各自修音（C1）
  - giantmidi-002278 | 古利特小提琴奏鸣曲，旋律线的音准与揉弦最考验修音插件（C1）
  - pdmx-000183 | 莫扎特安魂曲，声部密集，分离与总线处理最容易留下痕迹（C1）
  - groove-001115 | 112 BPM 摇滚鼓组，瞬态是否被母带助手压平一听便知（C1）
sources:
  - 主流 AI 音频插件公开文档所列功能、格式与授权方式（2026-10-30 复核）。
  - 分离、修音与限幅的常见伪影，参考混音实践惯例。
updated: 2026-10-30
---

::: zh
## 能替你做完什么

它能在工程里把一条混好的立体声拆成人声、鼓、贝斯与其他，让你单独处理其中一层。能把走音的主唱或独奏修到可发布，能压掉底噪、口水声与房间回声。能在总线上挂一版母带助手，快速得到响度与音色都接近成品的版本。也能给对白或采样做清理，让素材先变得可用。这些工作过去要开独立软件、导出再导入，现在留在一条插件链里。

## 它怎么工作

这类插件多半在本地跑一个神经网络：分离用掩码估计每个频段属于哪件乐器，再重建波形；修音先跟踪基频，再按目标音高与颤音曲线重合成；母带助手则分析素材的频谱与动态，套入匹配的均衡、压缩与限幅。它们通常提供很少的参数，把判断藏在模型里，并把处理写成可旁通的插件状态。实时监听与离线渲染是两条路径，前者受缓冲区限制，后者可以慢慢算。

## 哪里会坑你

第一是格式与宿主。插件分 VST3、AU、AAX 等，买错格式就打不开；宿主大版本升级也可能让旧插件失效。第二是授权。按机器或加密狗激活的插件，换电脑、离线演出、协作方打开工程都要先解决授权，工程里的设置才会响。第三是延迟。实时分离与修音会引入监听延迟，录音时不能挂在监听链上；离线渲染又不适合边弹边改。第四是伪影。密集混音分离后常带金属味与串音，修音过度会让颤音变平、齿音发硬，母带助手则容易把瞬态压成一块。第五是它不判断。哪一层该留、哪个音该修、压多少算刚好，仍要你的耳朵和上下文。

## 换成什么

要更细的频谱编辑，用独立修复软件，它的笔刷与频谱视图仍是插件比不了的。只在交付前要一版响度，用云端母带服务更省事，但要接受上传与按量计费。插件最适合的位置是工程内反复试：分离出参考轨、修一版人声、给总线做 A/B。搭配上，保留未处理的原始轨与插件预设，别让工程只剩下处理后的声音。

## 先学三件事

先学三件事：确认插件格式与授权方式、用旁通做 A/B、把处理结果渲染一份并检查相位。然后读这里的分离工具、人声修音与响度目标三篇，再决定哪些环节常驻插件、哪些交给独立软件。

```audiolab
{"type":"instrument","gm":41,"phrase":["G4","D5","A5"],"label":"独奏音准","label_en":"Solo intonation","hint":"修音后听颤音是否还在，而不是只听话准","hint_en":"After tuning, listen for vibrato, not only pitch"}
```
:::

::: en
## What it finishes for you

It can split a mixed stereo file into vocals, drums, bass and other so one layer can be treated alone. It can bring a sharp lead vocal or solo instrument close to release quality, and suppress noise floor, mouth clicks and room ring. It can place a mastering assistant on the bus and return a near-finished version. It can also clean dialogue or a sample until the material is usable. The work stays in one chain.

## How it works

Most of these plug-ins run a neural network locally: separation estimates which instrument owns each time-frequency region and rebuilds the waveform; tuning tracks the fundamental, then resynthesises toward a target pitch and vibrato curve; a mastering assistant analyses spectrum and dynamics, then applies matched EQ, compression and limiting. They expose few parameters, hide the judgement in the model, and store processing as bypassable plug-in state. Real-time and offline rendering are different paths: the first is buffer-bound, the second can take its time.

## Where it bites

First, format and host. Plug-ins ship as VST3, AU, AAX and others, so the wrong purchase will not open, and a host upgrade can break an older build. Second, authorisation. Machine- or dongle-locked licences must be resolved before a new computer or an offline show will make sound. Third, latency. Real-time separation and tuning add monitoring delay, so they cannot sit on the record chain. Fourth, artefacts. Dense mixes separate with metallic residue and bleed, over-tuning flattens vibrato and hardens sibilance, and a mastering assistant can crush transients into a slab. Fifth, it cannot judge which layer to keep, which note to fix or how much is enough; that still needs your ears and context.

## What to swap in

For finer spectral work, use a dedicated repair application whose brush and spectrogram still beat any plug-in. If you only need a release version, a cloud mastering service is simpler, provided you accept uploads and per-use billing. The plug-in's best role is iteration inside the project: print a reference stem, tune one vocal, A/B the bus. Keep the untreated original and preset so the session is not left with processed sound only.

## First three things

Learn three things first: the plug-in format and how it is authorised, how to bypass it for an A/B, and how to print a result and check phase. Then read the site's pages on separation tools, vocal tuning and loudness targets before deciding what stays on the chain.

```audiolab
{"type":"instrument","gm":41,"phrase":["G4","D5","A5"],"label":"Solo intonation","label_en":"Solo intonation","hint":"After tuning, listen for vibrato, not only pitch","hint_en":"After tuning, listen for vibrato, not only pitch"}
```
:::
