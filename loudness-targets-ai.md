---
id: loudness-targets-ai
site: ai
cat: D
title: 响度目标
title_en: Loudness Targets
summary: 先对齐响度再比较，平台标准与真峰值决定你能留多少动态
summary_en: Match levels before comparing, and let platform targets and true peak decide how much dynamics you can keep.
level: standard
tags: [响度, 真峰值, 平台标准, 归一化]
tags_en: [loudness, true peak, platform targets, normalization]
alias: [响度标准, LUFS, loudness targets]
order: 4
links:
  - "[[glossary:lufs]]"
  - "[[glossary:true-peak]]"
  - "[[glossary:loudness-normalization]]"
instances:
  - atepp-001283 | 肖邦夜曲 Op.37 No.2，整体偏窄，适合检查目标响度下的呼吸（C1）
  - groove-000000 | 138 BPM 放克鼓组，电平对齐后比瞬态与底鼓重量（C1）
  - openscore-000270 | 马勒《我有一把灼热的刀》，爆发段最容易顶到真峰值（C1）
sources:
  - 流媒体与播送的响度目标——依据来自公开标准与平台文档。
  - Streaming and broadcast loudness targets, summarized from public standards and platform documentation
updated: 2026-10-30
---

::: zh
## 要解决的事

两个版本一前一后播放，响的那个总显得更好，低频更足，人声更前。这不是音质差异，是响度偏差。AI 生成的成品常常直接给到很响，混音时又容易跟着这个印象走，越推越高，动态越剩越少。到了平台，响度被统一，剩下的只有被压扁的痕迹。

## 运行方式

流媒体平台按整体响度做归一化。Spotify 与 YouTube 大致把目标定在 -14 LUFS，Apple Music 大致 -16 LUFS，播送标准 EBU R128 是 -23 LUFS。超过目标的作品会被整体衰减，不会更响，只会更平。真峰值上限通常留 -1 dBTP，给编码留余量。整体响度是整首的平均值，短时响度才反映副歌有多满，两者要一起看。单曲与专辑也要分开看，专辑内部的相对关系比绝对值更重要。

## 具体做法

混音阶段把整体压在 -18 到 -20 LUFS，留 4 到 6 dB 余量，总线上不要挂限幅器。母带时先定交付平台，按目标响度做，不要按「越响越好」做。限幅器开 4 倍以上过采样，真峰值控制在 -1 dBTP。比较版本时把两者电平对齐到 0.1 dB，再听低频与瞬态。如果对齐后原版更好，说明响度没有换来任何东西，回混音找动态。短时响度与整体响度差得太多，说明段落对比大，别用限幅器把它抹平。播送或影视的版本单独做，不要拿流媒体母带去顶，那里需要更大的余量。交付前把整张专辑过一遍，确认曲目之间的响度关系。

## 耳朵要抓的点

肖邦夜曲 Op.37 No.2 整体偏窄，适合检查目标响度下是否还有呼吸。138 BPM 放克鼓组用来对齐电平后比瞬态，底鼓的重量在响度竞赛里最先丢失。马勒《我有一把灼热的刀》的爆发段最容易顶到真峰值，听限制器是否把字头削平。三处都先降到同一响度再判断。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4","C4","G3"],"label":"同一段在不同响度下","label_en":"One phrase at two levels","hint":"把音量调到一样再比音色，响的会先骗过耳朵","hint_en":"Match the level before comparing tone; louder fools the ear first"}
```
:::

::: en
## The problem to solve

Play two versions back to back and the louder one always seems better, with more low end and a more forward vocal. That is not a quality difference but a level difference. AI output often arrives loud, and mixing tends to follow that impression upward until little dynamics remain. On a platform the loudness is normalized away, leaving only the flattening.

## How it runs

Streaming services normalize by integrated loudness. Spotify and YouTube target roughly -14 LUFS, Apple Music roughly -16 LUFS, and the broadcast standard EBU R128 is -23 LUFS. A track above the target is turned down as a whole, so it is not louder, only flatter. True peak is usually capped at -1 dBTP to leave room for encoding. Integrated loudness averages the whole track, while short-term loudness shows how full the chorus really is, so read both. Single and album context also matter, because relative level inside an album counts for more than the absolute number.

## In practice

Mix at -18 to -20 LUFS with 4 to 6 dB of headroom and no limiter on the bus. Decide the delivery platform before mastering, then work to its target rather than to loudness for its own sake. Run the limiter with at least 4x oversampling and keep true peak at -1 dBTP. When comparing versions, match levels within 0.1 dB, then listen for low end and transients. If the original wins after matching, the loudness bought nothing, so go back to the mix for dynamics. When short-term and integrated loudness diverge widely, the section contrast is large, and the limiter should not be allowed to erase it. Make broadcast or film versions separately instead of sending a streaming master into a slot that needs more headroom.

## What the ear catches

Chopin's Nocturne Op. 37 No. 2 is narrow throughout, which makes it a good check for whether breathing survives at the target. The 138 BPM funk groove tests transients after level matching, and kick weight is the first thing lost in a loudness push. In Mahler's Ich hab' ein glühend Messer, the outburst is where true peak is exceeded first, so hear whether the limiter shaves the attacks. Bring all three to the same level before judging.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4","C4","G3"],"label":"One phrase at two levels","label_en":"One phrase at two levels","hint":"Match the level before comparing tone; louder fools the ear first","hint_en":"Match the level before comparing tone; louder fools the ear first"}
```
:::
