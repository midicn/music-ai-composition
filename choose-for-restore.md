---
id: choose-for-restore
site: ai
cat: A
title: 修复选型
title_en: Choosing Tools for Restoration
summary: 修复的上限是原始素材，不是软件；先定修到什么程度，再选工具。
summary_en: Restoration stops at the source material, not the software; decide how far to go before choosing a tool.
level: standard
tags: [选型, 修复, 降噪, 老录音]
tags_en: [selection, restoration, noise reduction, archival]
alias: [修复选型, 降噪工具, restoration]
order: 16
links:
  - "[[glossary:headroom]]"
  - "[[glossary:monitoring]]"
  - "[[glossary:mastering]]"
tool_kind: guide
tool_vendor: 本站
tool_form: 网页
tool_platforms: [浏览器]
tool_price: 免费
tool_jobs: [选型, 修复]
tool_verified: 2026-10-30
instances:
  - cyberhymnal-000001 | 桑基《九十九只羊》，十九世纪福音赞美诗，窄带老录音的典型素材（C1）；这是该用途常见产出的参照，不是本站工具的演示
  - pdmx-002646 | 《纽约的人行道》，十九世纪末的流行歌曲，方整短小，修完容易听出处理痕迹（C1）；这是该用途常见产出的参照，不是本站工具的演示
  - giantmidi-004939 | 格什温《斯瓦尼》，早期流行歌曲，人声与乐队争频段的参照（C1）；这是该用途常见产出的参照，不是本站工具的演示
  - cyberhymnal-001734 | 勃拉姆斯《伯利恒摇篮曲》，弱奏管风琴，底噪与动态的边界（C1）；这是该用途常见产出的参照，不是本站工具的演示
sources:
  - 谱修复、降噪与语音增强的公开技术说明，2026-10-30 核对，未抄原文
  - 档案保存与再发行的通行做法，依通识核对，未据以下法律结论
updated: 2026-10-30
---

::: zh
## 它能完成什么

三种活：把家庭卡带录音修到能送人；把有空调声的采访修到能上播客；把老唱片修到能发数字版。前两个要的是听得清，后一个还要说得出改了什么，因此交付物不只是一条音频，还有一份处理记录。

## 它怎么工作

四条路线，按控制力、交付形态、学习成本、权利风险分。

分离再分别修（Demucs、LALAL.AI 加逐轨处理）：控制力中等，能单独修人声，代价是串音与水声。交付是分轨或重混。学习成本中等。风险在于分离不改变原录音的权利状态，二次发行仍要授权。

一体化修复套件（iZotope RX 这类）：控制力最高，去嗡、去噪、去爆音与谱修复都能局部画出来。交付是整轨修复版，加一份处理链说明。学习成本高，难在判断修多少。风险低，本地处理，素材不外传。

云端一键增强（Adobe Enhance 这类在线服务）：控制力低，参数少，常见结果是高频被补出来、人声发塑料味。交付是增强后的单声道或立体声。学习成本最低。风险中高，素材上传、条款允许的用途与再分发都要看。

转 MIDI 重演或重合成：控制力中等，交付其实是新录音。学习成本中等。风险中等，这已经不是修复而是重制，署名与权利另算。

## 边界与坑

第一，补出来的高频不是录到的信息，修到「像新的」往往就失真了。第二，链式处理会累积：降噪叠三层，喷气声与齿音会一起被削掉。第三，档案与发行必须分开走，档案留原始文件与处理链说明，发行版才可以修得激进。

不要在一次处理里连开三个降噪。不要把增强后的文件当档案母版。不要在没获授权时用分离轨做新发行。不要把七十八转唱片的窄带补成宽频，然后说这是原始音质。

## 替代与搭配

只要人声清楚、不保留音乐，用 Demucs 或 LALAL.AI 先分离再修；要整段都动，用 iZotope RX 这类套件；素材只有一两条、又不想学软件，Adobe Enhance 能应付一次，别把它当流程。最常见的搭配是：分离做粗修，套件做精修，母带环节只碰响度与真峰值。

## 上手路径

先学三件事：留一份未处理的原件、每一步只做一件事、每次处理前后做 A/B。然后读本站的修复伪影、分轨分离工具、响度目标三篇。

```audiolab
{"type":"instrument","gm":"Reed Organ","synth":"reed","phrase":["G3","B3","D4","G4","F4","D4","B3","G3"],"label":"老录音里的管风琴","label_en":"An organ from an old recording","hint":"先听底噪，再决定要修掉多少","hint_en":"Hear the noise floor first, then decide how much to remove"}
```
:::

::: en
## What it lets you finish

Three jobs: a family cassette repaired enough to give away; an interview with air-conditioner noise repaired enough for a podcast; an old record repaired enough for digital release. The first two need audibility, the third also needs an account of what changed, so the deliverable is not only audio but a processing record.

## How it works

Four routes, judged on control, deliverable, learning cost and rights exposure.

Separate first, then treat each stem, using Demucs or LALAL.AI plus per-stem work: control is medium, and you can fix the voice alone at the cost of bleed and watery artefacts. The deliverable is stems or a remix. Learning cost is medium. The risk is that separation does not change the rights status of the recording, so redistribution still needs clearance.

A restoration suite such as iZotope RX gives the most control: hum, noise, clicks and spectral repair can all be painted in locally. The deliverable is a repaired master with a written processing chain. Learning cost is high, because the hard part is deciding how much to remove. Risk is low, since processing stays local.

One-click cloud enhancement, as in Adobe Enhance, gives the least control: few parameters, and the usual result is invented high end and a plastic vocal. The deliverable is an enhanced mono or stereo file. Learning cost is lowest. Risk is medium-high, because material is uploaded and the terms govern permitted use and redistribution.

Transcribe to MIDI and replay, or resynthesize: control is medium, but the deliverable is really a new recording. Learning cost is medium. Risk is moderate, since this is no longer restoration but re-creation, with credit and rights counted separately.

## Limits and traps

First, invented high frequencies are not recorded information, and repairing until it sounds new usually means it now sounds false. Second, processing accumulates: three noise reducers in a row take the plosives and sibilance with them. Third, archive and release must part ways, with the original and its processing notes kept, and only the release version pushed hard.

Do not stack three noise reducers in one pass. Do not file an enhanced file as the archival master. Do not release separated stems without clearance. Do not widen a narrow-band disc transfer and then call it the original sound.

## Alternatives and pairings

If the voice must be clear and the music can go, separate with Demucs or LALAL.AI and treat the vocal; if the whole tape needs work, use a suite such as iZotope RX; for one or two files and no appetite for learning software, Adobe Enhance handles a single job but is not a workflow. The usual pairing: separation for rough repair, a suite for detail, mastering only for loudness and true peak.

## First three things to learn

Learn to keep an untouched original, to change one thing per pass, and to A/B before and after every step. Then read this site's pages on fixing artifacts, stem separation tools and loudness targets.

```audiolab
{"type":"instrument","gm":"Reed Organ","synth":"reed","phrase":["G3","B3","D4","G4","F4","D4","B3","G3"],"label":"An organ from an old recording","label_en":"An organ from an old recording","hint":"Hear the noise floor first, then decide how much to remove","hint_en":"Hear the noise floor first, then decide how much to remove"}
```
:::
