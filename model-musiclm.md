---
id: model-musiclm
site: ai
cat: I
title: MusicLM 研究线
title_en: "The MusicLM Research Line"
summary: 从音频续写到文本生成音乐的研究脉络，方法与限制比产品更有用。
summary_en: A research line from audio continuation to text-to-music, where the method and its limits matter more than any product.
level: standard
tags: [模型档案, 研究, 生成模型, 音频, 论文]
tags_en: [model profile, research, generative model, audio, paper]
alias: [MusicLM, AudioLM, MusicFX, 谷歌音乐生成, 研究模型]
order: 15
model_vendor: Google Research
model_form: 研究模型
model_input: [文本, 音频提示]
model_output: [音频]
model_licence: 无公开权重与通用 API，论文许可与演示服务条款各自独立，训练音频的授权需按公开说明核对
model_verified: 2026-10-30
links:
  - "[[glossary:timbre]]"
  - "[[glossary:reference-track]]"
  - "[[period:impressionist]]"
instances:
  - oga-000002 | 短小的游戏场景配乐，情绪与场景绑定，适合看文本描述能否抓住功能——这是该类产出的参照，不是本模型生成（C1） | A short game cue tied to a scene, to see whether a text description captures its function; a reference for this kind of output, not a generation by this model (C1)
  - pdmx-000206 | 探戈改编，旋律与伴奏层次清楚，适合看生成模型能不能保住声部关系——这是该类产出的参照，不是本模型生成（C1） | A tango arrangement with clear melody and accompaniment layers, to see whether part relations survive; a reference for this kind of output, not a generation by this model (C1)
  - oga-000000 | 二十几秒的小品，短、完整、目标明确，接近研究模型的生成长度——这是该类产出的参照，不是本模型生成（C1） | A twenty-second miniature, short, complete and focused, close to a research model's output length; a reference for this kind of output, not a generation by this model (C1)
sources:
  - AudioLM 与 MusicLM 的建模思路（公开论文摘要）。
  - 研究模型与商用服务的差别，参考公开文档与惯例。
updated: 2026-10-30
---

::: zh
## 实际用途

帮你理解"先语义、后声学"的分层建模范式；解释为什么续写比从零生成稳；用文本描述探索音色与氛围的边界；给评估方法提供参照，例如怎么判断一段生成音频与描述相符；在读商业模型说明时，分辨哪些能力来自这类研究、哪些是产品工程。

## 怎么给，给回什么

研究阶段的输入是文本描述，或一段音频前缀用于续写；输出是单条音频，不带分轨、不带 MIDI、不带工程文件。没有公开权重，也没有面向所有开发者的通用接口；公开能试到的是消费级演示，接口与条款与论文不是一回事。输出长度有限，长曲要靠拼接或分层生成。

## 最好用的地方

- 分层 token 的思路清楚：先建语义结构，再补声学细节，长结构的稳定性由此而来。
- 续写与文本条件被放在同一框架里讨论，便于理解两者的取舍。
- 论文与评测集公开，方法可以复现，评估指标可以借用。
- 对氛围、音色与情绪的文本响应好，适合做参考音与情绪板。
- 影响了一代商业模型的设计，读懂它有助于判断产品宣传里的说法。

## 会翻车的地方

- 不是产品：没有稳定入口、没有服务承诺，不能放进交付流程。
- 结构指令弱：文本里的"三段式""转调""副歌重复"很难被准确执行，长曲中段容易散。
- 人声：唱不出可懂的歌词，人声段落更像音色而不是演唱。
- 拼接：分段生成再拼，接缝处的调性与织体会跳，需要手动过渡。
- 版权：训练音频含受版权保护的作品，授权问题在论文层面并未解决。
- 演示与论文的落差：演示服务会过滤提示、限制时长，能试到的不等于论文里的能力。

## 收费、授权与替代品

要确认的问题：论文的许可允许什么用途？演示服务的条款是否允许商用与再分发？训练数据里受版权保护的音频如何处理？把演示输出放进作品，权利状态清楚吗？

研究阶段没有价格；消费级演示是否收费、是否有地区限制，以官方页面为准。

替代：MusicGen——要能本地跑的开源权重时换它；Stable Audio——要有明确商用条款的服务时换它；MusicFX 一类演示——只想试听文本生成音乐的效果时用它。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["D3","A3","E4","F4","E4","A3","D3","A2"],"label":"一段氛围铺底","label_en":"An atmospheric bed","hint":"文本模型擅长这种没有明确旋律的材料","hint_en":"Text models do best with material that has no firm melody"}
```
:::

::: en
## In practice

Understand the hierarchy of semantic tokens followed by acoustic tokens; explain why continuation is steadier than generation from nothing; probe the edges of timbre and mood with text; borrow evaluation methods, such as how to judge whether audio matches a description; read commercial model claims and tell which abilities come from this research and which from product engineering.

## How you feed it, what it returns

At research stage the input is a text description, or an audio prefix for continuation; the output is a single audio track with no stems, no MIDI and no project file. There are no public weights and no general developer interface; what the public can try is a consumer demo whose terms differ from the paper. Output length is limited, and longer pieces need stitching or layered generation.

## Where it shines

- The layered-token idea is clear: build semantic structure first, then acoustic detail, which is where long-form stability comes from.
- Continuation and text conditioning are discussed in one framework, which makes their trade-off legible.
- Papers and evaluation sets are public, so methods can be reproduced and metrics borrowed.
- Strong text response for atmosphere, timbre and mood, which suits reference tracks and mood boards.
- It shaped a generation of commercial models, so reading it helps judge product claims.

## Where it falls over

- Not a product: no stable entry point and no service commitment, so it cannot sit in a delivery pipeline.
- Weak structural control: instructions such as three sections, a key change or a repeated chorus are poorly followed, and long pieces drift in the middle.
- Voice: it does not produce intelligible lyrics, and vocal passages read as timbre rather than singing.
- Stitching: generating in sections and joining them jumps in key and texture, and transitions need manual work.
- Rights: training audio includes copyrighted work, and the licensing question is not settled at paper level.
- Demo gap: demos filter prompts and cap length, so what you can try is not what the paper describes.

## Cost, licence, alternatives

Questions to check: what uses does the paper licence allow? Do demo terms permit commercial use and redistribution? How is copyrighted training audio handled? If demo output goes into a work, is its rights status clear?

There is no price at research stage; whether the consumer demo charges or is region-limited is as stated on the official pages.

Alternatives: MusicGen when you need open weights that run locally; Stable Audio when you need a service with explicit commercial terms; a demo such as MusicFX when you only want to hear what text-to-music sounds like.

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["D3","A3","E4","F4","E4","A3","D3","A2"],"label":"An atmospheric bed","label_en":"An atmospheric bed","hint":"Text models do best with material that has no firm melody","hint_en":"Text models do best with material that has no firm melody"}
```
:::
