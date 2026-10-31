---
id: hybrid-human-ai-performance
site: ai
cat: E
title: 人机混合演奏
title_en: Hybrid Human and AI Performance
summary: 真人加生成声部，先定谁定拍，再谈音色
summary_en: With a human performance plus generated parts, decide who owns the beat before discussing tone.
level: standard
tags: [人机协作, 时间, 律动, 演奏]
tags_en: [human and AI, timing, groove, performance]
alias: [混合演奏, 人机合奏, hybrid performance]
order: 9
links:
  - "[[glossary:rubato]]"
  - "[[glossary:tempo]]"
  - "[[glossary:dynamics]]"
instances:
  - musicnet-000288 | 莫扎特钢琴三重奏，听钢琴与弦乐谁定拍（C1）
  - musicnet-000069 | 贝多芬四重奏慢乐章，听四个人的集体呼吸（C1）
  - giantmidi-002992 | 格里格钢琴协奏曲，听独奏与乐队交换主导（C1）
  - groove-000002 | 86 BPM soul 鼓组，听 laid-back 的落点在哪（C1）
sources:
  - 合奏时间基准与速度图的做法，参考演奏与制作实践。
  -  (Ensemble timing and tempo maps).
updated: 2026-10-30
---

::: zh
## 哪里不对

真人演奏加生成声部，最容易散架的不是音色，是时间。真人会提前、会拖、会在乐句末尾呼吸，生成部分如果锁死 BPM，两条时间线就会互相拉扯。听众说不清哪里不对，只觉得“不在一起”。这种不一致在耳机里更明显，在小喇叭上反而被掩盖。

## 为什么会这样

合奏的时间基准有两种。一种是独奏者定拍，其他人跟随，速度随乐句伸缩；另一种是节奏声部定拍，独奏在上面自由。生成部分必须明确属于哪一种。让它同时跟拍又跟表情是做不到的，只能选一个，再用 tempo map 把另一部分补上。速度图记录的是每一拍的实际位置，比一个固定 BPM 更接近真人的时间。速度图不必精确到每一毫秒，但段与段之间的伸缩要留住。

## 怎么修

让真人先录一版不带节拍器的参考，从录音里提取 tempo map。生成声部按速度图走，不用固定 BPM。先对齐重音，再对齐音符起点，顺序反了会越调越乱。保留真人十到三十毫秒的提前与延后，不要量化到网格。生成部分音量低三到六分贝，加同样的房间声，放进同一个混响。生成声部不要抢独奏的换气口。检查乐句的呼吸是否同步，尤其段尾和转句。最后由演奏者听一遍，觉得“被拖着走”就重来，不要用压缩或延迟去掩盖。

## 耳朵要抓的点

在莫扎特的钢琴三重奏里听钢琴与弦乐谁让谁，在贝多芬四重奏的慢乐章里听四个人的集体呼吸，在格里格协奏曲里听独奏与乐队怎么交换主导，在 soul 86 的鼓组里听 laid-back 的落点。人机混合的成败，全在这几处。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["E4","G4","A4","B4","A4","G4","E4","D4"],"label":"一条生成的小提琴声部","label_en":"A generated violin part","hint":"跟着真人的速度图走，不要锁死 BPM","hint_en":"Follow the human tempo map instead of locking to a fixed BPM"}
```
:::

::: en
## What is off

When a human performance meets generated parts, the first thing to fall apart is rarely tone. It is time. Players push, drag and breathe at the end of phrases. If the generated part is locked to a fixed BPM, two timelines pull against each other. Listeners cannot name the fault; they just say it does not sit together.

## Why it happens

Ensemble timing follows one of two models. Either the soloist sets the pace and everyone follows, with tempo flexing by phrase, or the rhythm section holds the beat and the soloist floats above it. A generated part must belong clearly to one model. It cannot track the beat and the expression at the same time; choose one and supply the other through a tempo map. A tempo map records where each beat actually falls, which is closer to human time than a single BPM value.

## How to fix it

Record the human first without a click, then extract a tempo map from that take. Drive the generated part from the map, not from a fixed tempo. Keep the player's ten to thirty milliseconds of push and drag instead of quantising to the grid. Set the generated part three to six decibels lower, give it the same room sound, and place both in one reverb. Check that breaths line up, especially at the end of sections and at turns. Finally, have the player listen. If it feels like being dragged, start again rather than hiding it with compression or delay.

## What the ear catches

In Mozart's piano trio, listen to who yields between piano and strings. In the slow movement of Beethoven's quartet, listen to four players breathing together. In Grieg's piano concerto, listen to soloist and orchestra trading the lead. In the soul groove at 86, listen to where the laid-back feel actually lands. Hybrid performance succeeds or fails in these details.

```audiolab
{"type": "instrument", "gm": "Violin", "synth": "bowed", "phrase": ["E4", "G4", "A4", "B4", "A4", "G4", "E4", "D4"], "label": "A generated violin part", "label_en": "A generated violin part", "hint": "跟着真人的速度图走，不要锁死 BPM", "hint_en": "Follow the human tempo map instead of locking to a fixed BPM"}
```
:::
