---
id: dynamic-range-decisions
site: ai
cat: D
title: 动态范围取舍
title_en: Choosing a Dynamic Range
summary: AI 素材天生偏平，留多少起伏是审美决定，不是参数默认
summary_en: AI material is born flat, and how much contrast to keep is an aesthetic call rather than a setting.
level: standard
tags: [动态范围, 段落对比, 音量自动化, 峰均比]
tags_en: [dynamic range, section contrast, volume automation, crest factor]
alias: [动态取舍, 动态对比, dynamic range]
order: 6
links:
  - "[[glossary:dynamics]]"
  - "[[glossary:compressor]]"
  - "[[glossary:loudness-war]]"
instances:
  - openscore-000269 | 马勒《当我的爱人举行婚礼》，人声从低语到爆发，宏观动态清楚（C1）
  - giantmidi-008198 | 梅尔·博尼斯《受伤的大教堂》，听建筑感怎样一段段垒起来（C1）
  - musicnet-000091 | 贝多芬第十二四重奏慢乐章，长音之间极小的力度差（C1）
sources:
  - 宏观与微观动态的区分，依混音与母带通识核对，未抄文本
  - Macro and micro dynamics, based on general mixing and mastering practice, no text copied
updated: 2026-10-30
---

::: zh
## 问题

AI 生成的音乐常常从头到尾一样满。主歌和副歌的差别只在配器，不在力度。直接压成母带，听起来专业却没有起伏。另一头，为了制造对比硬拉音量，又会做出抽吸和忽大忽小的假动态。留多少动态，是一个取舍，不是参数默认值。

## 原理

动态分两层。宏观是段落之间的电平差，微观是音符与瞬态之间的峰均比。AI 素材通常宏观平、微观也平，因为生成时按固定密度输出，后处理又做了限幅。压缩能缩小动态，不能创造动态。真正的起伏来自编曲密度、演奏力度和音量自动化，压缩只负责把已经存在的起伏收拢。

## 做法

先定每个段落的相对电平。主歌比副歌低 2 到 4 LU，桥段可以再低一点，用音量自动化写出来，不要用压缩器压出来。段落之间的过渡用两到四小节渐变，不要一步跳到位，耳朵对突变比对差距更敏感。鼓组保留 2 到 4 dB 的峰均比，别把所有击打压成同一高度。总线压缩只在需要收拢时用，增益衰减不超过 2 dB。用整体响度范围检查，流行歌 5 到 8 LU 算正常，古典与影视可以更宽，背景音乐可以更窄。做完把监听音量调低听一遍，动态还在，说明不是靠响度撑起来的。

## 听什么

在马勒《当我的爱人举行婚礼》里，听人声从低语到爆发的过程，这是宏观动态。在梅尔·博尼斯《受伤的大教堂》里，听建筑感是怎样一段段垒起来的，段落之间有没有台阶。在贝多芬第十二四重奏的慢乐章里，听长音之间极小的力度差，这是微观动态。三处都调到同一响度再比。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C2","G2","C3","G3","C4","G4","C5","G5"],"label":"从低到高","label_en":"Low to high","hint":"听每一段是否真的有力度差，而不只是音高不同","hint_en":"Hear whether each step differs in force, not only in pitch"}
```
:::

::: en
## The problem

AI music often stays equally full from start to finish. Verse and chorus differ in instrumentation but not in force. Compress that into a master and it sounds professional without ever moving. Push levels the other way to manufacture contrast and you get pumping and fake swells. How much range to keep is a decision, not a default.

## How it works

Dynamics work on two levels. Macro dynamics are the level differences between sections; micro dynamics are the crest factor between notes and transients. AI material is usually flat on both, because generation outputs a fixed density and post-processing limits it. Compression can reduce dynamics but cannot create them. Real movement comes from arrangement density, playing force and volume automation; a compressor only gathers what already exists.

## Practice

Set a relative level for each section first. A verse 2 to 4 LU below the chorus, a bridge perhaps lower still, written with volume automation rather than squeezed out of a compressor. Shape transitions over two to four bars instead of stepping, since the ear notices a jump more than a gap. Leave the drum bus 2 to 4 dB of crest factor instead of flattening every hit to one height. Use bus compression only where you need to gather, with no more than 2 dB of gain reduction. Check the loudness range, where 5 to 8 LU is normal for pop, wider for classical and film, narrower for background music. Finally, turn the monitor level down; if the movement survives, it was not carried by loudness.

## What to listen for

In Mahler's Wenn mein Schatz Hochzeit macht, hear the voice move from murmur to outcry, which is macro dynamics. In Mel Bonis's La Cathédrale blessée, hear the structure build step by step and whether the sections leave a stair. In the slow movement of Beethoven's String Quartet No. 12, hear the tiny differences of force between long notes, which is micro dynamics. Bring all three to the same loudness first.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C2","G2","C3","G3","C4","G4","C5","G5"],"label":"Low to high","label_en":"Low to high","hint":"Hear whether each step differs in force, not only in pitch","hint_en":"Hear whether each step differs in force, not only in pitch"}
```
:::
