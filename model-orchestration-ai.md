---
id: model-orchestration-ai
site: ai
cat: I
title: 配器辅助模型
title_en: "Orchestration Assistants"
summary: 把钢琴草图分给各声部，省誊抄时间，平衡仍要人听。
summary_en: It spreads a piano sketch across sections, saving copying time while balance remains an ear decision.
level: standard
tags: [模型档案, 配器, 编曲, 管弦, 记谱]
tags_en: [model profile, orchestration, arranging, orchestra, notation]
alias: [配器, 自动配器, 编配助手, orchestration AI, AIVA]
order: 17
model_vendor: AIVA · 记谱软件的编配功能
model_form: 网页服务
model_input: [MIDI, 钢琴谱, 风格描述]
model_output: [MIDI, 音频]
model_licence: 生成式服务的产出归属与署名要求随档位变化，规则式功能的产出按软件许可，均需按官方条款核对
model_verified: 2026-10-30
links:
  - "[[glossary:voicing]]"
  - "[[instrument:violin]]"
  - "[[period:romantic]]"
instances:
  - musicnet-000068 | 弦乐四重奏乐章，四个声部各有独立走向，适合看配器是否尊重声部（C1） | A quartet movement with four independent lines, to see whether orchestration respects the parts (C1)
  - giantmidi-006813 | 莱茵贝格四重奏，织体厚、中频密，最容易听出配器后变浑（C1） | A Rheinberger quartet, thick in texture and crowded in the midrange, where orchestration muddies first (C1)
  - pdmx-000002 | 长笛练习曲，单线条清楚，适合看一条旋律被分到哪件乐器（C1） | A solo flute etude with one clear line, for seeing which instrument a melody is given to (C1)
  - mutopia-000498 | 交响曲乐章，动态与编制都大，适合比较草案与成品的差距（C1） | A symphony movement, large in dynamics and scoring, for comparing a draft with the finished work (C1)
sources:
  - 配器辅助的两类做法（规则式展开与生成式编配），参考公开说明。
  - 配器中的音区与平衡问题；配器实践惯例是主要依据。
updated: 2026-10-30
---

::: zh
## 能替你做完什么

把一份钢琴谱展开到弦乐、木管、铜管的各个声部；给旋律配一层和声或对位伴奏；一次出几个配器方案供试奏比较；生成多轨 MIDI，进 DAW 换成音源做 mockup；给教学演示"同一材料换编制"的差别；把草图快速变成能听的版本，先给导演或客户听方向。

## 怎么给，给回什么

输入是 MIDI 或钢琴谱，加上编制、风格与情绪的描述；输出是多轨 MIDI，或直接渲染的音频。它不给分谱排版，也不检查演奏法，声部数量、音区与换气都需要人工核。规则式功能（记谱软件里的展开与编配）结果可预测；生成式服务偏向按风格重建，不一定贴着你的动机。

## 最好用的地方

- 省誊抄与试配时间，一个动机能很快听到几种编制。
- 能给非钢琴家写出可弹的声部，避免十度叠置这类没法演奏的写法。
- 一次出多个方案，便于 A/B 试奏，不必从零改。
- 与 DAW、记谱软件衔接顺，MIDI 进去就能换音源。
- 规则式展开确定、可复现，适合教学与流水线工作。
- 适合做 mockup 前的粗配，先定方向再精修。

## 会翻车的地方

- 演奏法：不懂换气、弓法、连奏与双音限制，写得出但不好演，乐团一试就露。
- 平衡：音区与力度缺少配器常识，木管常被弦乐埋，内声部糊成一片。
- 和声：展开时把平行五度、声部交叉一起放大，四声部写作尤其明显。
- 生成式偏离：按风格重建时不一定保留你的动机与结构，改到面目全非。
- 特殊乐器：竖琴踏板、打击乐记谱、铜管弱音器这类细节常不可用。
- 术语与排版：声部名与缩写不统一，进乐谱还要重排一遍。

## 收费、授权与替代品

要确认的问题：生成式服务的产出归谁，免费档是否要求署名？上传的草图是否被用于训练？商用发行与影视同步各需要什么授权？生成 MIDI 再分发给乐团或制作方是否允许？

价格：生成式服务按订阅或按量，记谱软件买断或订阅，以官方页面为准；地区可用性以官方页面为准。

替代：记谱软件的展开与编配功能——要确定、可复现、完全在本地时用它；AIVA 一类生成服务——要从零生成而不是配你的草图时换它；NotePerformer 一类回放工具——要更可信的试听而不是配器时换它。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","D4","A4","F4","C4","G3","C3"],"label":"一段被分到四个声部的和弦","label_en":"A chord spread across four parts","hint":"先听中音区是否挤在一起，配器最容易在这里变浑","hint_en":"Hear whether the middle register crowds; orchestration muddies there first"}
```
:::

::: en
## What it finishes for you

Spread a piano score across string, woodwind and brass parts; add a harmony or countermelody under a tune; produce several orchestration options to play through and compare; export multi-track MIDI for a mockup with your own sounds; show students how one idea changes with instrumentation; turn a sketch into something audible so a director or client can react to the direction.

## How you feed it, what it returns

You input MIDI or a piano score plus a description of ensemble, style and mood; you get multi-track MIDI or rendered audio. It does not engrave parts or check playability, so part count, register and breathing need human review. Rule-based functions in notation software are predictable; generative services lean toward rebuilding in a style and may not stay close to your motif.

## Where it shines

- Saves copying and trial time: one motif can be heard in several instrumentations quickly.
- Writes playable parts for non-pianists, avoiding tenths and other unplayable spacing.
- Several options at once make A/B auditioning cheap instead of a rewrite.
- Fits DAWs and notation software; MIDI goes in and sounds can be swapped immediately.
- Rule-based spreading is deterministic and reproducible, which suits teaching and production lines.
- Useful for a rough pre-mockup pass that fixes direction before detail work.

## Where it falls over

- Playing technique: breathing, bowing, slurs and double-stop limits are unknown, so parts look fine and fall apart in rehearsal.
- Balance: register and dynamic sense is missing, woodwind is buried under strings, and inner parts smear together.
- Harmony: spreading amplifies parallel fifths and voice crossing, most audibly in four-part writing.
- Generative drift: rebuilding in a style may not preserve your motif or form, and the result can be unrecognisable.
- Special instruments: harp pedalling, percussion notation and brass mutes are often unusable.
- Naming and layout: part names and abbreviations are inconsistent, so the score needs re-laying out.

## Cost, licence, alternatives

Questions to check: who owns output from a generative service, and does the free tier require credit? Are uploaded sketches used for training? What permissions cover commercial release and sync? May generated MIDI be sent to an orchestra or a production partner?

Price: generative services bill per subscription or per use, notation software is bought outright or subscribed, as stated on the official pages; regional availability is as stated there too.

Alternatives: the spread and arrange functions in notation software when you need deterministic, reproducible, fully local results; a generative service such as AIVA when you want music from scratch rather than your sketch orchestrated; a playback tool such as NotePerformer when you need a more convincing audition rather than orchestration.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","D4","A4","F4","C4","G3","C3"],"label":"A chord spread across four parts","label_en":"A chord spread across four parts","hint":"Hear whether the middle register crowds; orchestration muddies there first","hint_en":"Hear whether the middle register crowds; orchestration muddies there first"}
```
:::
