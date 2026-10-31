---
id: model-tme-tianqin
site: ai
cat: I
title: 腾讯音乐天琴
title_en: TME Tianqin
summary: 平台里的工具链：分轨、分析、修音与曲谱，不是一键整曲。
summary_en: A toolchain inside a music platform: stems, analysis, repair and scores, not one-click songs.
level: standard
tags: [模型档案, 中文歌曲, 分轨, 平台工具]
tags_en: [model profile, Chinese songs, stems, platform tools]
alias: [天琴, 天琴实验室, TME Studio]
order: 203
model_vendor: 腾讯音乐娱乐（天琴实验室）
model_form: 网页服务
model_input: [音频, 文本]
model_output: [分轨, 音频]
model_licence: 上传素材、产出与商用范围按腾讯音乐相关产品条款；账号类型与授权范围需逐项确认
model_verified: 2026-10-31
links:
  - "[[glossary:stems]]"
  - "[[instrument:erhu]]"
  - "[[glossary:sample-rate]]"
instances:
  - pdmx-000048 | 波萨诺瓦编制，人声与吉他贝斯贴得近，适合看分离残渣（C1） | A bossa arrangement with voice close to guitar and bass, to inspect separation residue (C1)
  - cyberhymnal-002209 | 十八秒的中国旋律，适合看 MIR 能否抓住五声调式（C1） | An eighteen second Chinese melody, to see whether MIR captures a pentatonic mode (C1)
  - cyberhymnal-003336 | 中文歌词的短赞美诗，看字与音的对应（C1） | A short hymn with Chinese words, to hear syllables mapped to notes (C1)
  - groove-000001 | 105 BPM 放克鼓组，看鼓轨分离与节拍分析（C1） | A 105 BPM funk kit, to check drum separation and beat analysis (C1)
sources:
  - 腾讯音乐天琴实验室与 TME Studio 的公开产品页（功能入口与工具清单）。
  - TME Studio 官方说明中的音乐分离、MIR 计算、辅助写词与智能曲谱范围。
  - 腾讯音乐相关产品条款与账号权限说明（上传素材、产出使用与商用）。
updated: 2026-10-31
---

::: zh
## 一条平台里的工具链

天琴是腾讯音乐的音视频技术团队，能力散在 TME Studio、QQ 音乐等产品里，不是单一模型。它接的活很具体：把一首成品拆成人声、鼓、贝斯、吉他、钢琴；分析 BPM、调性、和弦与副歌位置；给作词找押韵；把音频转成吉他谱。整曲生成不是它的主线，别拿它当 Suno 用。天琴实验室另有听歌识曲、智能修音、音频超分与母带处理，这些能力分散在不同入口。

## 上传一首歌，能拆出什么

输入是音频，输出是分轨、分析数据或曲谱。分离的颗粒度按乐器分，不是按演奏段落分；鼓轨里军鼓与镲片仍会互相带。MIR 给的是估算值，调性与和弦在转调、离调段常出错，BPM 在半拍与双拍之间也可能判反。辅助写词给的是候选词，不是成句；智能曲谱给的是吉他谱，不是总谱。

| 工具 | 产出 | 适用 |
|---|---|---|
| 音乐分离 | 人声、鼓、贝斯、吉他、钢琴 | 重混、采样、伴奏 |
| MIR 计算 | BPM、调性、和弦、副歌位置 | 编曲参考、检索 |
| 辅助写词 | 押韵词与候选句 | 填词起步 |
| 智能曲谱 | 吉他谱 | 弹唱、教学 |

## 中文歌的分轨与分析

中文流行歌的人声常压得靠前，混响与延迟多，分离后的人声轨会带空间残渣；戏曲、民歌的颤音与滑音，容易被当成噪声削掉。好处是平台曲库大，中文歌的训练素材足，常见编制拆得比较干净。中文歌的伴奏轨、翻唱底轨是它的常见用法；要拆戏曲的细碎装饰音，仍要手修。

## 平台锁定与导出限制

工具在网页里，账号、额度、导出格式都受平台控制；分轨的采样率与位深不一定能选，批量处理要按档位。上传的歌曲涉及版权，公开曲库里的歌不等于可以随便上传处理。跨产品跳转也麻烦：分离在 TME Studio，发行在另一个入口，工程文件不跟人走。想把分轨带进自己的 DAW，先确认导出格式与命名规则。

## 授权与替代路线

要确认：上传素材的保留期与用途、分轨能否商用、产出的归属、账号类型对应的权限。具体以腾讯音乐相关产品条款为准。替代：要一键出整曲，换 Suno 或 MiniMax Music；要更干净的分轨，换 Demucs 或 LALAL.AI；要可编程的分离，换开源模型自己部署。

```audiolab
{"type":"instrument","gm":"Fiddle","synth":"bowed","phrase":["D4","E4","G4","A4","G4","E4","D4","A3"],"label":"一句带滑音感的五声旋律","label_en":"A pentatonic line with room for slides","hint":"分离工具该保住连弓与滑音，而不是把每个音切成块","hint_en":"A separator should keep the bow and slides, not chop every note into blocks"}
```
:::

::: en
## A toolchain inside a platform

Tianqin is Tencent Music's audio and video technology team, and its capabilities are spread across TME Studio, QQ Music and other products rather than packaged as one model. The jobs are concrete: split a finished track into vocals, drums, bass, guitar and piano; estimate BPM, key, chords and chorus positions; suggest rhymes for lyric writing; turn audio into a guitar score. Whole-song generation is not the main line, so do not treat it as Suno. The lab also works on music recognition, vocal repair, audio upscaling and mastering, each at a different entry point.

## What comes out of an uploaded song

Input is audio; output is stems, analysis data or a score. Separation works by instrument, not by performed section, and snare and cymbals still bleed into each other in the drum stem. MIR returns estimates: key and chords often fail at modulations and borrowed harmony, and BPM can be halved or doubled. Lyric assistance offers candidate rhymes, not finished lines; the smart score is a guitar part, not a full score.

| Tool | Output | Use |
|---|---|---|
| Music separation | Vocals, drums, bass, guitar, piano | Remix, sampling, backing |
| MIR analysis | BPM, key, chords, chorus positions | Arrangement reference, search |
| Lyric assistance | Rhymes and candidate lines | Starting a lyric |
| Smart score | Guitar tab | Strumming, teaching |

## Chinese songs, stems and analysis

Chinese pop vocals usually sit forward with plenty of reverb and delay, so the separated vocal keeps spatial residue; vibrato and slides in opera and folk styles are easily treated as noise and shaved off. The upside is a large Chinese catalogue, so common arrangements separate reasonably cleanly. For backing tracks and cover beds it saves time; for the fine ornaments of opera, expect hand repair.

## Platform lock-in and export limits

The tools live in a browser, and account, quota and export format are all controlled by the platform; sample rate and bit depth may not be selectable, and batch work depends on your tier. Uploaded songs carry rights, and a track being public does not mean it can be uploaded for processing. Moving between products is awkward: separation happens in TME Studio, release somewhere else, and the project file does not travel with you. Before taking stems into your DAW, confirm formats and naming.

## Licensing and alternatives

Confirm: retention and use of uploaded material, whether stems may be used commercially, who owns the output, and what your account tier permits. The current Tencent Music product terms are the authority. Alternatives: Suno or MiniMax Music for finished songs; Demucs or LALAL.AI for cleaner separation; an open model you deploy yourself if you need programmatic access.
:::
