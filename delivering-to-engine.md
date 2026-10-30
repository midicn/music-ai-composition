---
id: delivering-to-engine
site: ai
cat: F
title: 交付到引擎
title_en: Delivering to the Engine
summary: 采样率、循环点、响度、命名，四项错一项就返工
summary_en: Sample rate, loop points, loudness and naming, one mistake means a redo
level: standard
tags: [交付, 采样率, 响度, 命名]
tags_en: [delivery, sample rate, loudness, naming]
alias: [引擎交付, 中间件导入, engine delivery]
order: 9
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:stem-mastering]]"
instances:
  - pdmx-002453 | 持续低音加高泛音，重采样先坏高频（C1）
  - pdmx-000801 | 低频在单声道里是否还在，交付前必查（C1）
  - pdmx-000450 | 大动态段落，响度统一后被压掉多少（C1）
  - oga-000283 | 短循环，检查循环点与文件信息（C1）
sources:
  - 音频交付到游戏引擎的格式与元数据要求，依中间件文档与工程通识核对，未抄原文
  - Audio delivery requirements for game engines, checked against middleware documentation and general practice, not copied
updated: 2026-10-30
---

::: zh
## 问题

音乐在 DAW 里听着没问题，进引擎就变样。采样率不对导致音高偏，循环点差几个采样每圈咔一声，响度没统一导致切场景时音量跳，命名混乱导致团队找不到文件。返工往往发生在最后一天。

## 原理

引擎按采样播放，任何非整数采样长度的循环都会有缝。重采样会改变高频，44.1 kHz 的素材进 48 kHz 工程要经过一次转换，镲和齿音最先受损。响度是另一条线，平台按 LUFS 统一，但循环素材如果逐条归一化，层与层的关系就没了。文件头里的速度、拍号、循环点，决定引擎怎么解释这段音频。同一段音频在两个平台上的时长可能差一两个采样，循环就会慢慢漂。

## 做法

交付前锁定采样率、位深、声道数，写进文档。循环点用整数采样，并在文件里标注 BPM 与拍号。响度按整组素材统一，不要逐条归一化。命名用固定字段顺序，项目、类别、名称、变体、版本。导入中间件后逐条试听，检查循环、淡入淡出和随机容器的行为。最后在目标设备上听一遍，手机扬声器和耳机差得很远。交付前留一天做检查，不要压到上线当天。

## 听什么

在维多尔的《第五管风琴交响曲》里听持续低音和高泛音，重采样时高频最先变。在德拉戈内蒂的低音提琴协奏曲里听低频在单声道下是否还在，在勃拉姆斯《德意志安魂曲》里听大动态段落被压掉多少，在 prehistoric-drum-loop 里听循环点是否干净。这些是导入后最先暴露的问题。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C2","G2","C3","E3","G3","C4","G4","C5"],"label":"持续低音与高泛音","label_en":"A held bass under high overtones","hint":"转换采样率后再听一次，高泛音是最先变的部分","hint_en":"Listen again after conversion; the high overtones change first"}
```
:::

::: en
## The problem

The music sounds fine in the DAW and changes once it reaches the engine. A wrong sample rate shifts the pitch, a loop point a few samples off clicks on every pass, loudness that was never unified jumps at a scene change, and chaotic naming means nobody can find the file. The rework usually lands on the last day.

## How it works

The engine plays by sample, so any loop whose length is not a whole number of samples has a seam. Resampling changes the top end, and 44.1 kHz material entering a 48 kHz project goes through one conversion that damages cymbals and sibilance first. Loudness is a separate line, normalized to LUFS by the platform, but normalizing every loop individually destroys the relationship between layers. Tempo, meter and loop points in the file header decide how the engine reads the audio.

## Practice

Lock sample rate, bit depth and channel count before delivery and write them into the documentation. Place loop points on whole samples and state BPM and meter in the file. Normalize loudness across the whole set rather than file by file. Name files with a fixed field order, project, category, name, variant, version. After importing into middleware, audition every file and check loops, fades and random container behaviour. Finally listen on the target device, since a phone speaker and headphones are far apart. Clear delivery notes save more time than explanations later. Leave a day for checks before the build.

## What to listen for

In Widor's Organ Symphony No. 5, a held bass under high overtones, where resampling shows first. In Dragonetti's double bass concerto, whether the low end survives in mono; in Brahms's A German Requiem, how much a wide dynamic is squashed by loudness matching; in prehistoric-drum-loop, whether the loop point is clean. These are the faults that appear first after import.

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C2","G2","C3","E3","G3","C4","G4","C5"],"label":"A held bass under high overtones","label_en":"A held bass under high overtones","hint":"Listen again after conversion; the high overtones change first","hint_en":"Listen again after conversion; the high overtones change first"}
```
:::
