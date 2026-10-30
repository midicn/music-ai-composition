---
id: interactive-layers
site: ai
cat: F
title: 交互分层
title_en: Interactive Layers
summary: 引擎要的是能单独成立、能随时开关的分层文件
summary_en: An engine needs layers that stand alone and can be switched at any bar
level: standard
tags: [分层, 分轨, 循环点, 电平]
tags_en: [layers, stems, loop points, levels]
alias: [分层配乐, 互动分层, interactive layers]
order: 8
links:
  - "[[glossary:stems]]"
  - "[[glossary:daw]]"
instances:
  - musicnet-000067 | 四件乐器各自独立，分层的参照（C1）
  - m21-000020 | 四声部进出清楚，适合拆层（C1）
  - oga-000287 | 电子循环靠增减元素维持律动，听层间关系（C1）
sources:
  - 交互分层的文件组织与电平设计，依游戏音频通识核对，未抄原文
  - Interactive layer organization and level design, checked against general game audio practice, not copied
updated: 2026-10-30
---

::: zh
## 问题

把一首完整混音交给游戏团队，他们没法用。引擎需要在战斗时加鼓、在潜行时只留低频、在剧情时淡出。这些操作要求各层是干净的分轨，有统一的起点、统一的长度、统一的电平。生成工具默认给的是成品混音，拆层往往比重新做还慢。

## 原理

引擎混音和 DAW 混音不一样，它按状态在运行时开关，没有人在旁边推推子。所以每一层必须能单独听而不空，合起来又不打架。层与层之间的电平差要预先设计，否则战斗层一开就盖住对白。循环点、静音段、尾音都要在文件里说清楚，不能靠猜。分层的单位是功能而不是乐器，一把大提琴可能同时属于低频层和旋律层。

## 做法

按功能分层，低频、和声、旋律、打击、氛围，每层一个立体声文件，采样率和位深统一。所有层从同一小节开始，长度取整小节。层内避免长混响，尾音单独留在最后一小节。命名写清项目、状态、层名、BPM、调性、版本。交付前把每一层单独听一遍，再全部叠起来听一遍。层的数量控制在五六层以内，再多引擎和人都管不过来。交付包附一份说明，写清层与状态的对应关系。

## 听什么

在贝多芬第十五弦乐四重奏里听四件乐器怎样各自独立又合得起来，在巴赫众赞歌里听四个声部的进出有多清楚，在 quantum-2 的循环版里听电子层怎样靠增减元素维持同一律动。分层的标准是每一层都能单独成立。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","C4","E4","G4","E4","C4","C3"],"label":"四层叠起来的和弦","label_en":"Four layers stacked into one chord","hint":"逐层关掉，听每一层单独是否还站得住","hint_en":"Mute layer by layer and hear whether each still stands alone"}
```
:::

::: en
## The problem

Hand a game team a finished mix and they cannot use it. The engine needs to add drums in combat, leave only low end in stealth, fade out under a story beat. That requires clean layers with one start point, one length and one level. Generation tools deliver a finished mix, and separating it afterwards often takes longer than rebuilding it.

## How it works

Engine mixing differs from DAW mixing. It switches stems on and off at runtime with nobody riding a fader, so every layer must sound complete on its own and still fit when stacked. Level differences between layers have to be designed in advance, or the combat layer buries dialogue the moment it starts. Loop points, silence and tails must be stated in the file rather than guessed. Layers are divided by function, not by instrument; a single cello may belong to both the low layer and the melody layer.

## Practice

Split by function, low end, harmony, melody, percussion, atmosphere, one stereo file each, with matching sample rate and bit depth. Start every layer at the same bar and keep lengths to whole bars. Avoid long reverb inside a layer and leave tails in the final bar. Name files with project, state, layer, BPM, key and version. Listen to each layer alone before delivery, then to all of them together. Keep the count to five or six; beyond that neither the engine nor the team can track them. Ship a note that maps every layer to its states.

## What to listen for

In Beethoven's String Quartet No. 15, how four instruments stay independent and still cohere; in the Bach chorale, how clearly the four voices enter and leave; in the loop version of quantum-2, how electronic layers keep one groove by adding and removing elements. The test of a layer is whether it stands alone.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","C4","E4","G4","E4","C4","C3"],"label":"Four layers stacked into one chord","label_en":"Four layers stacked into one chord","hint":"Mute layer by layer and hear whether each still stands alone","hint_en":"Mute layer by layer and hear whether each still stands alone"}
```
:::
