---
id: extending-and-continuing
site: ai
cat: C
title: 续写与接续
title_en: Extending and Continuing
summary: 续写的难点不在第一个音，而在八小节之后往哪里去
summary_en: Continuation rarely fails at the first note; it fails where the form has to decide what comes next.
level: standard
tags: [续写, 接续, 曲式, 动机]
tags_en: [continuation, extension, form, motif]
alias: [继续生成, 往后接, continuation]
order: 3
links:
  - "[[glossary:thematic-transformation]]"
  - "[[glossary:sonata-form]]"
  - "[[glossary:tempo]]"
instances:
  - thesession-021671 | The Unfinished，只写了前半段的曲调，正好用来试接（C1）
  - giantmidi-004867 | 亨德尔 G 大调恰空，固定低音是续写的硬约束（C1）
  - atepp-001928 | 巴赫半音阶幻想曲与赋格，听织体切换而语言不变（C1）
  - giantmidi-008186 | 雷格前奏曲、帕萨卡利亚与赋格，一个素材撑起长段落（C1）
sources:
  - 续写与接续的常见失败点——依据来自生成工具公开文档。
  - 曲式与动机发展的判断方法，对照作曲教学惯例整理。
updated: 2026-10-30
---

::: zh
## 常见卡点

续写看起来最省事，给一段已有的音频或 MIDI，让它往后接。失败很少发生在第一个音，而是从第八小节开始。动机原地打转，段落没有目标，该换段的地方还在重复，结尾草草收住。听的人说不出哪里错，只觉得这不像同一首曲子。这类问题在纯音乐配乐里最明显，因为没有歌词替你撑住结构。

## 它怎么运转

续写的条件只有前面那一段。模型擅长延续表面特征，速度、调性、音色、织体密度都能对上，但它不替你决定曲式。所以往哪去必须写进条件，总长度、是否转调、第几小节换段、结尾怎么收。调性与拍号是底线，给动机一个下一步的变形，比给一堆形容词有用。

## 怎么调整

截取八到十六小节做起点，最好停在乐句的开放处，停在终止上，续写往往只再补一个终止。把速度、调性、拍号写进提示或工程，生成后重新对齐一次。一次要两个版本，一个只延续，一个做发展，变奏或转调，比较哪个更像同一首曲子。接上后先改结尾两小节，让收束落在你安排的段落位置上。接上的部分先单独听一遍，站得住再往下写。

## 耳朵要抓的点

在 The Unfinished 这类只写了前半段的曲调里，听接上去的旋律是否还在同一调式，还是悄悄换了音阶。在亨德尔的恰空里，听固定低音有没有被续写保住。在巴赫的半音阶幻想曲与赋格里，听幻想段之后如何换织体而不换语言。在雷格的前奏曲、帕萨卡利亚与赋格里，听一个素材怎样撑住长段落。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["A3","C4","E4","A4","G4","F4","E4","D4"],"label":"停在开放处的八小节","label_en":"Eight bars stopping in the open","hint":"起点停在乐句开口，续写才不会马上收尾","hint_en":"Stop on an open phrase so the continuation does not close at once"}
```
:::

::: en
## Common snags

Continuing looks like the easy job: hand over an existing audio file or MIDI part and ask for more. Failure seldom happens on the first note. It starts around bar eight, where the motif circles, the section has no destination, the place that should change keeps repeating, and the ending stops abruptly. Listeners cannot name the fault, they just feel it is no longer the same piece. It shows most in instrumental cues, where no lyric holds the structure up.

## How it runs

The only condition a continuation model gets is the passage before it. It is good at carrying surface features, tempo, key, timbre, texture density, but it will not decide the form for you. So the destination belongs in the conditions: total length, whether to modulate, which bar changes section, how to close. Key and meter are the floor; a suggested next transformation of the motif is worth more than a pile of adjectives.

## How to adjust

Cut eight to sixteen bars as the start, ideally ending on an open phrase, since a continuation after a cadence usually just adds another cadence. Put tempo, key and meter into the prompt or the session, and realign after generating. Ask for two versions, one that merely continues and one that develops, by variation or modulation, and compare which sounds like the same piece. Then rewrite the last two bars so the close lands where your form needs it, and let the joined passage stand alone before extending again.

## What the ear catches

In a tune like The Unfinished, which exists only as a first half, whether the added melody stays in the same mode or quietly changes scale. In Handel's chaconne, whether the ground bass survives the continuation. In Bach's chromatic fantasia and fugue, how the texture changes after the fantasia without changing the language. In Reger's introduction, passacaglia and fugue, how one idea carries a long span.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["A3", "C4", "E4", "A4", "G4", "F4", "E4", "D4"], "label": "Eight bars stopping in the open", "label_en": "Eight bars stopping in the open", "hint": "起点停在乐句开口，续写才不会马上收尾", "hint_en": "Stop on an open phrase so the continuation does not close at once"}
```
:::
