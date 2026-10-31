---
id: localization-and-dubbing
site: ai
cat: F
title: 本地化配音
title_en: Localization and Dubbing
summary: 合成配音要过三关，时长、重音、发音，还有授权
summary_en: Synthetic dubbing must pass timing, stress and pronunciation, then consent
level: standard
tags: [配音, 本地化, 合成语音, 授权]
tags_en: [dubbing, localization, synthetic voice, consent]
alias: [配音本地化, 多语版本, dubbing]
order: 7
links:
  - "[[glossary:sync-license]]"
  - "[[glossary:timbre]]"
instances:
  - openscore-000269 | 德语一字一音，检查音节与音符的对齐（C1）
  - mutopia-001309 | 拉丁文合唱，辅音同步是最难的部分（C1）
  - abcmisc-000906 | 保加利亚民歌，非英语的元音与装饰（C1）
  - openscore-000538 | 法语连诵与重音，合成语音常丢（C1）
sources:
  - 配音时长适配与合成语音的授权问题，参考本地化行业惯例。
  - Dubbing timing and synthetic voice consent; general localization practice is the main basis.
updated: 2026-10-30
---

::: zh
## 卡住的地方

一部片子要做五六个语言版本，合成语音听起来已经很像，但一对口型就露馅。中文一句话八个字，英语可能要十二个音节，画面里的嘴还在动。人名、品牌、缩写的读法也常错，观众第一秒就听出来了。

## 背后的原理

配音受三个约束，时长要贴合原声的句子长度，重音要落在原演员的动作上，发音要符合当地习惯。合成语音按文本长度生成，不按画面长度，所以要么语速怪，要么溢出。韵律按标点走，不会因为画面里人物抬手而停顿。音色克隆还牵涉授权，训练数据从哪里来、能不能商用、能不能再训练，都要单独确认。

## 具体做法

配音不是翻译的附属品，要单独排期。先做翻译的时长适配，把每句的字数或音节数标出来，超出的改写而不是加速。给合成引擎一份发音表，人名、品牌、缩写逐条写清。需要严格对口型时，用音素对齐工具重排句子，或者接受画外音。合同写清声音授权的范围、期限和是否允许训练，交付时说明哪些段落是合成的。试听要找母语者，不要只靠自己的耳朵。

## 耳朵要抓的点

在马勒《流浪少年之歌》的《当我的爱人举行婚礼》里听德语每个音节怎样落在音符上，在莫扎特《安魂曲》的末日经里听合唱的辅音怎样齐，在保加利亚民歌《Katerino Mome》里听非英语的元音和装饰，在霍尔梅斯的《晨曲-哈巴涅拉》里听法语连诵。合成语音最容易丢的就是这些细节。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["C4","D4","E4","F4","E4","D4","C4","D4"],"label":"一字一音的句子","label_en":"A syllable per note","hint":"听每个字是不是都落在拍上，辅音有没有被吞掉","hint_en":"Hear whether every syllable lands on the beat and whether consonants disappear"}
```
:::

::: en
## Where it snags

One film needs five or six language versions. Synthetic voices already sound close, but the lip sync gives them away. A Chinese line of eight characters becomes twelve syllables in English while the mouth on screen is still moving. Names, brands and acronyms are also read wrongly, and the audience hears it in the first second.

## The principle

Dubbing is bound by three constraints, the length of the original line, the stress that matches the actor's gesture, and pronunciation that fits local usage. A synthetic voice is generated from text length, not picture length, so it either rushes or overruns. Prosody follows punctuation and will not pause because a character raises a hand. Voice cloning also raises consent questions, where the training data came from, whether commercial use is allowed, and whether it may be trained again.

## In practice

Dubbing is not a by-product of translation and needs its own schedule. Adapt the translation for length first, marking the character or syllable count of each line and rewriting whatever overruns instead of speeding it up. Give the engine a pronunciation list that spells out every name, brand and acronym. Where lip sync must be tight, use phoneme alignment to reorder the sentence, or accept a voice-over. The contract should define the scope and term of the voice licence and whether training is permitted, and the delivery should state which passages are synthetic. Have a native speaker audition the result rather than trusting your own ear.

## What the ear catches

In Mahler's Wenn mein Schatz Hochzeit macht, how each German syllable sits on a note; in the Dies irae of Mozart's Requiem, how the choir aligns its consonants; in the Bulgarian folk song Katerino Mome, the vowels and ornaments of a language that is not English; in Holmes's Aubade-Habanera, French liaison and stress. These are the details a synthetic voice drops first.

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["C4","D4","E4","F4","E4","D4","C4","D4"],"label":"A syllable per note","label_en":"A syllable per note","hint":"Hear whether every syllable lands on the beat and whether consonants disappear","hint_en":"Hear whether every syllable lands on the beat and whether consonants disappear"}
```
:::
