---
id: "instrumental-timbres-ai"
site: "ai"
cat: "E"
title: "音色选择"
title_en: "Choosing Instrumental Timbres"
summary: "采样、合成与生成音色各有所长，选错是角色错位而非音质问题"
summary_en: "Sampled, synthesized and generated timbres each have a job; the wrong choice is a casting error, not a quality one."
level: "standard"
tags: ["音色", "采样", "合成器", "配器"]
tags_en: ["timbre", "sampling", "synthesis", "orchestration"]
alias: ["音色挑选", "声音来源", "timbre choice"]
order: 6
links: ["[[glossary:timbre]]", "[[instrument:samplers]]", "[[instrument:piano]]"]
instances: ["atepp-001283", "atepp-001868", "mutopia-000437", "giantmidi-003765"]
sources: ["采样、合成与生成音色的差别，对照配器与合成器惯例整理。", "(Sampled, synthesized and generated timbres)."]
updated: "2026-11-03"
---

::: zh
## 症状与位置

同一个 part，用采样、合成器还是生成音色，差别不只是“像不像真的”，而是“像不像这个角色”。采样像录音，合成像设计，生成像拼贴。音色不是越贵越好，是越合适越好。最常见的错误是音色很漂亮，但和乐句对不上，整段听着像贴上去的。

## 为什么会这样

采样保留真实乐器的噪声、共鸣和演奏动作，但动态层有限，同一个音重复多了会露出“同一份录音”的痕迹。合成器可以连续控制亮度、包络和失谐，却没有身体，长音容易死。同一个音色在不同音区也会变，低音区松、高音区紧是常态。生成音色介于两者之间，新颖、有细节，但通常不可分层编辑。判断标准不是新旧，而是这个 part 需要什么，持续、颗粒、噪声，还是一个清楚的起音。

## 怎么修

先给每个 part 写功能，低音支撑、节奏骨架、色彩、旋律。独奏旋律优先采样或真人，持续音床可以用合成器，生成音色放在中景和效果层。检查起音和释放是否跟乐句一致，弦乐长音要有渐强，铜管要有起吹的延迟。把候选音色放进同一句里，音量对齐后 A/B，别在独奏时比。换音色比改音符便宜。给每个候选音色录同一句，隔一天再听。最后听它在整个织体里是否还站得住，站不住就换，不要靠加混响救。

## 耳朵要抓的点

下方可比较同一组音名的 GM 采样音色与浏览器合成近似。它们是当前音源的回放，不代表原演奏或原乐器录音。真实拨弦噪声、琴体共鸣和录音空间，需要另用获准的原始音频判断。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","E4","G4","E4","C4","G3"],"label":"音色与短句练习","label_en":"Timbre and phrase exercise","hint":"浏览器合成示意；不是模型输出或处理前后对比。","hint_en":"A browser-synthesized exercise, not model output or a processing comparison."}
```
:::

::: en
## Symptom and location

The same part played by a sample library, a synthesiser or a generated timbre differs in more than realism. It differs in casting. Samples sound recorded, synths sound designed, generated tones sound collaged. The usual mistake is a beautiful timbre that does not fit the phrase, so the part sits on top of the arrangement instead of inside it.

## Why it happens

Samples preserve the noise, resonance and playing action of a real instrument, but they have a limited number of dynamic layers; repeat one note often enough and the same recording shows through. A synth can sweep brightness, envelope and detune continuously, but it has no body, and long notes tend to die. Generated timbres sit between the two: novel and detailed, usually not editable in layers. The test is not old against new. It is whether the part needs sustain, grain, noise or a clear attack.

## How to fix it

Write a function for every part first: bass support, rhythmic frame, colour, melody. Give solo lines to samples or a player, use synths for sustained beds, and put generated timbres in the middle ground and effects layer. Check that attack and release match the phrase; string lines need a swell, brass needs the delay before the note speaks. Put candidates on the same phrase, match loudness, then compare. Finally, hear whether the timbre still holds inside the full texture. If it does not, replace it rather than adding reverb to rescue it.

## What the ear catches

Below, compare GM sampled timbre with a browser-synthesized approximation using the same pitches. These are renderings by the current sound generators, not the original performance or instrument recording. Assess actual string noise, body resonance and recording space with authorized source audio.

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","E4","G4","E4","C4","G3"],"label":"Timbre and phrase exercise","label_en":"Timbre and phrase exercise","hint":"A browser-synthesized exercise, not model output or a processing comparison.","hint_en":"A browser-synthesized exercise, not model output or a processing comparison."}
```
:::

