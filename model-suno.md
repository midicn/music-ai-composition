---
id: model-suno
site: ai
cat: I
title: Suno
title_en: Suno
summary: 整首歌连人声一起出，先拿到能听的草稿再决定改哪里。
summary_en: A whole song with vocals in one pass, enough to judge direction before production work.
level: standard
tags: [模型档案, 文本生成, 人声, 歌曲结构]
tags_en: [model profile, text to music, vocals, song structure]
alias: [Suno, 文生歌曲, text to song]
order: 1
model_vendor: Suno
model_form: 网页服务
model_input: [文本, 歌词, 参考音频]
model_output: [音频, 分轨]
model_licence: 商用范围、发行权限与训练数据来源需按当前订阅条款核对
model_verified: 2026-10-30
links:
  - "[[glossary:timbre]]"
  - "[[glossary:stems]]"
  - "[[period:contemporary]]"
instances:
  - groove-000006 | 138 BPM 流行鼓组，看整首歌的节奏底盘能否被稳定复现（C1） | A 138 BPM pop kit, to check whether a song's rhythmic bed holds (C1)
  - groove-000007 | 65 BPM 摇滚鼓组，看慢歌的推力有没有被做出来（C1） | A 65 BPM rock kit, to check the drive of a slow song (C1)
  - mutopia-000622 | 人声加钢琴的通俗歌曲，看一首歌的骨架（C1） | A voice-and-piano popular song, to hear the shape of a song (C1)
  - abcmisc-001329 | 里尔舞曲，看带重复段落的器乐小品怎么成立（C1） | A reel, to check how repeated sections hold (C1)
sources:
  - 产品能力与导出形态；官方公开说明与条款页是主要依据。
  - 失败模式来自公开用户报告与创作实践，未引用具体评测数据。
updated: 2026-10-30
---

::: zh
## 它接什么活

给一句风格描述和一段歌词，它交出一首带人声、有主副歌结构的完整歌曲。适合先要一个能听的版本：给客户定方向、给视频配临时轨、给自己的编曲找参照。也可以只出器乐，或者用一句描述快速试探某种风格。它擅长的是"从零到能听"，不负责"从能听到能上架"。

## 接口的两端

输入是文本：风格与情绪描述、歌词、可选的段落标记（主歌、副歌、桥段），部分档位接受参考音频来限定音色与律动。输出通常是立体声音频，部分档位可导出分轨与人声。同一提示会给多个候选，每次结果不同，能留档复现的只有提示与种子，不是音频本身。下面的试听与实例取自同类产出，供对照。

## 最好用的地方

- 人声与伴奏一起出，省掉找歌手、编曲、录一版小样的时间。
- 段落标记确实起作用：写了主歌副歌，结构通常照做，副歌会抬高。
- 风格跨度大，民谣、电子、管弦、摇滚都能给出可信的表面质感。
- 改一句歌词再生成，能快速比较不同唱法与断句，适合歌词打磨阶段。

## 会翻车的地方

- 三分钟以上的歌，后半段常回到前面的和声与配器。可复现的测法：同提示生成两次，比较最后三十秒，会听到几乎相同的段落。
- 咬字在快句、多音节词和中文声调上容易糊，副歌叠唱处最明显。要逐句对照歌词听，别只看波形。
- 同一提示两次生成的人声音色不一致，跨次拼接会出现像换了一个人的效果。
- 分轨不干净：人声轨常带混响尾巴和镲片残留，拿去重混得先修。
- 对精确的速度、调性与和声进行不敏感，写"125 BPM、D 小调"得到的是近似值，要精确就落到 MIDI 上重做。
- 参考音频能定大致音色，但很难同时锁住配器与律动，常出现音色对了、节奏不对。

## 收费、授权与替代品

要确认：当前订阅档位的商用范围、能否在流媒体发行、分轨与 MIDI 的导出权限、训练数据来源的官方说明。价格按档位分，具体数字与地区可用性以官方页面为准。
替代：要更接近录音的人声质感，换 Udio；只要器乐铺底、不想碰人声相关条款，换 Stable Audio。两者都可能牺牲整首歌的结构完整度，按当前任务取舍。

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E3","G#3","B3","C#4","B3","G#3","E3","B2"],"label":"一段流行吉他动机","label_en":"A pop guitar motif","hint":"这类短动机常被要求整首反复出现，可用它对照模型有没有把动机记住","hint_en":"A motif like this is usually asked to recur through a whole song; use it to check whether the model keeps it"}
```
:::

::: en
## The jobs it takes

Give it a style line and some lyrics and it returns a complete song with vocals, verses and a chorus. It is for getting a listenable version first: fixing direction with a client, temp-scoring a video, or hearing a reference for your own arrangement. You can also ask for instrumental only, or use one line to probe a style quickly. It handles zero-to-listenable, not listenable-to-releasable.

## Both ends of the interface

Input is text: style and mood, lyrics, optional section tags for verse, chorus and bridge; some tiers accept reference audio to narrow timbre and groove. Output is usually stereo audio, with stems and vocals exportable on some tiers. One prompt returns several candidates and each run differs; what you can archive and reproduce is the prompt and seed, not the audio itself. The listening examples and instances below are references for this kind of output, not this model's generations.

## Where it shines

- Vocals and backing arrive together, saving the time of hiring a singer, arranging, and cutting a demo.
- Section tags do work: write verse and chorus and the structure usually follows, with the chorus lifting.
- Broad style range: folk, electronic, orchestral and rock all get a plausible surface.
- Changing one lyric line and regenerating lets you compare phrasing quickly, which suits lyric editing.

## Where it falls over

- Past three minutes the song tends to return to earlier harmony and orchestration. A reproducible test: generate twice from one prompt and compare the last thirty seconds; the sections are nearly identical.
- Diction blurs on fast lines, long words and Mandarin tones, worst in stacked chorus vocals. Check line by line against the lyric, not just the waveform.
- Two runs from the same prompt give different vocal timbres, so stitching across runs sounds like a change of singer.
- Stems are not clean: the vocal stem often carries reverb tails and cymbal bleed, and needs repair before remixing.
- Exact tempo, key and chord progression are not honoured; "125 BPM, D minor" comes back approximate, so anything precise belongs in MIDI.
- Reference audio can fix timbre broadly but rarely groove and instrumentation at once: the tone lands, the rhythm does not.

## Cost, licence, alternatives

Confirm: the commercial scope of your current tier, whether streaming release is allowed, what export rights you have for stems and MIDI, and the official statement on training data. Pricing is tiered; exact figures and regional availability belong on the official page, and those belong on the official page.
Alternatives: Udio if you need a more recorded-sounding voice; Stable Audio if you only need instrumental beds and want to avoid vocal-related terms. Both may cost you whole-song structural coherence, so choose by the job at hand.

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E3","G#3","B3","C#4","B3","G#3","E3","B2"],"label":"A pop guitar motif","label_en":"A pop guitar motif","hint":"A motif like this is usually asked to recur through a whole song; use it to check whether the model keeps it","hint_en":"A motif like this is usually asked to recur through a whole song; use it to check whether the model keeps it"}
```
:::
