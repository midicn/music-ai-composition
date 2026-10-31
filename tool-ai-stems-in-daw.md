---
id: tool-ai-stems-in-daw
site: ai
cat: J
title: DAW 内分轨
title_en: Stem Separation Inside the DAW
summary: 在工程里把成品拆成可单独处理的轨，先问分离痕迹会不会毁掉这一版。
summary_en: Splitting a finished mix into separately treatable tracks inside the session starts with whether the artefacts ruin this version.
level: standard
tags: [分轨, 分离, 混音, 采样]
tags_en: [stems, separation, mixing, sampling]
alias: [工程内分轨, 实时分离]
order: 4
links:
  - "[[glossary:stems]]"
  - "[[glossary:phase]]"
  - "[[glossary:mixdown]]"
tool_kind: plugin
tool_vendor: 分轨插件厂商
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [混音, 剪辑, 声音设计]
tool_verified: 2026-10-30
instances:
  - openscore-000443 | 艺术歌曲的人声与钢琴，两件乐器分离后是否还像同一间房（C1）；这是该工具常见产出的参照，不是该工具的演示
  - musicnet-000288 | 莫扎特钢琴三重奏，三件乐器是检验分轨层次的合适参照（C1）；这是该工具常见产出的参照，不是该工具的演示
  - pdmx-000183 | 莫扎特安魂曲，合唱与乐队叠在一起，分离后最容易剩下糊边（C1）；这是该工具常见产出的参照，不是该工具的演示
  - groove-001115 | 112 BPM 摇滚鼓组，拆鼓时瞬态与镲片残响是否保住（C1）；这是该工具常见产出的参照，不是该工具的演示
sources:
  - 主流 DAW 内分轨功能的公开说明与格式限制，参考2026-10-30 复核。
  - 掩码分离的串音与相位问题；混音实践惯例是主要依据。
updated: 2026-10-30
---

::: zh
## 能替你做完什么

它能在工程里把一首成品拆成人声、鼓、贝斯与其他，让你给人声加混响、给鼓换采样、把贝斯抽掉做伴奏版。能把一段参考曲里的鼓 loop 单独取出来，做节奏替换或采样。能给练习者做去人声的伴奏轨，也能给混音师做一版可 solo 的参考分层。分离结果直接落在时间线上，和原曲对齐，省去导出再导入。

## 它怎么工作

分离模型把频谱切成时频块，估计每一块属于哪件乐器，再按掩码重建各轨波形。常见是四轨模型，也有把人声再拆主唱与和声、把鼓再拆底鼓军鼓踩镲的细分模型。重建时原曲的相位关系被打破，各轨相加不一定还原原曲，所以工程里通常保留一条原曲做对照。运算多在本地离线完成，长文件要等，实时监听则要靠低延迟模型或硬件加速。

## 哪里会坑你

第一是伪影。分离出的人声常带金属味与齿音毛刺，鼓的镲片会变成沙沙的噪声，贝斯低频会与底鼓互相偷能量。第二是串音。原曲里本来就叠在一起的声部，模型只能猜，solo 时听得到别的乐器。第三是相位与单声道。各轨重新相加可能出现梳状滤波，在单声道里尤其明显，做伴奏版要在手机喇叭上再听。第四是版权。拿别人的成品做分轨，处理完仍是别人的录音，采样使用要清权，不能因为拆开了就当成新素材。第五是它不等于多轨。真正的多轨能改演奏，分离只能改处理；两者在混音里的可用程度差很远。

## 换成什么

要更干净的结果，用独立分离服务或修复软件，它们通常给更多轨数与更细的笔刷，代价是往返。手里有原始多轨时，永远优先用多轨，分离只做参考或采样。搭配上，把分离轨当成音色层而不是主轨：和原曲叠一点，或只取其中一段，伪影会被掩盖。

## 先学三件事

先学三件事：用原曲做 A/B、检查单声道与相位、确认素材的授权边界。随后读这里的分轨级编辑、分轨分离工具与混 AI 分轨三篇，再决定哪些轨值得留下。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":112,"label":"拆出的鼓","label_en":"Separated drums","hint":"solo 鼓轨，听镲片是否变成噪声","hint_en":"Solo the drum stem and listen for noisy cymbals"}
```
:::

::: en
## What it finishes for you

Inside the session, it can split a finished song into vocals, drums, bass and other, so you can add reverb to the voice, replace the drums or drop the bass for a backing version. It can pull a drum loop out of a reference track for a rhythm swap or a sample. It can make a minus-one for practice and a soloable layered reference for a mix engineer. Results land on the timeline aligned with the original, with no export and re-import.

## How it works

The model cuts the spectrum into time-frequency blocks, estimates which instrument owns each block, then rebuilds each stem through a mask. Four-stem models are common; finer models split lead and backing vocals or kick, snare and cymbals. Reconstruction breaks the original phase relationships, so the stems do not necessarily sum back to the source, and a reference copy usually stays in the project. Processing is mostly local and offline: long files take time, and real-time monitoring needs low latency or hardware acceleration.

## Where it bites

First, artefacts. Separated vocals carry metallic residue and harsh sibilance, cymbals turn into hiss, and bass loses energy to the kick or steals it back. Second, bleed. Parts already overlapping in the source can only be guessed at, and solo reveals other instruments. Third, phase and mono. Recombined stems can comb-filter, especially in mono, so check a backing track on a phone speaker. Fourth, rights. Separating someone else's release still leaves it their recording; sampling needs clearance and does not become new material because it was split. Fifth, it is not multitrack. Real tracks allow performance changes; separation only allows processing, and the two are far from equally useful in a mix.

## What to swap in

For cleaner results, use a standalone separation service, which usually offers more stems and finer brushes at the cost of a round trip. When the original multitrack exists, always prefer it; separation is for reference or sampling. Pair the output as a layer, not a lead: blend a little with the source, or use one section only, and the artefacts hide.

## First three things

Learn three things first: A/B against the original, check mono and phase, and confirm what the source material allows. Then read the site's pages on stem-level editing, separation tools and mixing AI stems before deciding which stems are worth keeping.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":112,"label":"Separated drums","label_en":"Separated drums","hint":"Solo the drum stem and listen for noisy cymbals","hint_en":"Solo the drum stem and listen for noisy cymbals"}
```
:::
