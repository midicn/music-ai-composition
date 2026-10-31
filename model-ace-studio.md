---
id: model-ace-studio
site: ai
cat: I
title: ACE Studio（合成演唱）
title_en: ACE Studio
summary: 把歌词和旋律唱出来，音高曲线可以手绘。
summary_en: Lyrics and a melody become singing, with pitch curves you can draw.
level: standard
tags: [模型档案, 歌声合成, 人声, 插件]
tags_en: [model profile, singing synthesis, vocals, plugin]
alias: [ACE Studio, ACE 虚拟歌手, 合成演唱]
order: 7
model_vendor: ACE Studio
model_form: 插件
model_input: [歌词, MIDI, 文本]
model_output: [人声轨, 音频]
model_licence: 声库与商用授权分开核对，虚拟形象与声音的使用范围以官方条款为准
model_verified: 2026-10-30
links:
  - "[[instrument:voice]]"
  - "[[glossary:vibrato]]"
  - "[[glossary:timbre]]"
instances:
  - mutopia-000546 | 艺术歌曲的人声线条，看词怎么随旋律走——这是该类产出的参照，不是本模型生成（C1） | An art-song vocal line, to hear words riding a melody; a reference for this kind of output, not an ACE Studio generation (C1)
  - mutopia-000782 | 德沃夏克的艺术歌曲，看长句的换气与收尾——这是该类产出的参照，不是本模型生成（C1） | A Dvorak art song, to hear breath and phrase endings; a reference for this kind of output, not an ACE Studio generation (C1)
  - mutopia-000527 | 通俗歌曲的人声与钢琴，看近麦演唱的吐字——这是该类产出的参照，不是本模型生成（C1） | A popular song for voice and piano, to hear close-miked diction; a reference for this kind of output, not an ACE Studio generation (C1)
  - cyberhymnal-003336 | 中文歌词的赞美诗，看声调与旋律怎么配合——这是该类产出的参照，不是本模型生成（C1） | A hymn with Chinese words, to hear tones meeting melody; a reference for this kind of output, not an ACE Studio generation (C1)
sources:
  - 产品形态、声库与编辑方式，对照官方公开说明与条款页整理。
  - 失败模式来自公开用户报告与创作实践，未引用具体评测数据。
updated: 2026-10-30
---

::: zh
## 它接什么活

把歌词与旋律交给它，得到一条唱出来的人声轨。可以在钢琴卷帘上逐字改时值、改音高，画颤音与滑音，调气声与力度。成品能当主唱、和声或叠唱层，导成音频或直接在工程里用。它只负责人声，伴奏要你自己做或另找工具。

## 喂什么，拿什么

输入是歌词、MIDI 旋律与音符时值，部分流程可用文本提示调整唱法。输出是人声轨，可导出干声或带效果的音频。独立程序与插件两种形态，插件用于在编曲软件里边听边改。声库的语种覆盖与可用音色以官方页面为准。下面的试听与实例只是该类产出的参照，不是本模型生成。

## 最好用的地方

- 逐字对齐：时值、音高、辅音位置都能手改，做中文歌的咬字比纯文本模型可控。
- 音高曲线可手绘，颤音深度与延迟能按句调整，长音不至于一条直线。
- 多套声库可以叠成合声，做主唱加和声的设计很直接。
- 以插件形式在工程里工作，改一句词不用导来导去。

## 会翻车的地方

- 声库不是无限的：想要的音色可能没有对应声库，商用授权还要单独确认，虚拟形象的使用范围另算。
- 中文多音字与轻声容易读错，必须逐个改拼音；不改就会在整句里冒出一个错字。可复现的测法是写一句含多音字的词，听它默认怎么读。
- 长音的表情偏平，渐强渐弱要手画，否则听起来像风琴而不是人。
- 换气点默认按规则插入，快歌里常插在错的字之间，要逐句挪。
- 只出人声，编曲、混音、母带仍是你的活；把它当"完整歌曲工具"会失望。
- 声库与程序版本更新后，旧工程里的人声可能变味，重要项目要导出干声留档。

## 收费、授权与替代品

要确认：声库的商用范围、虚拟形象与声音的使用限制、订阅到期后已导出音频的使用权、训练数据与声音来源的官方说明。价格按订阅或按声库分，具体数字与地区可用性以官方页面为准。
替代：要开源、可自建声库，换 DiffSinger；要整首歌连伴奏一起出，换 Suno。它适合"人声必须逐字可控"的活。

```audiolab
{"type":"instrument","gm":"Synth Choir","synth":"vocal","phrase":["D4","F4","A4","G4","F4","E4","D4"],"label":"一条带歌词的人声线","label_en":"A sung vocal line","hint":"这里用合成合唱代替声库，听的是换气位置与长音的稳定度","hint_en":"A synthetic choir stands in for a voicebank; listen for breath placement and steady long notes"}
```
:::

::: en
## The jobs it takes

Hand it lyrics and a melody and get a sung vocal track. You edit timing and pitch syllable by syllable on a piano roll, draw vibrato and slides, and shape breath and intensity. The result can be a lead, a harmony or a stacked layer, exported as audio or used inside the session. It handles the voice only; the backing is your work or another tool's.

## What goes in, what comes out

Input is lyrics, a MIDI melody and note lengths, with some workflows taking text direction for delivery. Output is a vocal track, exportable dry or with effects. It exists as a standalone program and as a plugin, the plugin letting you revise while listening in the DAW. Language coverage and available voicebanks follow the official pages. The listening examples and instances below are references for this kind of output, not this model's generations.

## Where it shines

- Syllable-level alignment: timing, pitch and consonant placement are editable, which makes diction more controllable than with text-only models.
- Pitch curves are drawable, so vibrato depth and onset can differ per phrase and long notes need not be flat.
- Several voicebanks can be stacked into harmony, making lead-plus-backing design direct.
- Working as a plugin means changing one word does not require exporting back and forth.

## Where it falls over

- Voicebanks are finite: the timbre you want may not exist, commercial use is licensed separately, and use of a virtual persona is a further question.
- Mandarin polyphones and neutral tones are misread, so every character needs its reading checked; skip it and one wrong word surfaces in the line. A reproducible test is a phrase full of polyphonic characters, heard as delivered by default.
- Long notes stay flat in expression unless you draw the swells, and otherwise sound like an organ rather than a person.
- Breath marks are inserted by rule, often between the wrong characters in fast songs, and need moving phrase by phrase.
- It produces voice only; arrangement, mixing and mastering remain yours, so treating it as a whole-song tool disappoints.
- After program or voicebank updates, vocals in old projects can change character, so export dry stems for anything that matters.

## Cost, licence, alternatives

Confirm: the commercial scope of each voicebank, limits on virtual personas and voices, what happens to exported audio after a subscription ends, and the official statement on training data and voice sources. Pricing is by subscription or by voicebank; exact figures and regional availability belong on the official page.
Alternatives: DiffSinger for an open-source route with your own trained voicebank; Suno when you want a whole song with backing. This is the tool for work where every syllable of the vocal must be controllable.

```audiolab
{"type":"instrument","gm":"Synth Choir","synth":"vocal","phrase":["D4","F4","A4","G4","F4","E4","D4"],"label":"A sung vocal line","label_en":"A sung vocal line","hint":"A synthetic choir stands in for a voicebank; listen for breath placement and steady long notes","hint_en":"A synthetic choir stands in for a voicebank; listen for breath placement and steady long notes"}
```
:::
