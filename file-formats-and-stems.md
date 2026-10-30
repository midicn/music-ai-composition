---
id: file-formats-and-stems
site: ai
cat: H
title: 文件与分轨
title_en: Files and Stems
summary: 交付包的目标不是给全，而是让对方能接着做
summary_en: A delivery package exists so someone else can continue the work.
level: standard
tags: [分轨, 交付, 命名, 采样率]
tags_en: [stems, delivery, naming, sample rate]
alias: [文件交付, 分轨交付, stems delivery]
order: 4
links:
  - "[[glossary:stems]]"
  - "[[glossary:sample-rate]]"
  - "[[glossary:bit-depth]]"
instances:
  - musicnet-000067 | 贝多芬第十五弦乐四重奏，四声部正好对应四条分轨（C1）
  - mutopia-000497 | 贝多芬第五，多组总线与大量分轨的交付样本（C1）
  - groove-000000 | 单条鼓循环，用来检查单轨交付的循环点与尾音（C1）
  - pdmx-000153 | 二十六分钟长文件，分段与体积在交付时最容易被忽略（C1）
sources:
  - 分轨与工程交付的常见结构，依制作实务通识归纳，未抄原文
  - 采样率与位深的取舍，依数字音频公开规范核对，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

只交一个立体声混音，合作就到此为止，对方没法改贝斯，也没法替换一个音色。另一个极端是丢过去四十个未整理的文件，没有速度、没有起点、没有说明，接收的人要花半天重建工程。交付包的目标不是给全，而是让对方能在你的基础上继续工作。

## 交付包里放什么

一份完整混音，按要求留母带余量，如果加了限制器要注明。一份纯伴奏，一份清唱，按项目需要。按总线分的分轨，鼓、贝斯、和声乐器、主奏、人声、效果各一组，不要一件乐器一轨地散着给。生成工具能导出 MIDI 的，附上 MIDI，对方可以换音色。带混响和延迟的轨道，干声与湿声各一份。再加一份说明，写明速度、调性、采样率、位深、工程文件版本、用到的插件。

## 规格与命名

分轨用二十四位 WAV，采样率跟工程走，影视项目常用四十八千赫，纯音乐常用四十四点一千赫，不要把四十四点一的成品升到九十六冒充高清。所有分轨要能相加还原混音，做不到就写明增益补偿。命名统一为项目、曲名、版本、分轨名、速度、日期，用 ASCII，不用空格，版本号补零。同一项目的分轨名跨版本保持一致，对方的模板才不用重做。交付前用接收方的 DAW 打开一次，确认轨道数、起点与采样率一致，五分钟的检查能省掉对方一天的返工。

## 听什么

在贝多芬第十五弦乐四重奏里听四个声部如何分轨，四条就够，边界清楚。在贝多芬第五交响曲里听多组总线的分法。在放克鼓循环里听单轨交付时，循环点与尾音有没有交代。在二十六分钟的托卡塔里听长文件的分段与文件体积，命名和分段在这里最容易被忽略。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C4","E4","G4","C5"],"label":"分轨里的弦乐","label_en":"Strings inside the stems","hint":"每件乐器单独一轨，混音才有退路","hint_en":"One part per stem gives the mix somewhere to go back to"}
```
:::

::: en
## The problem

Delivering only a stereo mix ends the collaboration, because nobody can change the bass or swap a sound. The opposite extreme, forty unlabelled files with no tempo, start point or notes, forces the recipient to rebuild the session. The goal of a delivery package is not to send everything but to let someone continue working from where you stopped.

## What goes in

A full mix with the requested mastering headroom, and a note if a limiter is engaged. An instrumental and a vocal-only version where relevant. Stems grouped by bus, drums, bass, harmony, lead, vocals, effects, rather than one file per instrument. MIDI for generated parts if the tool exports it, so the recipient can change sounds. Dry and wet versions of anything with reverb or delay. A readme with tempo, key, sample rate, bit depth, session file version and plug-ins used.

## Specs and naming

Deliver stems as 24-bit WAV at the project rate, 48 kHz for most video work, 44.1 kHz for music-only, and never upsample a 44.1 kHz render to 96 kHz and call it high resolution. Stems must sum back to the mix, or the gain offsets must be documented. Name files as project, track, version, stem, tempo and date, in ASCII without spaces, with zero-padded version numbers. Keep stem names identical across versions so the recipient's template still works. Open the package once in the recipient's DAW and confirm track count, start point and sample rate; a five-minute check prevents a day of reconstruction.

## What to listen for

In the Beethoven String Quartet No. 15, how four voices map onto four clean stems. In the Beethoven Fifth, how many bus groups a large score needs. In the funk loop, whether a single-stem delivery explains its loop point and tail. In the twenty-six minute Toccata, how segmentation and file size become the easily forgotten part of delivery.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C4", "E4", "G4", "C5"], "label": "Strings inside the stems", "label_en": "Strings inside the stems", "hint": "每件乐器单独一轨，混音才有退路", "hint_en": "One part per stem gives the mix somewhere to go back to"}
```
:::
