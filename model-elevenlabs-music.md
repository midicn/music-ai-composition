---
id: model-elevenlabs-music
site: ai
cat: I
title: ElevenLabs 音乐与声音
title_en: ElevenLabs Music and Sound
summary: 音效、配音与短音乐，接口化的声音服务。
summary_en: Effects, dubbing and short music from an API-shaped audio service.
level: standard
tags: [模型档案, 音效, 配音, 声音克隆]
tags_en: [model profile, sound effects, dubbing, voice cloning]
alias: [ElevenLabs, Eleven Music, 音效生成]
order: 8
model_vendor: ElevenLabs
model_form: 网页服务
model_input: [文本, 参考音频, 人声]
model_output: [音频, 音效, 人声轨]
model_licence: 商用范围按订阅与声音授权核对，克隆声音需取得本人同意
model_verified: 2026-10-30
links:
  - "[[glossary:sync-license]]"
  - "[[instrument:voice]]"
  - "[[glossary:reverb]]"
instances:
  - oga-000003 | 一分半的紧张场景曲，看短配乐的铺陈——这是该类产出的参照，不是本模型生成（C1） | A ninety second tension cue, to hear short-form scoring; a reference for this kind of output, not an ElevenLabs generation (C1)
  - oga-000005 | 三十八秒的战斗片段，看强节奏短音效的用法——这是该类产出的参照，不是本模型生成（C1） | A thirty-eight second battle cue, to hear rhythm-driven short audio; a reference for this kind of output, not an ElevenLabs generation (C1)
  - oga-000031 | 一段氛围循环，看环境音的层次——这是该类产出的参照，不是本模型生成（C1） | An ambient loop, to hear environmental layers; a reference for this kind of output, not an ElevenLabs generation (C1)
  - cyberhymnal-003336 | 中文歌词的赞美诗，看配音与歌词的咬字——这是该类产出的参照，不是本模型生成（C1） | A hymn with Chinese words, to hear diction for dubbing; a reference for this kind of output, not an ElevenLabs generation (C1)
sources:
  - 产品线、接口与授权流程，对照官方公开说明与条款页整理。
  - 失败模式来自公开用户报告与创作实践，未引用具体评测数据。
updated: 2026-10-30
---

::: zh
## 具体的产出

用一句描述生成音效：脚步、开门、爆炸、环境底噪；也能给视频做配音与多语种替换，或用一段短描述出十几秒的音乐垫。适合给短片补音效、给游戏做临时声音、给广告配音。它是一个接口化的声音服务，音乐只是其中一项，不是它的主战场。

## 喂什么，拿什么

输入是文本，配音与克隆需要参考音频或已授权的声音。输出是音频文件，音效与人声可单独导出，音乐通常没有分轨。批量调用按字符或时长计量。可用的声音、语种与音效类别以官方页面为准。下面的试听与实例只是该类产出的参照，不是本模型生成。

## 最好用的地方

- 音效生成实用：描述具体物件与动作，能拿到可直接铺进时间线的素材。
- 配音的多语种替换省事，同一段话换语言不用重录。
- 声音克隆（经授权）能保持同一音色跨多条素材，做系列内容很省。
- 接口稳定，适合把音效与配音接进自动流程批量出。

## 会翻车的地方

- 音乐只有短垫的水平：超过十几秒就开始重复，写"主歌副歌"不会真的给你结构。可复现的测法是要求一分钟以上的曲子，听它在哪里开始循环。
- 音效的尾音常被截断，做循环会听到接缝；环境类素材尤其明显。
- 配音的情绪与口型对不齐，长句的停顿位置常与画面错开，要手动切。
- 克隆声音需要本人明确同意与验证，未经授权的声音即使技术上做得出也不能用；这是条款问题，不是技术问题。
- 语种覆盖不均，小语种与方言的发音常带口音，专业术语容易读错。
- 按字符或时长计量的额度用完后会直接拒绝请求，批量任务要留余量。

## 收费、授权与替代品

要确认：当前订阅的商用范围、克隆声音的授权与验证流程、生成音效能否作为音效库再分发、训练数据来源的官方说明。价格按订阅与用量分，具体数字与地区可用性以官方页面为准。
替代：要成段的音乐，换 Stable Audio；要能逐字控制唱法的人声，换 ACE Studio。它适合"声音素材要快、要能批量"的活。

```audiolab
{"type":"instrument","gm":"Music Box","synth":"struck","phrase":["C5","E5","G5","B5","G5","E5"],"label":"一段短音效式的动机","label_en":"A short sting","hint":"这类几秒的短素材是它最常被要求的粒度，听的是尾音是否完整","hint_en":"Short assets of a few seconds are its usual grain; listen for whether the tail is complete"}
```
:::

::: en
## Concrete output

Generate a sound effect from one description: footsteps, a door, an explosion, room tone. It also dubs video into other languages and produces short musical beds from a brief. It suits filling effects into a short film, temp sound for a game, or voice for an ad. It is an API-shaped audio service where music is one item, not the main event.

## What goes in, what comes out

Input is text; dubbing and cloning need reference audio or a consented voice. Output is audio files, with effects and voice exportable separately and music usually without stems. Batch calls are metered by characters or duration. Available voices, languages and effect categories follow the official pages. The listening examples and instances below are references for this kind of output, not this model's generations.

## Where it shines

- Effect generation is practical: describe a specific object and action and you get material that drops onto a timeline.
- Multilingual dubbing saves re-recording the same script in each language.
- Consented voice cloning holds one timbre across many assets, which suits series work.
- The interface is stable enough to wire effects and dubbing into automated batch pipelines.

## Where it falls over

- Music stays at the level of short beds: past a dozen seconds it repeats, and asking for verse and chorus does not produce structure. A reproducible test is to request more than a minute and hear where it starts looping.
- Effect tails are often cut, so loops click; ambience suffers most.
- Dubbed emotion and lip sync drift, and pause placement in long lines misses the picture and needs manual cuts.
- Cloning requires explicit consent and verification; an unauthorised voice may be technically possible but is not usable, which is a terms question, not a technical one.
- Language coverage is uneven, and minority languages and dialects carry accents while technical terms are misread.
- Metered quotas reject requests once exhausted, so batch jobs need headroom.

## Cost, licence, alternatives

Confirm: the commercial scope of your subscription, the consent and verification flow for cloned voices, whether generated effects may be redistributed as a library, and the official statement on training data. Pricing is by subscription and usage; exact figures and regional availability belong on the official page.
Alternatives: Stable Audio for music in longer sections; ACE Studio when sung words must be controlled syllable by syllable. This is the tool for sound assets that must be fast and batchable.

```audiolab
{"type":"instrument","gm":"Music Box","synth":"struck","phrase":["C5","E5","G5","B5","G5","E5"],"label":"A short sting","label_en":"A short sting","hint":"Short assets of a few seconds are its usual grain; listen for whether the tail is complete","hint_en":"Short assets of a few seconds are its usual grain; listen for whether the tail is complete"}
```
:::
