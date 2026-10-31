---
id: lyric-writing-for-ai
site: ai
cat: B
title: 为 AI 写词
title_en: Writing Lyrics for AI
summary: 歌词要按演唱来写，重音、换气与韵脚决定合成人声唱不唱得出来。
summary_en: Write lyrics for singing, where stress, breath and rhyme decide whether a synthetic voice can deliver them.
level: standard
tags: [歌词, 咬字, 韵脚, 人声]
tags_en: [lyrics, diction, rhyme, vocals]
alias: [写词, 歌词, lyric writing]
order: 9
links:
  - "[[glossary:text-painting]]"
  - "[[glossary:ornaments]]"
  - "[[instrument:voice]]"
instances:
  - cyberhymnal-000000 | 赞美诗的四句体，韵脚与句长都非常规整（C1）
  - thesession-015842 | 传统曲调的歌词，音节与旋律一一对应（C1）
  - atepp-001114 | 肖邦叙事曲，作为对照听无词旋律的呼吸（C1）
sources:
  - 歌词与旋律的音节对应关系；歌曲写作惯例是主要依据。
  - 合成人声的咬字限制——依据来自语音合成公开资料。
updated: 2026-10-30
---

::: zh
## 毛病在哪

给 AI 写词和写诗不一样。诗可以靠视觉排布，歌词必须被唱出来：每个音节要落在旋律上，重音要与拍点一致，换气要留出位置。合成人声对不合适的音节更不宽容，拗口的组合会直接糊成一团。

## 为什么会这样

旋律的音符数与歌词的音节数要匹配，一个音对多个音节会变成花腔，多个音对一个音节则要合并。重音落在强拍上才自然，倒过来会听成错字。韵脚帮助记忆，但不必每句都押。开口音适合长音，闭口音适合快速经过。合成人声在辅音簇、连续鼻音与快速咬字上最容易失败。

## 怎么修

先写旋律骨架，再填词，或者先写词再让旋律服从音节。每句留出换气点，长句拆成短句。避免连续三个以上辅音，避免同音重复过多。录一版人声 demo 再交给合成，能听出哪里拗口。写完后朗读一遍，读不顺的地方唱起来一定不顺。需要多语言版本时，按目标语言的音节重写，不要直译。

## 耳朵要抓的点

在赞美诗里听规整句长与韵脚的作用，在传统曲调里听音节与旋律的对应，在无词旋律里听呼吸的位置如何被留出。歌词的好坏，最终由唱出来的清晰度决定。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["C4","D4","E4","F4","E4","D4","C4","G3"],"label":"音节落在旋律上","label_en":"Syllables on a melody","hint":"每个音一个音节最清楚，挤进两个就会糊","hint_en":"One syllable per note stays clear; two per note smears"}
```
:::

::: en
## Where the fault is

Writing lyrics for AI is not writing poetry. A poem can live on the page, but lyrics must be sung: each syllable lands on a note, stress agrees with the beat, and breaths need somewhere to happen. Synthetic voices are less forgiving, and awkward consonant clusters collapse into mush.

## Why it happens

The number of notes must match the number of syllables; one note over several syllables becomes melisma, several notes over one syllable must merge. Stress belongs on strong beats, and reversing it sounds like a wrong word. Rhyme aids memory but need not appear in every line. Open vowels suit long notes and closed vowels suit fast passing. Synthetic voices fail first on consonant clusters, long nasals and rapid diction.

## How to fix it

Write a melodic skeleton first and fit words to it, or write words first and let the melody obey the syllables. Leave a breath in each phrase and split long lines. Avoid three consonants in a row and too much repetition of one vowel. Record a rough human demo before handing words to a synthetic voice to hear what is awkward. Read the lyric aloud, since anything hard to say is harder to sing. For other languages, rewrite to the target language's syllables rather than translating literally.

## What the ear catches

In the hymn, how regular line lengths and rhyme help; in the traditional tune, the one-to-one fit of syllable and note; in the wordless melody, where breaths are left. Lyrics are judged by how clearly they come out when sung.

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["C4","D4","E4","F4","E4","D4","C4","G3"],"label":"Syllables on a melody","label_en":"Syllables on a melody","hint":"One syllable per note stays clear; two per note smears","hint_en":"One syllable per note stays clear; two per note smears"}
```
:::
