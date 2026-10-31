---
id: preserving-human-expression
site: ai
cat: E
title: 保留人味
title_en: Preserving Human Expression
summary: 机器越准，人味越少，呼吸、弹性速度和微小偏差要故意留
summary_en: The more precise the machine, the less human it sounds; keep breaths, rubato and small errors on purpose.
level: standard
tags: [表情, 弹性速度, 呼吸, 人性化]
tags_en: [expression, rubato, breath, humanisation]
alias: [人味, 表情保留, human feel]
order: 10
links:
  - "[[glossary:rubato]]"
  - "[[glossary:vibrato]]"
  - "[[glossary:dynamics]]"
instances:
  - atepp-001283 | 肖邦夜曲，听速度随乐句伸缩而非等分（C1）
  - atepp-001114 | 第一叙事曲现场版，听临场的时间选择（C1）
  - openscore-000084 | 舒伯特歌曲，换气位置本身就是表情（C1）
  - musicnet-000023 | 巴赫大提琴组曲萨拉班德，听弓速与余音（C1）
sources:
  - 演奏表情与量化损失的讨论，对照演奏惯例与制作实践整理。
  - , with reference to Expression, rubato and quantisation loss.
updated: 2026-10-30
---

::: zh
## 卡住的地方

量化、修音、对齐，每一步都在去掉偏差。偏差去掉之后，拍子准了，音也准了，听起来却像演示文件。把人声修到完美，往往先失去的是换气声。人味不是玄学，它是几类可以被指认的偏差，能被去掉，也能被故意放回去。

## 背后的机制

表情主要来自三处。时间，rubato 的借与还，旋律相对伴奏的提前或延后。力度，不是音量，是触键和气息的变化，同一个音弹两次不会一样。噪声，换气、指法、弓噪、踏板，这些声音不写进谱子，却告诉听众这是一个人在演奏。听众靠这些线索判断演奏者是否投入，而不是靠音准表。机器的默认是取平均，平均恰好把这三处一起抹平，而且抹得很均匀。

## 从哪开始

不要全量化，留十到二十毫秒的偏差。长音结尾做渐弱，不要一刀切。每个乐句留换气口，管乐尤其明显，弦乐也要留。同一段录三遍，用不同的力度与时间，再挑着拼，不要只留最准的那一遍。力度变化要成句，不要一个字一个音量。rubato 要有借有还，快的地方后面要补回来。给生成部分手动加百分之五左右的时间与力度变化，别用同一个种子重复。保留一点手指离开琴键的噪声，别全都降噪掉。最后把手录版和全自动版并排听，差异就是你要保留的东西。

## 耳朵要抓的点

在肖邦夜曲里听速度怎么随乐句伸缩，在第一叙事曲的现场版里听临场的时间选择，在 Du bist die Ruh 里听换气的位置，在巴赫大提琴组曲的萨拉班德里听弓速和余音。人味就在这些不被记谱的地方。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","G4","B4","E5","D5","B4","G4","E4"],"label":"一句需要呼吸的旋律","label_en":"A phrase that needs to breathe","hint":"留一点提前与延后，听起来才像人在弹","hint_en":"Leave a little push and drag so it sounds played, not placed"}
```
:::

::: en
## Where it snags

Quantising, tuning and aligning each remove deviation. Once the deviations are gone, the beat is exact and the pitch is exact, and the result sounds like a demonstration file. Human feel is not mysterious. It consists of identifiable deviations that can be removed and can also be put back deliberately.

## The mechanism

Expression comes from three places. Time: rubato borrowing and repaying, melody arriving slightly ahead of or behind the accompaniment. Dynamics: not loudness but changes of touch and breath, so the same note played twice is never identical. Noise: breaths, finger noise, bow noise, pedal, sounds that never appear in the score yet tell a listener a person is playing. A machine defaults to the average, and the average flattens all three at once, very evenly.

## Where to start

Do not quantise everything; leave ten to twenty milliseconds of deviation. Fade the ends of long notes instead of cutting them. Keep a breath at every phrase, obvious in wind playing and still necessary in strings. Record a passage three times with different weight and timing, then assemble from the best moments rather than keeping the most accurate take. Rubato must pay back what it borrows, so a rush is recovered later. Add roughly five percent timing and velocity variation to generated parts by hand, and avoid repeating the same seed. Finally, compare the played version and the fully automatic one side by side. The difference is what you are trying to keep.

## What the ear catches

In Chopin's nocturne, listen to tempo flexing with the phrase rather than dividing evenly. In the live Ballade No. 1, listen to timing choices made in the moment. In Du bist die Ruh, listen to where the breaths fall. In the Sarabande of Bach's cello suite, listen to bow speed and the resonance after the note. Human feel lives in places the score does not notate.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["E4", "G4", "B4", "E5", "D5", "B4", "G4", "E4"], "label": "A phrase that needs to breathe", "label_en": "A phrase that needs to breathe", "hint": "留一点提前与延后，听起来才像人在弹", "hint_en": "Leave a little push and drag so it sounds played, not placed"}
```
:::
