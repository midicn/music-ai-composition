---
id: "reference-matching"
site: "ai"
cat: "D"
title: "参考曲匹配"
title_en: "Matching a Reference"
summary: "参考曲是尺子不是模板，先对齐电平，每次只比一个维度"
summary_en: "A reference is a ruler, not a template, so match the level and compare one dimension at a time."
level: "standard"
tags: ["参考曲", "电平匹配", "音色平衡", "比较方法"]
tags_en: ["reference track", "level matching", "tonal balance", "comparison"]
alias: ["参考曲", "对标", "reference matching"]
order: 9
links: ["[[glossary:reference-track]]", "[[glossary:lufs]]", "[[glossary:eq]]"]
instances: []
sources: ["https://www.izotope.com/en/learn/13-tips-for-using-references-while-mixing", "https://www.itu.int/rec/R-REC-BS.1770-5-202311-I/"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "参考匹配需要同响度对照相同段落，并把频谱、动态和空间分别比较；无关曲目直接播放会混入电平与编配差异，不能证明匹配效果。"
---

::: zh
## 难点在哪

自己的 AI 成品和商业参考放在一起，总觉得薄、散、不够亮。于是照着参考提高频、加宽、压响，越做越偏。问题往往不在处理，在比较方法。没有对齐电平，没有限定比较的维度，参考就从尺子变成了诱惑。

## 背后的机制

响度会偏置判断。响 3 dB 的版本，低频显得更足，高频显得更亮，人耳几乎无法抵抗。参考曲还带着母带处理、编曲密度和录音空间，这些不一定适合你的素材。参考曲的编曲密度如果和你的差太远，比较低频量就没有意义，先换一首更接近的。有效的比较只在一个维度上进行，低频量、中频密度、高频空气感或混响长度，一次一个，且两者电平相同。

## 怎么调整

选一到两首同类型、编曲密度接近的成品。用响度表把参考降到与你相同的整体响度，误差控制在 0.1 dB 以内。切换点选在副歌或鼓组进入处，每次只听十秒，只判断一件事。发现差异先回编曲找原因，参考的低频少，可能是你的贝斯多了一层。频谱只做辅助核对，不要按曲线硬调。把结论写成一句话，比如低频多 2 dB、人声少一点空气感，再回工程找对应的一个参数。明确不抄的部分，母带的响度、失真量和混响长度都属于参考曲自己的选择，搬过来只会让你的素材更假。
:::

::: en
## Where it gets hard

Put your AI track next to a commercial reference and it feels thin, scattered, not bright enough. So you raise the highs, widen the image and push the limiter, drifting further from the goal. The fault is usually not the processing but the method. Without matched levels and a single dimension to compare, the reference stops being a ruler and becomes a temptation.

## The mechanism

Loudness biases judgement. A version 3 dB louder seems to have more low end and more brightness, and the ear rarely resists. The reference also carries its own mastering, arrangement density and recording space, none of which necessarily suits your material. If the reference is much denser or sparser than your track, comparing low-end weight means nothing, so choose a closer one first. A useful comparison isolates one dimension at a time, low-end weight, midrange density, high-frequency air or reverb length, with both signals at the same level.

## How to adjust

Choose one or two finished tracks of the same genre and similar density. Use a loudness meter to bring the reference down to your integrated level within 0.1 dB. Switch at the chorus or where the drums enter, listen for ten seconds, and judge one thing. When you hear a difference, look for the cause in the arrangement first; less low end in the reference may mean your bass has an extra layer. Use a spectrum display only as a sanity check, never as a curve to match. Write the finding as one sentence, for example 2 dB more low end or less air on the vocal, then find the single parameter that matches. Decide what not to copy, since the reference's loudness, distortion and reverb length are its own choices, and importing them only makes your material less convincing.
:::

