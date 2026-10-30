---
id: reverb-and-space-ai
site: ai
cat: D
title: 空间与混响
title_en: Space and Reverb
summary: 素材自带空间时，补混响之前先决定要一个空间还是两个
summary_en: When the material already carries space, decide whether you want one room or two before adding reverb.
level: standard
tags: [混响, 空间, 早期反射, 尾音]
tags_en: [reverb, space, early reflections, decay]
alias: [混响, 空间感, reverb and space]
order: 8
links:
  - "[[glossary:reverb]]"
  - "[[glossary:stereo-technique]]"
  - "[[glossary:phase-check]]"
instances:
  - openscore-000299 | 马勒《在这样的天气里》，人声与钢琴必须共享一个空间（C1）
  - atepp-000433 | 海顿降 E 大调奏鸣曲慢乐章，近场钢琴与踏板延音的比例（C1）
  - mutopia-001413 | 萨蒂《裸体歌舞》第三首，和弦之间的空气加多了就糊（C1）
sources:
  - 早期反射与尾音的区分，依混响与空间处理通识核对，未抄文本
  - Early reflections and decay tails, based on general reverb and spatial practice, no text copied
updated: 2026-10-30
---

::: zh
## 问题

AI 生成的素材经常自带空间。人声后面有厅，鼓后面有房间，钢琴带着踏板与录音室的尾巴。很多人听不出来，又加了一个混响，结果两个空间叠在一起，声音糊成一片。要不要加，加多少，先要判断素材里已经有什么。

## 原理

混响分早期反射与尾音。早期反射给出距离与房间大小，尾音给出长度。混响不是越多越有空间，过多只会让所有乐器退到同一面墙后面。AI 素材里的空间往往是整体生成的，早期反射与乐器位置对不上，尾音却很长。再叠一个混响，等于给同一件事加了两条时间线，起音被拖模糊，字与字之间失去缝隙。低频的混响尾巴还会堆在 200 Hz 附近，让整体变闷。

## 做法

先拿干声或分轨听，把已有空间找出来。如果是分离出来的轨，尾音通常已经被削过，可以补一个短房间，前延迟 10 到 20 ms，衰减 0.8 到 1.2 秒。如果原素材自带长尾，就别再加长混响，最多用一点早期反射补距离感。需要统一空间时，所有轨共用一个混响，靠发送量区分远近。同一首歌不要超过两个混响，前延迟差控制在 10 ms 以内，否则听感会分裂。发送前高通到 200 到 300 Hz，避免低频拖尾。混响量用自动化写，副歌可以少一点，留出清晰度。

## 听什么

在马勒《在这样的天气里》里，听人声与钢琴是否在同一个空间，两个空间会立刻露馅。在海顿降 E 大调奏鸣曲的慢乐章里，听近场钢琴的干与踏板延音之间的比例。在萨蒂《裸体歌舞》第三首里，听稀疏和弦之间的空气，加多了就糊成一片。三处都先听干声，再决定补什么。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["C4","E4","G4","C5","G4","E4","C4","G3"],"label":"自带空间的和声","label_en":"Harmony that carries its own space","hint":"先听尾音有多长，再决定还要不要加混响","hint_en":"Hear how long the tail already is before deciding to add reverb"}
```
:::

::: en
## The problem

AI material often arrives with space attached. There is a hall behind the vocal, a room behind the drums, pedal and studio tail on the piano. Many people miss it, add a reverb, and stack two spaces until the mix turns to wash. Whether to add anything, and how much, starts with identifying what is already there.

## How it works

Reverb divides into early reflections and a tail. Early reflections tell you distance and room size; the tail tells you length. More reverb does not mean more space; too much pushes every instrument behind the same wall. Space in AI material is usually generated as a whole, so the early reflections do not match the instrument positions while the tail runs long. Adding another reverb gives one event two timelines, blurring attacks and closing the gaps between words. Low-frequency tails also pile up near 200 Hz and make everything dull.

## Practice

Listen to the dry signal or the stems and locate the existing space. A separated track has usually had its tail shaved, so a short room can help, with 10 to 20 ms of pre-delay and a 0.8 to 1.2 second decay. If the source already has a long tail, do not add a long reverb; at most use a little early reflection to restore distance. When the space must be unified, send every track to one reverb and let send level set the depth. Keep it to two reverbs per song, with pre-delays within 10 ms of each other, or the space splits. High-pass the send at 200 to 300 Hz to keep the low end out. Automate the amount, using less in the chorus to preserve clarity.

## What to listen for

In Mahler's In diesem Wetter, hear whether voice and piano share one space, since two spaces expose themselves immediately. In the slow movement of Haydn's Sonata in E-flat, hear the ratio between the close piano and the pedal decay. In Satie's Gymnopedie No. 3, hear the air between sparse chords, which turns to wash when overdone. Start from the dry signal in all three.

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["C4","E4","G4","C5","G4","E4","C4","G3"],"label":"Harmony that carries its own space","label_en":"Harmony that carries its own space","hint":"Hear how long the tail already is before deciding to add reverb","hint_en":"Hear how long the tail already is before deciding to add reverb"}
```
:::
