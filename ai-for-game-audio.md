---
id: ai-for-game-audio
site: ai
cat: F
title: 游戏音频
title_en: AI for Game Audio
summary: 游戏要的是可循环可触发的资产，不是一首完整的曲子
summary_en: A game needs loopable, triggerable assets, not a finished song
level: standard
tags: [游戏音频, 循环, 触发, 引擎]
tags_en: [game audio, loops, stingers, engine]
alias: [游戏音乐, 游戏配乐, game audio]
order: 2
links:
  - "[[glossary:stems]]"
  - "[[glossary:loudness-normalization]]"
instances:
  - oga-000293 | 菜单循环，听首尾接缝与进入速度（C1）
  - oga-000031 | 环境层的噪声底与静默，检查循环是否稳（C1）
  - oga-000056 | 紧张状态循环，听节奏层是否按拍对齐（C1）
sources:
  - 游戏音频的状态划分与循环做法，依引擎文档与制作通识核对，未抄原文
  - Game audio state design and looping, checked against engine documentation and general practice, not copied
updated: 2026-10-30
---

::: zh
## 问题

游戏音乐不是一首首独立的曲子，而是一组能被触发和循环的片段。一段战斗循环可能要播二十分钟，菜单音乐要在一秒内进入又要能无缝接回开头。用 AI 生成"一段史诗战斗音乐"很容易，做成能进引擎的资产很难。

## 原理

引擎关心的是格式而不是风格。循环点必须落在采样上，首尾电平要接得上；同一状态的不同层要共享速度、调性和小节网格；短 stinger 的尾巴不能拖进下一个状态。生成模型通常按一首歌来输出，有前奏、有收尾、有渐弱，这些在游戏里都要切掉。循环长度还决定加载方式，太长就只能流式播放。同一段素材循环二十遍，任何相位或噪声问题都会被放大，耳朵会先记住接缝。

## 做法

先写状态表，探索、战斗、胜利、失败、菜单各要什么，长度和触发条件写清楚。每个状态先生成两分钟素材，再在 DAW 里裁出可循环的段落，切掉前奏和尾音，补上循环点。所有层统一速度和调，导出时写清 BPM、拍号和循环长度。响度按平台规范统一，别让战斗音乐比对白响十 dB。生成时把无缝循环、无前奏、同一调性写进描述，能省掉一半返工。stinger 单独做，长度控制在一句对白之内。

## 听什么

在 rpg-main-menu-fanfare-loop 里听循环点有没有接缝，在 creepy-ambient-loop 里听环境层的噪声底是否稳定，在 fast-mystery-loop-040 里听紧张层的节奏是否按拍对齐。这三个都是引擎里实际会遇到的形态，比听一首完整的游戏配乐更有用。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":120,"label":"可循环的一小节","label_en":"One bar that has to loop","hint":"听首尾接不接得上，循环点比风格更难做对","hint_en":"Hear whether the ends meet; the loop point is harder to get right than the style"}
```
:::

::: en
## The problem

Game music is not a set of independent pieces but a set of fragments that can be triggered and looped. A combat loop may play for twenty minutes; menu music has to start within a second and return seamlessly to its own beginning. Generating "an epic battle cue" with AI is easy. Turning it into a usable engine asset is not.

## How it works

The engine cares about format, not style. Loop points must land on samples and levels must match across the seam; layers of one state must share tempo, key and bar grid; the tail of a stinger must not bleed into the next state. Generation models output something shaped like a song, with an intro, an ending and a fade, and in a game all three have to be cut off. Loop length also decides how the file is loaded, since a long loop can only be streamed. Any phase or noise problem is amplified when the same bar plays twenty times, and the ear learns the seam first.

## Practice

Write a state table first, exploration, combat, victory, defeat, menu, with length and trigger conditions. Generate two minutes per state, then cut a loopable section in the DAW, removing the intro and the tail and placing loop points. Keep every layer at the same tempo and key, and export with BPM, meter and loop length written into the metadata. Normalize loudness across the set rather than per file, so combat does not sit ten dB above dialogue. Ask for seamless loops, no intro and one key in the prompt; it removes half the rework. Make stingers separately and keep them shorter than a line of dialogue.

## What to listen for

In rpg-main-menu-fanfare-loop, whether the loop point has a seam; in creepy-ambient-loop, whether the noise floor stays steady; in fast-mystery-loop-040, whether the tension layer sits on the beat. These are the shapes an engine actually meets, more useful than listening to a finished game score.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":120,"label":"One bar that has to loop","label_en":"One bar that has to loop","hint":"Hear whether the ends meet; the loop point is harder to get right than the style","hint_en":"Hear whether the ends meet; the loop point is harder to get right than the style"}
```
:::
