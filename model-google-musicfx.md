---
id: model-google-musicfx
site: ai
cat: I
title: Google MusicFX / Lyria 系
title_en: Google MusicFX / Lyria
summary: 器乐铺底与音效的试验入口，人声不是它的活。
summary_en: An experimental entry for instrumental beds and effects; vocals are not its job.
level: standard
tags: [模型档案, 器乐生成, 云服务, 音效]
tags_en: [model profile, instrumental, cloud service, sound design]
alias: [MusicFX, Lyria, Google 音乐生成]
order: 6
model_vendor: Google
model_form: 网页服务
model_input: [文本]
model_output: [音频]
model_licence: 商用与再分发范围随产品与云服务条款变化，需逐项核对
model_verified: 2026-10-30
links:
  - "[[glossary:timbre]]"
  - "[[instrument:violin]]"
  - "[[period:contemporary]]"
instances:
  - oga-000001 | 三分钟的管弦场景曲，看器乐铺底的段落感——这是该类产出的参照，不是本模型生成（C1） | A three minute orchestral scene cue, to hear sectional instrumental writing; a reference for this kind of output, not a MusicFX or Lyria generation (C1)
  - oga-000011 | 一分半的 Boss 战配乐，看强节奏的器乐写作——这是该类产出的参照，不是本模型生成（C1） | A ninety second boss cue, to hear rhythm-driven instrumental writing; a reference for this kind of output, not a MusicFX or Lyria generation (C1)
  - oga-000009 | 半分钟的场景铺底，看短提示的产出粒度——这是该类产出的参照，不是本模型生成（C1） | A half minute scene bed, to hear the grain of short cues; a reference for this kind of output, not a MusicFX or Lyria generation (C1)
  - cyberhymnal-008729 | 管风琴赞美诗，看持续音与和声铺陈——这是该类产出的参照，不是本模型生成（C1） | An organ hymn, to hear sustained harmony; a reference for this kind of output, not a MusicFX or Lyria generation (C1)
sources:
  - 产品入口、可用范围与输出形态，依官方公开说明核对，未抄原文
  - 失败模式依公开用户报告与创作实践归纳，未引用具体评测数据
updated: 2026-10-30
---

::: zh
## 它能做什么

写一段描述，得到一段无人声的器乐或音效，偏向氛围、影视感、电子铺底。适合给视频找底、给游戏做环境层、给播客做片头。它也提供面向开发者的云接口，可以接进自己的流程批量调用。做的是背景与质感，不是带唱的歌。

## 输入与输出

输入主要是文本，部分入口允许选时长或乐器组合。输出是音频，没有分轨，也没有 MIDI。可用地区、账号要求与入口形态以官方页面为准，同一描述在不同入口给出的结果可能不同。下面的试听与实例只是该类产出的参照，不是本模型生成。

## 强项

- 氛围与影视感铺底稳定，长音、空间与配器层次都成立。
- 短提示就能出可用素材，做前期方向探索很快。
- 器乐写作偏保守，不会突然塞进奇怪音色，适合当背景。
- 有云接口，能接进自动化流程，批量出底乐。

## 弱项与翻车点

- 人声请求只会得到含混的类人声纹理，歌词听不出，合唱也做不了。
- 可用性与入口随地区和账号变化，今天能用的页面明天可能换位置。可复现的测法是隔一周再用同一提示，比较结果与入口。
- 时长通常偏短，做长铺底要自己拼接，接缝处电平与空间不一致。
- 编辑能力弱：生成后基本只能重来，不能指定某一段修改。
- 对精确速度、调性与和声的响应很弱，写具体数值得到的是近似。
- 风格偏某几类制作质感，想要粗糙、低保真或强失真的声音，常被"修"得太干净。

## 条款、价格与替代

要确认：所用入口（实验页或云服务）各自的商用范围、输出能否再分发、训练数据来源的官方说明；云服务还有配额与计费方式要看清。价格按产品或按量计，具体数字与地区可用性以官方页面为准。
替代：要更可控的时长与循环，换 Stable Audio；要带人声的歌，换 Suno。它适合当"快速拿到干净底乐"的那一档。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","E3","G3","B3","C4","G3","E3","C3"],"label":"一段弦乐铺底","label_en":"A string bed","hint":"这类无人声的器乐层次是它最常被要求的产出，听的是和声是否稳","hint_en":"Layered instrumental writing like this is its usual output; listen for whether the harmony holds"}
```
:::

::: en
## What it lets you finish

Write a description and get instrumental audio or an effect with no voice, leaning atmospheric, cinematic or electronic. It suits video beds, game ambience layers and podcast idents. There is also a cloud interface for developers to call in batches from their own pipeline. It makes backgrounds and texture, not sung songs.

## Inputs and outputs

Input is mainly text; some entries let you pick a duration or an instrument group. Output is audio with no stems and no MIDI. Available regions, account requirements and entry points follow the official pages, and the same description can give different results at different entries. The listening examples and instances below are references for this kind of output, not this model's generations.

## Strengths

- Atmospheric and cinematic beds are stable: sustained tones, space and layering hold together.
- Short prompts yield usable material, so early direction-finding is quick.
- Instrumental writing is conservative and rarely throws in stray timbres, which suits background use.
- A cloud interface allows automation and batch production of beds.

## Weaknesses and failure modes

- Vocal requests return indistinct vocal-like texture with no intelligible words, and choirs are out of reach.
- Availability and entry points shift with region and account, so a page usable today may move tomorrow. A reproducible test is to retry the same prompt a week later and compare both the entry and the result.
- Durations tend to be short, so long beds need stitching, and levels and space mismatch at the joins.
- Editing is weak: after generation you can mostly only reroll, not revise one section.
- Exact tempo, key and harmony get little response; specific values come back approximate.
- The style leans toward a few production flavours, and requests for rough, lo-fi or heavily distorted sound get cleaned up too much.

## Terms, price and alternatives

Confirm: the commercial scope of each entry you use, whether output may be redistributed, and the official statement on training data; cloud use adds quotas and billing to read carefully. Pricing is per product or usage; exact figures and regional availability belong on the official page.
Alternatives: Stable Audio for controllable duration and loops; Suno when you need a song with vocals. This is the quick route to clean instrumental beds.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","E3","G3","B3","C4","G3","E3","C3"],"label":"A string bed","label_en":"A string bed","hint":"Layered instrumental writing like this is its usual output; listen for whether the harmony holds","hint_en":"Layered instrumental writing like this is its usual output; listen for whether the harmony holds"}
```
:::
