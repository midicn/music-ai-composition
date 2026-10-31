---
id: model-riffusion
site: ai
cat: I
title: Riffusion
title_en: Riffusion
summary: 从频谱图生成循环，低保真与实验素材好用。
summary_en: Loops made from spectrograms, useful for lo-fi and experimental material.
level: standard
tags: [模型档案, 频谱生成, 循环, 低保真]
tags_en: [model profile, spectrogram, loops, lo-fi]
alias: [Riffusion, 频谱生成, 循环生成]
order: 5
model_vendor: Riffusion
model_form: 网页服务
model_input: [文本, 参考音频]
model_output: [音频]
model_licence: 商用范围与训练数据来源需按当前服务条款核对
model_verified: 2026-10-30
links:
  - "[[glossary:sampler]]"
  - "[[glossary:tempo]]"
  - "[[instrument:electronic-drums]]"
instances:
  - groove-000005 | 87 BPM 嘻哈鼓组，看循环的节奏骨架——这是该类产出的参照，不是本模型生成（C1） | An 87 BPM hip-hop kit, to hear a loop's rhythmic skeleton; a reference for this kind of output, not a Riffusion generation (C1)
  - groove-000002 | 86 BPM 灵魂乐鼓组，看低保真素材的松紧——这是该类产出的参照，不是本模型生成（C1） | An 86 BPM soul kit, to hear the looseness of lo-fi material; a reference for this kind of output, not a Riffusion generation (C1)
  - oga-000031 | 一段氛围循环，看可反复播放的短素材——这是该类产出的参照，不是本模型生成（C1） | An ambient loop, to hear a short repeating asset; a reference for this kind of output, not a Riffusion generation (C1)
  - groove-000007 | 65 BPM 摇滚鼓组，看慢速循环的呼吸——这是该类产出的参照，不是本模型生成（C1） | A 65 BPM rock kit, to hear the feel of a slow loop; a reference for this kind of output, not a Riffusion generation (C1)
sources:
  - 产品能力与生成方式（官方公开说明与条款页）。
  - 失败模式来自公开用户报告与创作实践，未引用具体评测数据。
updated: 2026-10-30
---

::: zh
## 用武之地

用一句描述生成一段可循环的短素材，鼓组、贝斯线、和弦铺底都能做，风格偏向低保真、电子与实验。生成的片段适合直接铺进编曲软件当循环层，或者当采样继续切。也能拿一段音频做变体，保留大致走向换音色。它做的是循环和纹理，不是有主副歌的歌。

## 怎么给，给回什么

输入是文本描述，部分档位接受参考音频。输出是音频，通常是一段可循环的短片段，没有分轨。生成在频谱图上进行，再还原成波形，这一步决定了它的声音特征。同一描述每次结果不同，音色差异明显。下面的试听与实例只是该类产出的参照，不是本模型生成。

## 最好用的地方

- 循环素材出得快，鼓与贝斯的律动密度容易调，适合做 beat 的底。
- 低保真、磁带感、颗粒感这类质感，比多数通用模型更对味。
- 一次给多个变体，做采样筛选的成本低。
- 短片段迭代快，改一个词就能听到明显不同的织体，适合找方向。

## 会翻车的地方

- 频谱还原会留下金属味：镲片与齿音发脆发毛，高频像被砂纸磨过。可复现的测法是把高频单独提起来听。
- 循环接缝对不上，首尾相位与电平不一致，直接循环会听到一声"嗒"。
- 人声完全不能用，唱出来的东西听不出词，只能当纹理。
- 没有段落概念，要求"主歌转副歌"只会得到更密的织体，不会真的转段。
- 低频常糊成一团，贝斯与底鼓抢同一块，进工程要切。
- 服务与模型会更新，上个月好用的描述这个月给出不同结果，项目要留音频副本而不是只留提示。

## 收费、授权与替代品

要确认：当前服务条款的商用范围、生成音频的再分发条件、训练数据来源的官方说明。价格按档位或按量计，具体以官方页面为准；地区可用性也以官方页面为准。
替代：要更干净的高频与更长的铺底，换 Stable Audio；要本地可控、能微调，换 MusicGen。它胜在循环手感，输在干净程度。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E2","E2","G2","A2","E2","D2","E2","G2"],"label":"一条循环贝斯线","label_en":"A looping bass line","hint":"这类两小节循环是它最常被要求的素材，听的是接缝与低频的干净度","hint_en":"Two-bar loops like this are its usual request; listen for the seam and how clean the low end is"}
```
:::

::: en
## Where it earns its place

Generate a short loopable asset from one description: drums, a bass line, a chord bed, with a lean toward lo-fi, electronic and experimental. The result drops into a DAW as a loop layer or gets chopped as a sample. It can also vary existing audio, keeping the general motion and changing timbre. It makes loops and textures, not songs with verses and choruses.

## How you feed it, what it returns

Input is text, with reference audio on some tiers. Output is audio, usually a short loopable clip, with no stems. Generation happens on a spectrogram that is then converted back to waveform, and that step defines its sound. Each run from one description differs clearly in timbre. The listening examples and instances below are references for this kind of output, not this model's generations.

## Where it shines

- Loops come fast, and the density of drums and bass is easy to steer, which suits beat beds.
- Lo-fi, tape and grain textures land closer than with most general models.
- Several variants per run make sample selection cheap.
- Short clips iterate quickly: change one word and the texture shifts, which helps find a direction.

## Where it falls over

- Spectrogram reconstruction leaves a metallic edge: cymbals and sibilance turn brittle and furry, as if the top end were sanded. A reproducible test is to solo the highs.
- Loop seams do not match; phase and level differ at head and tail, so looping as-is gives an audible tick.
- Vocals are unusable: words cannot be made out, so treat any voice as texture.
- There is no sense of sections; asking for verse into chorus yields a denser texture, not an actual transition.
- Low end often smears, with bass and kick fighting for the same band, so it needs cutting in the session.
- The service and models change, and a description that worked last month returns something else now, so archive audio rather than prompts alone.

## Cost, licence, alternatives

Confirm: the commercial scope of the current terms, conditions for redistributing generated audio, and the official statement on training data. Pricing is by tier or usage; exact figures and regional availability belong on the official page.
Alternatives: Stable Audio for cleaner highs and longer beds; MusicGen for local control and fine-tuning. It wins on loop feel and loses on cleanliness.

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["E2","E2","G2","A2","E2","D2","E2","G2"],"label":"A looping bass line","label_en":"A looping bass line","hint":"Two-bar loops like this are its usual request; listen for the seam and how clean the low end is","hint_en":"Two-bar loops like this are its usual request; listen for the seam and how clean the low end is"}
```
:::
