---
id: model-vocaloid-family
site: ai
cat: I
title: 歌声合成：VOCALOID 系
title_en: "Singing Synthesis: VOCALOID and Synthesizer V"
summary: 用音符与歌词拼出人声，音高可控，咬字与表情靠手调。
summary_en: You draw notes and type words to get a singing voice; pitch is exact, diction and expression are hand-worked.
level: standard
tags: [模型档案, 歌声合成, 虚拟歌手, 人声, 合成]
tags_en: [model profile, singing synthesis, virtual singer, vocals, synthesis]
alias: [VOCALOID, Synthesizer V, 虚拟歌手, 歌声合成器, vocal synth, 洛天依]
order: 10
model_vendor: Yamaha · Dreamtonics
model_form: 本地模型
model_input: [MIDI, 歌词, 音符]
model_output: [人声, 音频]
model_licence: 声库与编辑器的商用条款、署名要求、声优同意范围需按各声库的 EULA 核对，录音与训练来源以厂商说明为准
model_verified: 2026-10-30
links:
  - "[[glossary:vibrato]]"
  - "[[glossary:timbre]]"
  - "[[instrument:voice]]"
instances:
  - mutopia-000546 | 布拉姆斯艺术歌曲，长音与辅音交替，最考验合成人声的咬字——这是该类产出的参照，不是本模型生成（C1） | A Brahms art song alternating long notes with consonants, a hard test of synthetic diction; a reference for this kind of output, not a generation by this model (C1)
  - mutopia-000001 | 分句短、换气明显，可对照合成人声的呼吸处理——这是该类产出的参照，不是本模型生成（C1） | Short phrases with audible breaths, for comparing how a synthetic voice handles breathing; a reference for this kind of output, not a generation by this model (C1)
  - mutopia-000527 | 旋律简单、歌词重复，容易听清每个字的音头——这是该类产出的参照，不是本模型生成（C1） | A simple tune with repeated words, so each syllable onset is easy to hear; a reference for this kind of output, not a generation by this model (C1)
sources:
  - VOCALOID 与 Synthesizer V 的编辑方式——依据来自厂商公开说明。
  - 歌声合成的咬字与表情处理，对照制作实践惯例整理。
updated: 2026-10-30
---

::: zh
## 能替你做完什么

给 Demo 配一条音准完全可控的示范人声；把同一段旋律换一种语言再唱一遍；给主唱堆四部和声或做加倍；把一句歌词换几种唱法做对比；导出一条干净的人声轨交给混音师。它不生成伴奏，也不会从一句话变出一首歌。

## 接口的两端

输入是音符与歌词：在钢琴卷帘里画音高与时值，逐字填词，再调颤音、力度、气声与换气位置。也可以导入 MIDI，或从一段音频里提取旋律再改。输出是人声轨，可整段导出，也可分段导出以便对画面剪辑。工程文件保存的是参数而不是音频，所以换一个声库，同一份工程会得到另一个人的声音。

## 最好用的地方

- 音高与时值可以精确到写出装饰音、滑音和真人难唱的跳进。
- 改一个字或一个音不需要重录，试错成本接近零。
- 和声、加倍与多语言版本能从同一份工程派生，改动一次全线同步。
- 输出是干声，噪声底低，便于混音与后续处理。
- 适合先做出能听的 Demo，再决定是否请真人进棚。

## 会翻车的地方

- 咬字：辅音簇、连读、中文多音字都要手动指定发音，否则会唱错字；错得很顺，粗听不出来。
- 表情：不手画参数时，长音的颤音周期过于规律，换气点落在小节线上而不是乐句里，听感像读谱。
- 音色固定：一个声库只有一种基本音色，跨到摇滚、说唱或戏剧女高音时说服力明显下降。
- 语言边界：用日语声库唱中文、用中文声库唱英文，元音与重音都会别扭；中文声调与旋律走向冲突时，只能改旋律或改字。
- 拼接：和真人录音放在同一轨，噪声底与空间感对不上，需要补环境声或做匹配处理。
- 表演：装饰音与气口由参数画出，缺少歌手临场的即兴与失误，用多了会整齐得发假。

## 收费、授权与替代品

要确认的问题：这个声库是否允许商用发行？是否要求署名声库或厂商？角色形象的使用范围到哪里？声优的同意是否覆盖改编、翻译与再分发？把导出的干声交给第三方是否允许？

价格以编辑器加声库的买断为主，也有按订阅提供的云端服务；地区可用性以官方页面为准。

替代：ACE Studio——想少调参数、要更自然的中文咬字时换它；DiffSinger 一类开源方案——要完全离线或自己训练声库时换它；真人歌手——需要即兴、气口与真实情绪时，合成仍差一层。

```audiolab
{"type":"instrument","gm":"Lead 6 (voice)","synth":"vocal","phrase":["E4","G4","A4","B4","A4","G4","F#4","E4"],"label":"一条待填词的歌唱线","label_en":"A vocal line waiting for words","hint":"先听长音是否稳，再想每个辅音该落在哪一拍","hint_en":"Hear whether the long notes hold, then decide where each consonant lands"}
```
:::

::: en
## What it finishes for you

A demo vocal with pitch you control completely; the same melody tried in another language; four-part harmony or a doubled lead from one project; several readings of one line to compare; a clean vocal stem handed to a mixer. It does not make backing tracks, and it does not turn a sentence into a song.

## Both ends of the interface

You input notes and words: pitch and duration drawn on a piano roll, one syllable per note, then vibrato, dynamics, breathiness and breath points. MIDI import and melody extraction from audio are also available. The output is a vocal track, exported whole or in sections to cut against picture. The project stores parameters rather than audio, so swapping the voicebank gives the same project another singer.

## Where it shines

- Pitch and timing precise enough for ornaments, glides and leaps a singer would find hard.
- Changing one word or one note needs no retake; iteration is nearly free.
- Harmony, doubles and language versions derive from one project and update together.
- The output is a dry stem with a low noise floor, easy to mix and process.
- Good for a listenable demo before deciding whether to book a singer.

## Where it falls over

- Diction: consonant clusters, liaisons and Chinese polyphonic characters must be set by hand, or the voice sings the wrong word, smoothly enough to pass a casual listen.
- Expression: without drawn parameters, long-note vibrato cycles too regularly and breaths land on the barline instead of the phrase, which reads as sight-reading.
- Fixed timbre: each voicebank has one basic colour and loses conviction in rock, rap or dramatic soprano material.
- Language edges: a Japanese voicebank singing Chinese, or a Chinese one singing English, distorts vowels and stress; where tone and melody conflict, one of them has to change.
- Splicing: next to a real recording the noise floor and space do not match, so room tone or a matching chain is needed.
- Performance: ornaments and breaths are drawn, not felt, and used heavily the result is too even to believe.

## Cost, licence, alternatives

Questions to check: does the voicebank licence cover commercial release? Is credit to the voicebank or vendor required? How far does the character likeness licence reach? Does the voice provider's consent cover adaptation, translation and redistribution? May you hand the exported dry stem to a third party?

Pricing is mostly a one-off editor plus voicebanks, with some cloud services billed as subscriptions; regional availability is as stated on the official pages.

Alternatives: ACE Studio when you want fewer hand-set parameters and more natural Chinese diction; an open-source system such as DiffSinger when you need full offline work or a voice you trained; a session singer when you need improvisation, breath and real emotion, where synthesis still falls a layer short.

```audiolab
{"type":"instrument","gm":"Lead 6 (voice)","synth":"vocal","phrase":["E4","G4","A4","B4","A4","G4","F#4","E4"],"label":"A vocal line waiting for words","label_en":"A vocal line waiting for words","hint":"Hear whether the long notes hold, then decide where each consonant lands","hint_en":"Hear whether the long notes hold, then decide where each consonant lands"}
```
:::
