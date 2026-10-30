---
id: model-stable-audio
site: ai
cat: I
title: Stable Audio
title_en: Stable Audio
summary: 无人声的器乐、循环与音效，时长能指定。
summary_en: Instrumental beds, loops and effects with a duration you can set.
level: standard
tags: [模型档案, 文本生成, 器乐, 音效]
tags_en: [model profile, text to music, instrumental, sound design]
alias: [Stable Audio, 稳定音频, 器乐生成]
order: 3
model_vendor: Stability AI
model_form: 网页服务
model_input: [文本, 参考音频]
model_output: [音频]
model_licence: 商用范围随服务条款与订阅档位变化，训练数据来源以官方说明为准
model_verified: 2026-10-30
links:
  - "[[glossary:sampler]]"
  - "[[instrument:polysynth]]"
  - "[[glossary:reverb]]"
instances:
  - oga-000031 | 一段氛围循环，看铺底类素材的层次——这是该类产出的参照，不是本模型生成（C1） | An ambient loop, to hear the layering of bed material; a reference for this kind of output, not a Stable Audio generation (C1)
  - groove-000001 | 105 BPM 放克鼓组，看循环的律动密度——这是该类产出的参照，不是本模型生成（C1） | A 105 BPM funk kit, to hear the density of a loop; a reference for this kind of output, not a Stable Audio generation (C1)
  - oga-000009 | 海滩场景的短铺底，看环境声与器乐怎么混——这是该类产出的参照，不是本模型生成（C1） | A short beach cue, to hear ambience mixed with instruments; a reference for this kind of output, not a Stable Audio generation (C1)
  - mutopia-000059 | 赞美诗旋律，看两小节就能成立的短动机——这是该类产出的参照，不是本模型生成（C1） | A hymn tune, to hear a motif that works in two bars; a reference for this kind of output, not a Stable Audio generation (C1)
sources:
  - 产品能力、时长设置与导出形态，依官方公开说明与条款页核对，未抄原文
  - 失败模式依公开用户报告与创作实践归纳，未引用具体评测数据
updated: 2026-10-30
---

::: zh
## 它能做什么

描述一段氛围或一件乐器的织体，它给出一段无人声的器乐，时长可以指定，从几秒的转场到一分多钟的铺底。也支持拿一段已有音频做变形，保留走向、换掉音色。适合给视频配底、做游戏环境层、做采样素材。它不处理歌词与人声，那是另一类工具的事。

## 输入与输出

输入是文本描述，部分档位接受参考音频做音频到音频的转换。输出是立体声音频，通常没有分轨。指定的时长决定生成的长度，但不会自动做成可无缝循环的片段。同一描述每次结果不同，音色与织体变化明显。下面的试听与实例只是该类产出的参照，不是本模型生成。

## 强项

- 环境铺底与氛围织体是它的舒适区，长音、纹理、空间感都站得住。
- 时长可控，做转场、做片头、做固定长度的底噪都省去裁剪。
- 音频到音频的变形能保留原素材的节奏骨架，换掉配器。
- 无人声，条款上少一层人声与肖像的牵连，做商用底乐时省事。

## 弱项与翻车点

- 要循环就会听到接缝：首尾电平与混响不对齐，直接设成循环模式会有一声咔哒。可复现的测法是把片段循环播放十次，接缝处最清楚。
- 描述里写曲式（"两段副歌再桥段"）几乎没有响应，它给的是连续织体，不是有段落的曲子。
- 人声请求会被做成含混的类人声纹理，歌词完全听不出，别指望它唱。
- 同描述两次生成的低频量差别很大，做一组素材时响度不统一，需要逐条归一。
- 参考音频的转换幅度不好控制，稍微加大就丢掉原素材的可辨识特征。
- 极短的片段（一两秒）常带淡入淡出，想做打击类采样得自己切。

## 条款、价格与替代

要确认：当前档位的商用范围、生成音频的再许可条件、训练数据来源的官方说明、是否允许把输出作为采样库分发。价格按档位分，具体数字与地区可用性以官方页面为准。
替代：要本地跑、要能用自己的数据微调，换 MusicGen；要带人声的歌，换 Suno。两者在氛围织体的细腻度上未必更好，按是否需要离线与人声来选。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["D3","A3","F4","E4","D4","A3"],"label":"一段氛围铺底","label_en":"An ambient bed","hint":"这类长音织体是它最常被要求的素材，听的是空间与稳定度","hint_en":"Sustained textures like this are its usual job; listen for space and stability"}
```
:::

::: en
## What it lets you finish

Describe an atmosphere or an instrumental texture and it returns instrumental audio with no voice, at a length you specify, from a few-second transition to a bed over a minute long. It can also transform existing audio, keeping the motion and changing the timbre. It suits video beds, game ambience layers and sample material. It does not handle lyrics or singing; that is another class of tool.

## Inputs and outputs

Input is text; some tiers accept reference audio for audio-to-audio conversion. Output is stereo audio, usually without stems. The duration you set fixes the length but does not make the result seamlessly loopable. Each run from the same description differs noticeably in timbre and texture. The listening examples and instances below are references for this kind of output, not this model's generations.

## Strengths

- Ambient beds and atmospheric textures are its comfort zone: sustained tones, grain and space hold up.
- Duration is controllable, so transitions, idents and fixed-length beds need no trimming.
- Audio-to-audio keeps the rhythmic skeleton of source material while swapping the instrumentation.
- With no voice involved, there is one less layer of vocal and likeness terms when scoring commercially.

## Weaknesses and failure modes

- Loops expose the seam: head and tail levels and reverb do not match, and looping the file as-is gives an audible click. A reproducible test is to loop it ten times and listen at the join.
- Form requests ("two choruses then a bridge") get almost no response; it returns continuous texture, not a piece with sections.
- Vocal requests become indistinct vocal-like texture with no intelligible words, so do not expect singing.
- Low-end level varies widely between runs from one description, so a set of cues needs per-file normalisation.
- The strength of audio-to-audio is hard to steer; push it and the source loses its identifying features.
- Very short clips often carry fades at both ends, so percussion samples need hand-trimming.

## Terms, price and alternatives

Confirm: commercial scope for your tier, the conditions for re-licensing generated audio, the official statement on training data, and whether output may be redistributed as a sample library. Pricing is tiered; exact figures and regional availability belong on the official page.
Alternatives: MusicGen for local runs and fine-tuning on your own data; Suno when you need a song with vocals. Neither is necessarily better at fine atmospheric texture, so choose by whether you need offline use or singing.

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["D3","A3","F4","E4","D4","A3"],"label":"An ambient bed","label_en":"An ambient bed","hint":"Sustained textures like this are its usual job; listen for space and stability","hint_en":"Sustained textures like this are its usual job; listen for space and stability"}
```
:::
