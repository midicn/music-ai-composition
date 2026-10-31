---
id: model-kunlun-tiangong
site: ai
cat: I
title: 昆仑万维天工 SkyMusic
title_en: Kunlun Tiangong SkyMusic
summary: 中文整曲的早期玩家，八十秒规格，版本与入口要看清。
summary_en: An early Chinese full-song model with an eighty-second format; check version and entry.
level: standard
tags: [模型档案, 中文歌曲, 多模态, 整曲生成]
tags_en: [model profile, Chinese songs, multimodal, full-song generation]
alias: [天工, SkyMusic, 天工 SkyMusic]
order: 205
model_vendor: 昆仑万维
model_form: 网页服务
model_input: [文本, 歌词, 参考音频]
model_output: [音频]
model_licence: 生成歌曲的使用、商用与发行按天工与 Mureka 的当前条款；公测期的免费策略不代表现在的授权
model_verified: 2026-10-31
links:
  - "[[glossary:timbre]]"
  - "[[instrument:pipa]]"
  - "[[glossary:binary-form]]"
instances:
  - cyberhymnal-002209 | 十八秒的中国旋律，适合看短曲的收束（C1） | An eighteen second Chinese melody, to hear how a short piece closes (C1)
  - mutopia-000527 | 六十三秒的分节歌，句幅整齐，适合看段落与重复（C1） | A sixty-three second strophic song with even phrases, to hear sections and repetition (C1)
  - oga-000002 | 九十秒的战斗配乐，节奏密，适合看短视频卡点（C1） | A ninety second battle cue with dense rhythm, to check short-video sync points (C1)
  - groove-000007 | 65 BPM 摇滚鼓组，看慢速说唱的底盘（C1） | A 65 BPM rock kit, to hear the bed under slower rap (C1)
sources:
  - 昆仑万维天工 SkyMusic 官方发布页与产品说明（时长、采样率与歌词段落控制）。
  - 天工 SkyMusic 公测与后续 Mureka 系列的公开演进说明。
  - 天工与 Mureka 的当前条款与入口说明（生成歌曲的使用与商用范围）。
updated: 2026-10-31
---

::: zh
## 文本与音乐在同一条产品线

天工是昆仑万维的大模型品牌，SkyMusic 是其中的音乐分支，和文本、图片、搜索放在同一个入口下。它的定位不是专业编曲工具，而是“输入歌名、歌词、风格，出一首能听的中文歌”。对短视频、直播、活动主题曲这类需要快速出成品的场景，入口短、门槛低是优势；要工程文件与分轨，它不提供。

## 一句描述还是一整段词

可以只给主题让模型写词，也可以自带完整歌词；风格用标签或参考曲限定，部分版本支持方言与说唱。输出是混好的立体声，没有人声与伴奏分轨。歌词的段落会影响情绪走向：主歌压低、副歌抬高、桥段换配器，这些在宣传里是明确卖点，实际效果按句子质量波动。参考曲能定大致风格，但很难同时锁住音色与编曲。

| 你给的 | 它常回的 | 要盯 |
|---|---|---|
| 歌名加主题 | 自动写词，套路明显 | 副歌是否有记忆点 |
| 完整歌词 | 段落大致照做 | 长句是否被吞 |
| 参考曲 | 风格接近，音色不一定 | 是否只模仿表面 |
| 方言标记 | 发音有方言味 | 声调是否跑偏 |

## 中文说唱与短视频

在公开演示里，中文说唱是它的强项：字多、拍密、需要语气的地方，它处理得比较自然。八十秒的规格刚好覆盖短视频的副歌循环，做十五秒、三十秒裁切时，副歌位置通常能对上。古风、民谣、放克这些标签也有对应产出，适合先定方向，再拿成品去找编曲或歌手重做。

## 八十秒的天花板

八十秒意味着一首完整的主副歌刚好，前奏、间奏、尾奏要挤；想做三分钟的发行曲，得拼接或扩写，接缝处的调性与人声质感容易露。版本迭代快，早期公测的免费与不限量不代表现在；入口从独立页并到天工或 Mureka，老链接可能失效。生成队列在高峰期要等，批量出歌要留时间。

## 版本与条款

要确认：当前入口是哪一个、可用时长与采样率、生成歌曲能否商用与发行、参考曲的版权责任、是否需要标注 AI 生成。具体以天工与 Mureka 的当前条款为准。替代：要更长的整曲，换 YuE 或 MiniMax Music；要分轨，换腾讯音乐天琴；要网页端多风格快速试听，换 Suno。

```audiolab
{"type":"instrument","gm":"Shamisen","synth":"plucked","phrase":["D4","D4","F4","G4","A4","G4","F4","D4"],"label":"一段短促的古风动机","label_en":"A short, plucked guofeng motif","hint":"听咬字与鼓点是否咬合，而不是各走各的","hint_en":"Hear whether the vocal and the beat lock together instead of drifting apart"}
```
:::

::: en
## Text and music on one product line

Tiangong is Kunlun's large-model brand, and SkyMusic is its music branch, sitting beside text, image and search in the same entry. It is not a professional arranging tool; it is "give a title, lyrics and a style, get a listenable Chinese song". For short video, livestreams and event themes that need a quick finish, the short path and low barrier are the advantage. It does not give you a project file or stems.

## A prompt or a full lyric

You can give only a theme and let the model write words, or bring a complete lyric; style comes from tags or a reference track, and some versions support dialects and rap. Output is a mixed stereo file without vocal and backing stems. Lyric sections steer the emotional arc: verses lower, choruses lift, bridges change instrumentation. That is the stated selling point, though results vary with the lines. A reference track fixes a broad style, rarely timbre and arrangement at once.

| You give | It often returns | Watch |
|---|---|---|
| Title and theme | Auto-written lyrics with familiar shapes | Whether the chorus has a hook |
| Full lyrics | Sections roughly followed | Whether long lines are swallowed |
| Reference track | Close style, uncertain timbre | Whether it copies only the surface |
| Dialect tag | Audible dialect colour | Whether tones drift |

## Chinese rap and short video

In public demos, Chinese rap is a strength: dense syllables, tight beats and places that need attitude are handled with reasonable ease. The eighty-second format fits a short-video chorus loop, and fifteen or thirty second cuts usually land on the chorus. Guofeng, folk and funk tags have corresponding output, which is enough to set a direction before taking the result to an arranger or singer.

## The eighty-second ceiling

Eighty seconds holds one verse and one chorus, with intro, interlude and outro squeezed in. A three-minute release needs stitching or extension, and the joins expose key and vocal timbre. Versions move fast: the free, unlimited public beta does not describe current access, and entries have moved from a standalone page into Tiangong or Mureka, so old links may fail. Queues at peak hours add waiting time, which matters for batch work.

## Versions and terms

Confirm: which entry is current, available duration and sample rate, whether generated songs may be used commercially and released, who is responsible for reference-track rights, and whether AI disclosure is required. The current Tiangong and Mureka terms are the authority. Alternatives: YuE or MiniMax Music for longer songs; TME Tianqin for stems; Suno for quick multi-style auditions in a browser.
:::
