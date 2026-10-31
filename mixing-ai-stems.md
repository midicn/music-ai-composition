---
id: mixing-ai-stems
site: ai
cat: D
title: 混 AI 分轨
title_en: Mixing AI Stems
summary: 分轨是 AI 出的，混音顺序不能照搬录音素材的那一套
summary_en: When the stems come from AI, the order of work has to change before the first fader moves.
level: standard
tags: [AI 分轨, 混音顺序, 串音, 相位]
tags_en: [AI stems, mix order, bleed, phase]
alias: [混分轨, 分轨混音, mixing AI stems]
order: 1
links:
  - "[[glossary:stems]]"
  - "[[glossary:phase-check]]"
  - "[[glossary:gain-staging]]"
instances:
  - musicnet-000067 | 贝多芬第十五四重奏首乐章，同族声部串音最难分，听中频是否变薄（C1）
  - groove-000002 | 86 BPM 灵魂乐鼓组，听每一击的重量，AI 分轨常把重音抹平（C1）
  - atepp-005385 | 拉威尔《绞刑架》，低音钟声与和弦之间的低频最容易留残渣（C1）
sources:
  - AI 分轨的串音与相位特征，对照源分离与混音实践惯例整理。
  - Stem-level gain staging and phase checks — based on general mixing practice.
updated: 2026-10-30
---

::: zh
## 要解决的事

AI 分轨拿到手，第一印象往往是干净。没有房间串音，没有话筒漏音，也没有演奏失误。戴上耳机单独听一遍，另一类问题才出现。声部之间互相渗，低频被分离算法削薄，鼓的每一击都一样重，间奏和副歌一样满。照录音分轨的老顺序先均衡再压缩，会把这些毛病放大。

## 背后的机制

录音分轨的串音来自同一个房间，是延迟和衰减，听起来像空间。AI 分轨的串音来自频谱估计，是残渣，听起来像水声或空洞。生成模型一次给出整体混音，声部常由分离或分层生成，相位关系没有保证，低频尤其容易互抵。动态方面，模型倾向输出已经限幅的素材，弱段不弱，强段不强。这些差异决定了顺序要改，先修结构与电平，再谈音色。

## 从哪开始

按四步走。第一步听整体，删掉重复层，AI 常生成两条几乎一样的铺底，留一条就少一处遮蔽。第二步查相位与极性，把底鼓和贝斯放在单声道里听，低频变薄就翻极性或微移时间。第三步修动态，用片段增益或音量自动化把弱段拉回来，扩展器放在压缩之前，门限只处理串音严重的段落。第四步才做均衡与压缩，非低频轨高通从 80 到 120 Hz 起，冲突处用窄切，不做大面积提亮。空间处理放最后，混响会掩盖串音，也会让判断失准。每改一步回到整体听十秒，solo 只用来确认问题，不用来做决定。

## 耳朵要抓的点

在贝多芬第十五弦乐四重奏的第一乐章里，听四把同族乐器怎样互相渗，分离之后中频会变薄。在 86 BPM 的灵魂乐鼓组里，听每一击的重量是否一致，AI 分轨常把重音抹平。在拉威尔《绞刑架》里，听低音钟声与和弦之间的低频，分离残渣最容易堆在这里。三处都先听整体，再用 solo 对照。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["A2","A2","C3","E3","D3","C3","A2","G2"],"label":"分轨里的贝斯","label_en":"A bass in the stems","hint":"先听低频是否连续，再听它与底鼓重叠的那一段","hint_en":"Hear whether the low end stays continuous, then the stretch where it overlaps the kick"}
```
:::

::: en
## The problem to solve

An AI stem pack looks clean at first. No room bleed, no mic leakage, no wrong notes. Solo a track and another set of problems appears. Parts leak into each other, the low end has been scooped by the separation model, every drum hit lands with the same weight, and the bridge is as full as the chorus. Running the recorded-stem order of EQ then compression makes these problems louder.

## The mechanism

Bleed in a recorded stem comes from one room, so it arrives as delay and decay and reads as space. Bleed in an AI stem is spectral estimation residue; it sounds watery or hollow. A generative model returns a whole mix at once, and the parts are separated or generated in layers, so phase relationships are not guaranteed and low frequencies cancel easily. Dynamics are usually already limited, with weak sections as loud as strong ones. Those differences change the order of work, fix structure and level first, tone later.

## Where to start

Four passes. Listen to the whole and delete duplicate layers, since generators often produce two near-identical pads and keeping one removes a masking problem outright. Check polarity and phase with kick and bass in mono, flipping polarity or nudging timing if the low end thins. Repair dynamics with clip gain or volume automation before any compressor, using an expander ahead of compression and gating only the worst bleed. Only then do EQ and compression, high-passing non-bass parts at 80 to 120 Hz and cutting narrow bands at conflicts instead of boosting broad ones. Leave space until the end, because reverb hides bleed and blurs judgement. After each move, return to the full mix for ten seconds. Solo confirms a problem but should not decide it.

## What the ear catches

In the first movement of Beethoven's String Quartet No. 15, hear how four instruments of one family bleed into each other and how the midrange thins after separation. In the 86 BPM soul groove, hear whether every hit carries the same weight, since AI stems tend to flatten accents. In Ravel's Le gibet, listen to the low end between the bell and the chords, where separation residue collects. Judge in context first and use solo only to confirm.

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["A2","A2","C3","E3","D3","C3","A2","G2"],"label":"A bass in the stems","label_en":"A bass in the stems","hint":"Hear whether the low end stays continuous, then the stretch where it overlaps the kick","hint_en":"Hear whether the low end stays continuous, then the stretch where it overlaps the kick"}
```
:::
