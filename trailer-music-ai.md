---
id: "trailer-music-ai"
site: "ai"
cat: "F"
title: "预告片音乐"
title_en: "Trailer Music with AI"
summary: "预告片靠留白和落点，生成素材要按 hit point 重剪"
summary_en: "Trailers run on silence and hit points; generated cues must be re-cut to them"
level: "standard"
tags: ["预告片", "结构", "重音落点", "剪辑"]
tags_en: ["trailers", "structure", "hit points", "editing"]
alias: ["预告片配乐", "电影预告", "trailer music"]
order: 4
links: ["[[glossary:sync-license]]", "[[glossary:cue]]"]
instances: []
sources: ["https://helpx.adobe.com/premiere/desktop/add-audio-effects/apply-audio-effects/remix-in-premiere.html", "https://tech.ebu.ch/docs/r/r128s1.pdf"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "预告片音乐的重点是实际镜头切点、版本长度和交付响度，三段结构并非普遍规则；没有画面的音乐播放不能证明命中点或短版交付合格。"
---

::: zh
## 症状与位置

预告片音乐有固定形状，三十秒到两分半，通常三段，第一段立设定，第二段堆压力，第三段爆发。中间要卡十几个 hit point，对白、logo、片名各有落点。让 AI 写"史诗预告片音乐"，得到的常是一段一直在高潮的音频，没有留白，也没有能和画面对上的点。

## 机制上的解释

预告片的力量来自对比，安静段越长，爆发越响。hit point 不是随便的重音，它要落在画面切点上，通常提前一到两帧。生成模型按音乐逻辑安排强弱，不按剪辑点，所以即使气势对了，落点也全错。它还会把结尾做成渐弱，而预告片要的是硬收或者直接切黑。

## 怎么修

先拿到锁定的画面和 hit point 表，把时间码写进工程。用 AI 生成素材，拆成低频、打击、铜管、氛围四类，按段落重排，而不是整段使用。riser 单独生成或合成，长度按镜头调整。drop 前的半秒留空，比加一层镲更有效。片名出现时用一个干净的终止，不要拖着混响。每版都对着画面看一遍，不要只听音频，很多问题只有看画面才发现。预告片里一半的冲击来自音效，音乐负责骨架和情绪线。
:::

::: en
## Symptom and location

Trailer music has a fixed shape, thirty seconds to two and a half minutes, usually in three acts, the first setting the premise, the second stacking pressure, the third breaking open. A dozen hit points sit inside it, for dialogue, logo and title. Ask AI for "epic trailer music" and you often get a cue that is already at full climax, with no silence and no points that line up with picture.

## The mechanism explains it

A trailer's force comes from contrast, and the longer the quiet section, the louder the drop feels. A hit point is not any accent; it lands on a cut, usually one or two frames early. Generation models place loud and soft by musical logic rather than edit points, so the shape can be right while every landing is wrong. They also end on a fade, where a trailer needs a hard stop or a cut to black.

## How to fix it

Get the locked picture and the hit point list first, and put the timecode into the session. Generate material, then split it into low end, percussion, brass and atmosphere, and re-cut those elements by section instead of using the cue whole. Make risers separately and size them to the shot. Half a second of silence before the drop does more than another cymbal layer. End the title on a clean cadence without a long reverb tail. Watch every version against picture; some problems only appear on screen. Half the impact comes from sound design, with the music supplying structure and the emotional line.
:::

