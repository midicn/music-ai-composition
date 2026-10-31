---
id: model-minimax-music
site: ai
cat: I
title: MiniMax Music
title_en: MiniMax Music
summary: API 优先的整曲生成，中文歌能批量出，版本要锁。
summary_en: API-first full-song generation; Chinese songs at batch scale, with versions pinned.
level: standard
tags: [模型档案, 中文歌曲, API, 整曲生成]
tags_en: [model profile, Chinese songs, API, full-song generation]
alias: [MiniMax Music, MiniMax 音乐, 海螺音乐]
order: 206
model_vendor: MiniMax
model_form: 服务
model_input: [歌词, 文本, 参考音频]
model_output: [音频]
model_licence: 产出商用、署名与再分发按 MiniMax 开放平台条款；不同模型版本的许可与配额可能不同
model_verified: 2026-10-31
links:
  - "[[glossary:stems]]"
  - "[[glossary:tempo]]"
  - "[[instrument:polysynth]]"
instances:
  - cyberhymnal-002209 | 十八秒的中国旋律，短而完整，适合做批量生成的对照（C1） | An eighteen second Chinese melody, short but complete, as a control for batch generation (C1)
  - mutopia-000527 | 六十三秒的分节歌，看长音与句尾（C1） | A sixty-three second strophic song, to hear long notes and line endings (C1)
  - cyberhymnal-003336 | 中文歌词的短赞美诗，适合看字与音的对应（C1） | A short hymn with Chinese words, to hear syllables mapped to notes (C1)
  - groove-000006 | 138 BPM 流行鼓组，看生成曲的节拍是否稳（C1） | A 138 BPM pop kit, to check whether a generated song holds tempo (C1)
sources:
  - MiniMax 开放平台的音乐生成 API 文档（歌词、描述、返回格式与限制）。
  - MiniMax Music 模型说明与版本列表（时长、采样率与可用模式）。
  - MiniMax 开放平台服务条款（产出商用、数据使用与配额）。
updated: 2026-10-31
---

::: zh
## 先看 API，再看网页

对开发者和批量场景，MiniMax Music 的主形态是接口：一次请求，歌词加音乐描述，返回一首带人声的成品。网页与第三方平台也能用，但批量、自动化、接进自己的产品，走 API 更顺。它不管编曲工程，也不给分轨；要改一轨，得回到生成或另找分离工具。对内容团队来说，它的价值是把“出歌”变成一个可排队、可重试、可计费的任务。

## 歌词、描述与段落标记

请求里最要紧的是两个字段：歌词与 prompt。歌词可以带 [Verse]、[Chorus]、[Bridge] 这类段落标记，prompt 写曲风、情绪、人声、配器与制作质感。返回的是音频数据或下载链接，格式、采样率与时长上限按当前模型版本。提示写得越像制作 brief，结果越稳；只写“好听的流行歌”，得到的是平均值。

| 字段 | 作用 | 常见错误 |
|---|---|---|
| lyrics | 唱什么、怎么分段 | 一行太长、段标记缺失 |
| prompt | 风格、人声、编曲 | 形容词堆叠、没有具体乐器 |
| 参考音频 | 锁音色或风格 | 与文字描述冲突 |
| 版本 | 能力与上限 | 不锁版本，结果漂移 |

## 中文歌的批量生产

中文咬字、声调与句尾的处理，是它在国内场景里的主要卖点；同样的歌词，听起来更接近本地歌手的念法。批量出歌时，固定歌词与版本，只改 prompt 里的一个变量，能较快找到可用方向。短视频、广告、有声内容的配乐，用它做初稿比人工编曲快得多。当前版本标称可到约五分钟，实际长度与返回格式以文档为准。

## 返回值、重试与版本漂移

接口同步返回，长歌要等；高峰期超时与限流是常态，重试要带退避，别把并发打满。同一请求两次结果不同，人声音色与混音会有差别，跨次拼接像换人。模型版本升级后，旧 prompt 的效果会变，生产环境要锁版本，并把歌词、prompt、版本号一起存档。返回链接通常有时效，落地后立刻转存。

## 商用边界与替代

要确认：产出能否商用与发行、是否需要署名、数据保留与训练使用、并发与配额、不同版本的许可差异。具体以 MiniMax 开放平台文档与条款为准。替代：要分轨与后期，换腾讯音乐天琴；要网页端即开即用，换 Suno；要本地可控，换 YuE 或 DiffRhythm。

```audiolab
{"type":"instrument","gm":"Electric Guitar (clean)","synth":"plucked","phrase":["E3","B3","C#4","B3","A3","G#3","E3","B2"],"label":"一段适合做副歌钩子的动机","label_en":"A motif built for a chorus hook","hint":"批量生成时，先听钩子有没有被记住，再听音色","hint_en":"In batch work, hear whether the hook is memorable before judging the tone"}
```
:::

::: en
## The API first, the browser second

For developers and batch work, MiniMax Music is primarily an API: one request with lyrics and a music description returns a finished track with vocals. The web app and third-party platforms work too, but batch runs, automation and product integration are smoother through the API. It does not provide a session file or stems; changing one part means regenerating or reaching for a separation tool. For a content team, its value is turning song production into a queueable, retryable, billable job.

## Lyrics, description, section tags

Two fields matter most: lyrics and prompt. Lyrics can carry tags such as [Verse], [Chorus] and [Bridge]; the prompt describes genre, mood, voice, instrumentation and production. The response is audio data or a download link, with format, sample rate and duration ceiling set by the model version. The more the prompt reads like a production brief, the steadier the result; "a nice pop song" gets you the average.

| Field | Role | Common mistake |
|---|---|---|
| lyrics | What is sung and how it is split | Lines too long, tags missing |
| prompt | Style, voice, arrangement | Stacked adjectives, no instruments |
| reference audio | Locks timbre or style | Conflicts with the text |
| version | Capability and limits | No pin, so results drift |

## Chinese songs at batch scale

Mandarin diction, tones and sentence endings are its main advantage in the domestic market; the same lyric sits closer to how a local singer would phrase it. In batch work, fix lyrics and version, change one prompt variable at a time, and a usable direction appears quickly. For short video, ads and spoken-word beds, drafts come far faster than manual arranging. Current versions state a ceiling around five minutes; actual length and response format belong to the docs.

## Responses, retries and version drift

The call is synchronous, so long songs wait; timeouts and rate limits are normal at peak, and retries need backoff rather than full concurrency. Two calls from one request differ in vocal timbre and mix, so stitching across runs sounds like a change of singer. A model upgrade changes how old prompts behave; pin the version in production and archive lyrics, prompt and version together. Download links usually expire, so store the file immediately.

## Commercial limits and alternatives

Confirm: commercial use and release, credit requirements, data retention and training use, concurrency and quota, and licence differences between versions. The MiniMax platform docs and terms are the authority. Alternatives: TME Tianqin for stems and post-production; Suno for a browser service; YuE or DiffRhythm for local control.
:::
