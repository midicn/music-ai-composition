---
id: blind-listening-tests
site: ai
cat: H
title: 盲听测试
title_en: Blind Listening Tests
summary: 盲听要做的只有三件事，去标签、对电平、随机顺序
summary_en: A blind test needs three things, no labels, matched levels, random order.
level: standard
tags: [盲听, 电平匹配, 偏差, 测试]
tags_en: [blind test, level matching, bias, testing]
alias: [盲听, A/B 测试, blind A/B]
order: 2
links:
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:reference-track]]"
  - "[[glossary:timbre]]"
instances:
  - atepp-001114 | 肖邦第一叙事曲现场版，与录音室版是两次演奏（C1）
  - atepp-001119 | 同一叙事曲的 1968 年录音重制版，适合做电平对齐后的比较（C1）
  - atepp-002965 | 巴赫 D 大调托卡塔，原版文件（C1）
  - atepp-002966 | 同曲“重制版”却长了三分多钟，说明标签不可信（C1）
sources:
  - 盲听与 ABX 方法的基本流程，依听测方法学通识核对，未抄原文
  - 等响与电平偏差对判断的影响，依心理声学公开资料核对，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

盲听失败，多数不是听不出来，而是测试本身不成立。你知道哪条是 AI、哪条是自己做的、哪条是第二版，判断就已经偏了。再加上电平差一两个 dB，更响的那条几乎总被选为好。一次只对比一对，听一遍就下结论，得到的多半是偏好，不是差异。

## 为什么要盲听

人判断声音时依赖上下文，看见标签就会去找证据支持已知答案，这是确认偏差。电平差也会伪装成音质差，响一点显得更清楚、更有细节。盲听要做的只有三件事，去掉标签，对齐电平，随机顺序。这样得到的答案才关于声音，而不是关于你希望谁赢。

## 做法

从同一段落截十五到三十秒，起点相同，长度相同，用整体响度对齐，不要用峰值。文件改成 A、B 这类中性名，由别人打乱顺序，答案先写在纸上再讨论。每对至少听十次，而不是一次；十次里赢不到八次，就当作听不出。问题要事先定好，是哪个结构更清楚，还是更喜欢哪个，两者不能混。偏好测试允许都不选，辨别测试必须二选一。先用一个明显的差异做对照，比如高频砍掉三 dB，确认这套流程能测出来。同一个人不要同时担任出题者与听者，否则再随机也白费。整场控制在二十分钟内，耳朵累了就停。

## 听什么

肖邦第一叙事曲的现场版与 1968 年录音重制版是两次演奏，不是同一条素材的两种处理，盲听前先确认这一点。巴赫 D 大调托卡塔的原版与重制版时长差了三分多钟，标签在这里不可信，正说明必须先去掉标签。要比较的是同一段落、同一电平下的演奏与音色，而不是封面上的字。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4","D4","C4"],"label":"同一段素材的两次播放","label_en":"One passage, two plays","hint":"先对齐音量，再判断是音色不同还是演奏不同","hint_en":"Match the level first, then ask whether timbre or playing changed"}
```
:::

::: en
## The problem

Blind tests usually fail because the test is invalid, not because the listener cannot hear. You know which file is AI, which is yours, which is version two, and the judgement is already bent. Add a one or two dB level difference and the louder file wins almost every time. One pair, one listen, one conclusion produces preference, not difference.

## Why blind

Listening depends on context. A visible label sends you looking for evidence of the answer you already hold, which is confirmation bias. Level differences also masquerade as quality, since louder seems clearer and more detailed. A blind test only has to do three things, remove labels, match level, randomize order. Then the answer is about sound rather than about who you want to win.

## Practice

Cut fifteen to thirty seconds from the same section with the same start point and length, and match integrated loudness rather than peak. Rename files A and B, let someone else shuffle the order, and write answers down before discussing them. Run at least ten trials per pair, not one; fewer than eight wins out of ten means no audible difference. Fix the question in advance, whether it is which structure is clearer or which you prefer, and never mix the two. Preference tests allow no preference; discrimination tests force a choice. Include a control with an obvious difference, such as a three dB high cut, to prove the setup works. Do not let the same person set the test and take it, or randomisation is wasted. Stop after twenty minutes, before the ears tire.

## What to listen for

The live Chopin Ballade and the 1968 remaster are two performances, not two treatments of one take, so confirm that before testing. Bach's Toccata in D major and its remastered file differ by more than three minutes, which shows the label cannot be trusted and must be removed. Compare the same passage at the same level, not the words on the cover.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "E4", "G4", "C5", "G4", "E4", "D4", "C4"], "label": "One passage, two plays", "label_en": "One passage, two plays", "hint": "先对齐音量，再判断是音色不同还是演奏不同", "hint_en": "Match the level first, then ask whether timbre or playing changed"}
```
:::
