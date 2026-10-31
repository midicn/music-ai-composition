---
id: chord-lock
site: ai
cat: C
title: 和弦锁定
title_en: Locking Harmony
summary: 用级数锁走向，用低音核对转位，锁太死会压扁旋律
summary_en: Lock the progression by scale degree and check the bass, knowing that too much locking flattens the melody.
level: standard
tags: [和弦, 级数, 转调, 借用和弦]
tags_en: [chords, roman numerals, modulation, borrowed chords]
alias: [和弦锁定, 锁定和声, chord lock]
order: 133
links:
  - "[[glossary:borrowed-chord]]"
  - "[[glossary:modulation]]"
  - "[[glossary:pivot-chord]]"
instances:
  - pdmx-000575 | 维塔利《恰空》，低音循环撑住整曲，变奏再密也不离和声骨架（C1）
  - giantmidi-000504 | 斯卡拉蒂《福利亚》，短小的固定低音主题，转位变化最容易听清（C1）
  - giantmidi-004867 | 亨德尔《G 大调恰空》，大调版本的低音循环，可与小调福利亚对照（C1）
  - pdmx-002370 | 《特里斯坦》钢琴改编，属和弦迟迟不落主音，听延宕怎样改变调性（C1）
sources:
  - Walter Piston, Harmony（Norton）与 Aldwell & Schachter, Harmony and Voice Leading 中关于级数、转位与转调的写法。
  - 文本条件中的调性与和弦表达，依据公开模型文档。
updated: 2026-10-31
---

::: zh
## 音名写对了，声部还是散的

提示里写 C–G–Am–F，回来的和弦对了，低音却每小节都翻上去，副歌进不来。和弦锁定不只是根音正确，还包括转位、低音走向与每个和弦的持续长度。只给音名，模型会自由选择排列，结果常常是音响对了、声部乱了。

## 级数锁定走向

先写调性，再写级数：C 大调，I–V–vi–IV，每和弦两拍。级数比音名稳，因为移调后仍然成立，也能约束模型留在调内。要更紧，就指定低音：每小节最低音落在根音，或第一转位。低音是检查和弦最直接的地方，听不出内声部时，先看每小节的最低音走向。

## 转调与借用和弦的写法

| 目标 | 写法 | 容易出的问题 | 核对 |
|---|---|---|---|
| 固定四和弦 | 调性加级数，标明每和弦拍数 | 转位随机，低音乱跳 | 看每小节最低音 |
| 副歌转调 | 写明升全音，用共同和弦过渡两小节 | 硬切，接缝断层 | 找两调共有的和弦 |
| 借用小下属 | 写明 iv 及其出现位置 | 被当成错音改掉 | 听四级是否降三音 |
| 半音低音线 | 写出低音逐拍走向 | 生成额外和弦 | 数每拍的和弦数 |

转调最稳的写法是给一个过渡：在旧调的最后两小节引入新调的共同和弦，再落到新主和弦。借用和弦要说明功能，比如主歌结尾用 iv 接 I，比单写一个和弦名更容易被保留。

## 锁死和声的代价

和声锁得越死，旋律越容易被压成和弦音，节奏也越容易变成每拍一个和弦。整首锁死还会让低音失去对位，副歌与主歌的差别只剩配器。可行的折中是只锁段落边界两小节和低音，其余留给模型；或者先锁和声生成，再单独改旋律。锁不住的时候，先检查提示里的调性是否前后一致，再检查是否同时给了互相冲突的参考。

```audiolab
{"type":"progression","key":"C4","degrees":["I","V","vi","IV"],"beat":0.9,"label":"被锁定的四小节","label_en":"Four locked bars","hint":"先听低音是否每小节都落在根音，再想把最后一个和弦换成小下属","hint_en":"Hear whether the bass lands on the root each bar, then imagine the last chord turned minor"}
```
:::

::: en
## Right chord names, scattered voices

Write C–G–Am–F and the chords arrive correct while the bass climbs every bar and the chorus never lifts. Locking harmony is not just getting roots right; it covers inversions, bass motion and how long each chord lasts. Given names alone, the model picks its own voicings, so the harmony is right and the voices are a mess.

## Lock the progression with scale degrees

State the key, then the degrees: C major, I–V–vi–IV, two beats each. Degrees hold better than chord names because they survive transposition and keep the model inside the key. To tighten further, specify the bass: the lowest note of each bar on the root, or in first inversion. The bass is the quickest place to check harmony; when inner voices are hard to hear, follow the lowest note bar by bar.

## Writing modulations and borrowed chords

| Goal | How to write it | Usual problem | Check |
|---|---|---|---|
| Fixed four-chord loop | Key plus degrees, with beats per chord | Random inversions, jumping bass | Lowest note in each bar |
| Chorus modulation | State the whole-step lift and a two-bar common-chord transition | Hard cut, broken seam | Find the chord shared by both keys |
| Borrowed minor subdominant | Name iv and where it appears | Treated as a wrong note | Does the fourth degree flatten |
| Chromatic bass line | Spell the bass beat by beat | Extra chords appear | Count chords per beat |

The safest modulation is written as a transition: introduce a chord shared with the new key in the last two bars of the old one, then land on the new tonic. A borrowed chord needs a function, such as iv to I at the end of a verse, which survives better than a bare chord name.

## What locking costs

The tighter the harmony, the more the melody is pressed into chord tones and the more the rhythm becomes one chord per beat. Locking an entire song also costs the bass its counterpoint, until verse and chorus differ only in instrumentation. A workable compromise locks two bars at each section boundary plus the bass, and leaves the rest open; another is to lock harmony for the first pass and rewrite the melody separately. When locking fails, check that the stated key stays consistent, then check whether two conflicting references were supplied at once.

```audiolab
{"type":"progression","key":"C4","degrees":["I","V","vi","IV"],"beat":0.9,"label":"Four locked bars","label_en":"Four locked bars","hint":"Hear whether the bass lands on the root each bar, then imagine the last chord turned minor","hint_en":"Hear whether the bass lands on the root each bar, then imagine the last chord turned minor"}
```
:::
