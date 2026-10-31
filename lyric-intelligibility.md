---
id: lyric-intelligibility
site: ai
cat: E
title: 咬字清晰度
title_en: Lyric Intelligibility
summary: 合成人声最常输在听不清词，问题多在辅音和字尾
summary_en: Synthetic vocals usually fail at being understood, and the fault lies in consonants and word endings.
level: standard
tags: [咬字, 辅音, 元音, 可懂度]
tags_en: [diction, consonants, vowels, intelligibility]
alias: [可懂度, 吐字, diction]
order: 5
links:
  - "[[instrument:voice]]"
  - "[[instrument:popular-voice]]"
  - "[[glossary:legato]]"
instances:
  - openscore-000039 | 法语快速歌曲，鼻化元音在快音节中的形状（C1）
  - openscore-000014 | 英语艺术歌曲，辅音起音决定词的边界（C1）
  - openscore-000008 | 德语叙事歌，三个角色的咬字必须分得开（C1）
sources:
  - 语音可懂度与共振峰的关系；语音学惯例是主要依据。
  -  (Consonants, vowels and intelligibility).
updated: 2026-10-30
---

::: zh
## 常见故障点

合成人声被抱怨最多的不是音色假，是听不清词。旋律一快、音一高，辅音先没，字尾跟着丢，听众只能靠字幕。字幕能救一时，救不了发行。听众不会替你猜，也不会替你改。可懂度可以测，不必靠感觉，也不用等听众来告诉你。

## 为什么会这样

听懂一个词靠两样东西。辅音给出词的边界，爆破音和擦音集中在二到八千赫兹，短、弱、容易被伴奏盖住。辅音还分送气与不送气，中文的 b 和 p 就靠这一点分开。元音给出词的身份，靠共振峰的位置区分。合成模型训练时优化的是“像人声”，不是“像这句话”，于是把短促的辅音抹平，把词尾并进下一个音。中文还多一层，字调要和旋律走向对齐，否则字对了调不对，听着还是别扭。

## 怎么修

先做一版慢速、逐字的参考录音，确认每个字落在哪个音上。给每个字标上音高与时长，再让模型唱，比整句生成更可控。写旋律时把字调放进去，一声可以往上，四声别硬拉到高音。一句超过八个音节就拆，在换气处断。混音时二到五千赫兹别压太狠，混响短一点，预延迟给三十毫秒以上。测法很直接，找三个人盲听写词，错一个字就回去改那一句。再用手机喇叭听一遍，小喇叭最能暴露辅音不足。

## 耳朵要抓的点

在 Mandoline 里听法语鼻化元音怎么在快速音节中保持形状，在 Come Away, Death 里听英语辅音怎么起音，在 Erlkönig 里听同一个人怎么把三个角色的咬字分开。听不清时，先怀疑辅音，再怀疑混响。合成人声先输的，就是这几处。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":96,"label":"逐字咬开的十六个音节","label_en":"Sixteen syllables bitten off one by one","hint":"每个十六分音符听字头，糊了就说明辅音被抹平","hint_en":"Listen to each onset; blur means the consonants were smoothed away"}
```
:::

::: en
## Common failure points

The most common complaint about synthetic vocals is not that the timbre sounds fake. It is that the words cannot be understood. Once the melody gets fast or high, consonants disappear first, word endings follow, and listeners reach for subtitles. Intelligibility can be tested instead of guessed, and you do not have to wait for an audience to tell you.

## Why it happens

Understanding a word depends on two things. Consonants mark where words begin and end; plosives and fricatives sit between roughly 2 and 8 kHz, and they are short, quiet and easily covered by an accompaniment. Vowels identify the word through formant positions. A synthesis model is trained to sound like a voice, not like this sentence, so it smooths brief consonants and merges word endings into the next note. Languages with lexical tone add another layer: the tone has to agree with the melodic direction, or the syllable is right and still sounds wrong.

## How to fix it

Record a slow, syllable-by-syllable reference first and confirm which note each syllable lands on. Write the melody with tone in mind; a rising tone can go up, a falling tone should not be forced to a high note. Split any phrase longer than eight syllables and break it at a breath. In the mix, do not over-compress 2 to 5 kHz, keep reverb short, and set pre-delay above thirty milliseconds. Test by having three people write down the lyrics blind. One wrong word sends that line back. Then listen on a phone speaker, which exposes missing consonants faster than monitors.

## What the ear catches

In Mandoline, listen to French nasal vowels keeping their shape in fast syllables. In Come Away, Death, listen to how English consonants start the words. In Erlkönig, listen to one singer separating three characters by diction alone. These are the first things a synthetic voice loses.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "s s s s s s s s s s s s s s s s", "bpm": 96, "label": "Sixteen syllables bitten off one by one", "label_en": "Sixteen syllables bitten off one by one", "hint": "每个十六分音符听字头，糊了就说明辅音被抹平", "hint_en": "Listen to each onset; blur means the consonants were smoothed away"}
```
:::
