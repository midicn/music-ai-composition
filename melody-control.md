---
id: melody-control
site: ai
cat: C
title: 旋律控制
title_en: Controlling Melody
summary: 哼唱给轮廓，MIDI 给音符，参考音频会把风格一起借来
summary_en: Humming gives contour, MIDI gives notes, and an audio reference lends its style along with the tune.
level: standard
tags: [旋律, 哼唱, MIDI 条件, 轮廓]
tags_en: [melody, humming, MIDI conditioning, contour]
alias: [旋律控制, 旋律参考, melody control]
order: 130
links:
  - "[[glossary:melody]]"
  - "[[glossary:phrase]]"
  - "[[glossary:counter-melody]]"
instances:
  - abcmisc-001334 | 《第十二街拉格》，切分主题反复出现，听两次的落点是否一致（C1）
  - atepp-001283 | 肖邦夜曲 Op.37 No.2，装饰音与句尾最能看出旋律有没有被改顺（C1）
  - pdmx-000575 | 维塔利《恰空》，低音循环不变，主题靠变奏推进，适合核对保留了多少（C1）
  - giantmidi-004867 | 亨德尔《G 大调恰空》，大调固定低音，与维塔利对照主题变形（C1）
sources:
  - William Russo, Composing Music（Prentice-Hall）与 Hindemith, The Craft of Musical Composition 中关于旋律轮廓与句读的章节。
  - 音频与符号两类旋律条件的差异，依据公开模型文档。
updated: 2026-10-31
---

::: zh
## 三种输入，三种后果

哼一段给模型，回来的旋律常常“像”但不对：音程差半个，句尾拐错方向。问题不在唱得准不准，而在哼唱传过去的是轮廓，不是音符。文字描述传过去的是情绪，连轮廓都没有。MIDI 传过去的是音高、时值与力度，可控性最高，也最容易被模型顺手改顺。

## MIDI 条件为什么更稳

符号输入把旋律拆成离散事件，音高与时值都有明确值，模型不必从频谱里猜。代价是它会把不规则的东西规整掉：切分的抢拍被拉回网格，装饰音被并进主音，长音的渐弱被写成固定力度。给 MIDI 时，保留原谱的节奏写法比保留音色更重要；先确认音符数与小节线对得上，再听表现力。

## 方法对照

| 输入 | 能锁住什么 | 常见失败 | 复核动作 |
|---|---|---|---|
| 哼唱，单声无伴奏 | 轮廓、句长、重音位置 | 半音被抹平，起音含糊 | 用钢琴逐个音程核对 |
| MIDI 单旋律 | 音高、时值、音区 | 切分被拉直，装饰音消失 | 数每小节音符，标出被改处 |
| 成品片段做参考 | 音色、气质、编配密度 | 旋律被整段借走，权利不清 | 只取两小节，主动改三处 |
| 文字描述走向 | 情绪、上行或下行 | 落点随机，音域失控 | 指定起音、最高音与落点 |

参考音频最容易被误用：它锁住的是“听起来像”，而不是“音符是”。想保住自己的旋律，就别把整段副歌丢进去；想借气质，取两小节，改掉句尾与节奏型，再用文字补上走向。

## 哼唱与参考音频的边界

哼唱适合起步，不适合定稿。音准漂移、气声、滑音都会让模型做出不同于谱面的判断。参考音频则会把伴奏织体、混响一并带进来，最后得到的往往是一首像那首的新歌，而不是你要的旋律。旋律一旦成为整曲的识别点，交付前必须回到谱面核对：主题第一次出现在第几小节，两次副歌的旋律是否真的相同。

```audiolab
{"type":"instrument","gm":"Flute","synth":"blown","phrase":["E4","G4","A4","G4","E4","D4","C4","D4"],"label":"一条可核对的旋律","label_en":"A melody you can check","hint":"先听轮廓，再把其中两个音改高半音，看句子是否还成立","hint_en":"Hear the contour, then raise two notes by a semitone and see whether the phrase still holds"}
```
:::

::: en
## Three inputs, three outcomes

Hum a phrase and the returned melody is often close but wrong: an interval off by a semitone, the ending turning the wrong way. The trouble is not pitch accuracy. Humming passes a contour, not notes. A text description passes a mood and not even a contour. MIDI passes pitch, duration and velocity, which gives the most control and also invites the model to smooth everything out.

## Why MIDI conditioning holds better

Symbolic input breaks the melody into discrete events with explicit pitch and length, so the model does not have to guess from a spectrum. The cost is regularisation: pushed syncopations return to the grid, ornaments merge into the main note, a decaying long note becomes a fixed velocity. With MIDI, keeping the rhythmic spelling matters more than keeping the timbre; confirm the note count and bar lines first, then listen for expression.

## Comparing the methods

| Input | What it locks | Usual failure | Check |
|---|---|---|---|
| Hummed, single line, no accompaniment | Contour, phrase length, accent placement | Semitones flattened, attacks vague | Play each interval on a piano |
| A single MIDI line | Pitch, duration, register | Syncopation straightened, ornaments lost | Count notes per bar, mark changes |
| A finished excerpt as reference | Timbre, character, arrangement density | The tune itself is borrowed, rights unclear | Take two bars, change three things |
| Described direction | Mood, rising or falling | Random landing, runaway range | Name the first note, the top note, the cadence |

An audio reference is the most misused input: it locks what something sounds like, not which notes are played. To keep your own melody, do not feed a whole chorus. To borrow a character, take two bars, change the ending and the rhythm, then describe the direction in words.

## Limits of humming and audio references

Humming is good for starting and poor for signing off. Pitch drift, breath and slides all push the model toward a reading that is not in the score. An audio reference also drags in the arrangement texture and the reverb, so what comes back is a new song that resembles that one rather than your melody. Once the melody identifies the track, check it against the score before delivery: which bar the theme first appears in, and whether the two choruses really state the same tune.

```audiolab
{"type":"instrument","gm":"Flute","synth":"blown","phrase":["E4","G4","A4","G4","E4","D4","C4","D4"],"label":"A melody you can check","label_en":"A melody you can check","hint":"Hear the contour, then raise two notes by a semitone and see whether the phrase still holds","hint_en":"Hear the contour, then raise two notes by a semitone and see whether the phrase still holds"}
```
:::
