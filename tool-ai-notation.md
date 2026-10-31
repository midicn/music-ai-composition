---
id: tool-ai-notation
site: ai
cat: J
title: 记谱与音频转谱
title_en: Notation and Audio-to-Score
summary: 把演奏或录音变成可编辑的谱面，省下打谱时间，校订仍要逐小节过。
summary_en: Turning a performance into an editable score saves engraving time, but proofreading still happens bar by bar.
level: standard
tags: [记谱, 转谱, 制谱, 校订]
tags_en: [notation, transcription, engraving, proofreading]
alias: [音频转谱, AI 记谱]
order: 3
links:
  - "[[glossary:score]]"
  - "[[glossary:ornaments]]"
  - "[[glossary:midi-protocol]]"
tool_kind: notation
tool_vendor: 记谱软件厂商
tool_form: 桌面应用
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [记谱, 编曲, 交付]
tool_verified: 2026-10-30
instances:
  - atepp-007103 | 莫扎特回旋曲，装饰音与自由速度是转谱最容易漏掉的部分（C1）；这是该工具常见产出的参照，不是该工具的演示
  - musicnet-000067 | 贝多芬四重奏，四个声部能否被拆开决定谱面能不能用（C1）；这是该工具常见产出的参照，不是该工具的演示
  - atepp-002148 | 巴赫英国组曲吉格，快速音群考验音符切分与连音线（C1）；这是该工具常见产出的参照，不是该工具的演示
  - giantmidi-003224 | 众赞歌前奏曲，密集和声最容易在转谱时糊成一片（C1）；这是该工具常见产出的参照，不是该工具的演示
sources:
  - 主流记谱与音频转谱软件公开文档所列输入输出与限制；2026-10-30 复核是主要依据。
  - 装饰音、连音线与声部划分的制谱通识——依据来自实践。
updated: 2026-10-30
---

::: zh
## 它能完成什么

它能把一段独奏录音转成可编辑的音符，让你在谱面上改而不是重新弹。能把弹进来的 MIDI 整理成有调号、有连音线、能打印的谱子。能把总谱拆成各声部分谱，检查音域与换页。能给一段即兴或民歌记谱，留住旋律骨架。也能把旧工程里杂乱的 MIDI 重新量化、改谱号、补休止符，让它在排练时看得懂。

## 它怎么工作

转谱通常分三步：先检测起音与基频，得到一串带时间的音高；再判断哪些音属于同一条旋律线，把复调拆成声部；最后按拍号、调号与常见节奏型把时值写成可读的音符，附上连音线、休止符与临时记号。输出多为 MusicXML 或 MIDI，进记谱软件后仍可改。有些工具对每个音给出置信度，低置信处会标红，提醒你回听。

## 边界与坑

第一是复调。声部越多、音区越近，拆分越容易错，四重奏常被记成两个声部，钢琴左手常与右手混在一起。第二是时间。自由速度、渐慢、装饰音、琶音与踏板延音，会让检测出的时值偏离记谱习惯；先做 tempo map 才有机会救回来。第三是记谱习惯。模型给的是音高与时值，不负责乐器写法：弓法、指法、换气、移调乐器、反复记号仍要人补。第四是校订成本。转出来的谱子很少能直接打印，逐小节对照录音的时间往往被低估。第五是它不理解句法。哪里是乐句、哪里是经过音、哪里该写成倚音而不是十六分音符，仍要读谱的人判断。

## 替代与搭配

单声部旋律可以用修音软件导出 MIDI，再手工记谱，往往比全自动更准。正式出版级谱面仍要靠 Dorico、Sibelius、MuseScore 这类软件排版，转谱工具只负责把音符倒进去。若原始录音质量差，先做降噪与分离，再转谱，错误会少很多。搭配上，把转谱结果当成草稿，而不是成品。

## 上手路径

先学三件事：给录音做 tempo map、检查声部拆分、逐小节对照原音校订。然后读这里的音频转谱、MIDI 后期编辑与文件与分轨三篇，再决定哪些段落值得自动转、哪些直接手打。

```audiolab
{"type":"instrument","gm":1,"phrase":["C4","E4","G4","C5"],"label":"谱面音型","label_en":"Notated figure","hint":"转谱后听音高与连奏是否与原演奏一致","hint_en":"After transcription, compare pitch and legato with the take"}
```
:::

::: en
## What it lets you finish

It can turn a solo recording into editable notes, so revisions happen on the page rather than in another take. It can tidy played-in MIDI into a score with key signature, slurs and printable layout. It can extract parts from a full score and check ranges and page turns. It can notate an improvisation or a folk melody and keep the melodic outline. It can also re-quantise old MIDI, fix clefs and add rests so the chart is readable at rehearsal.

## How it works

Transcription usually runs in three stages: detect onsets and fundamentals to produce timed pitches; decide which notes belong to the same line and split the polyphony into voices; then spell durations under the metre and key, adding slurs, rests and accidentals. Output is normally MusicXML or MIDI, still editable in notation software. Some tools attach a confidence value to each note and flag weak spots for checking by ear.

## Limits and traps

First, polyphony. The more voices and the closer their registers, the more the split goes wrong: a quartet may arrive as two voices, and piano left hand often merges with the right. Second, time. Rubato, ritardando, ornaments, arpeggios and pedal sustain pull detected durations away from notated convention; a tempo map is the minimum rescue. Third, notation practice. The model gives pitch and duration, not instrumental writing: bowing, fingering, breaths, transposing instruments and repeat signs are still yours. Fourth, proofreading cost. Outputs are rarely print-ready, and the hours spent checking bar by bar are routinely underestimated. Fifth, it does not understand syntax. Where a phrase ends, which note is passing, and whether a figure is a grace note or a semiquaver remain a reader's call.

## Alternatives and pairings

For a monophonic line, exporting MIDI from a tuning application and notating by hand is often more accurate than full automation. Publication-grade engraving still belongs to Dorico, Sibelius or MuseScore; the transcriber only feeds notes in. If the source recording is poor, denoise and separate first, then transcribe, and there will be fewer errors. Treat the output as a draft, never as the finished chart.

## First three things to learn

Learn three things first: making a tempo map for the recording, checking how voices were split, and proofreading bar by bar against the audio. Then read the site's pages on audio transcription, MIDI post-editing and file formats and stems before deciding which passages to automate and which to type.

```audiolab
{"type":"instrument","gm":1,"phrase":["C4","E4","G4","C5"],"label":"Notated figure","label_en":"Notated figure","hint":"After transcription, compare pitch and legato with the take","hint_en":"After transcription, compare pitch and legato with the take"}
```
:::
