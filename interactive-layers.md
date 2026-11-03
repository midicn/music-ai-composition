---
id: "interactive-layers"
site: "ai"
cat: "F"
title: "交互分层"
title_en: "Interactive Layers"
summary: "引擎要的是能单独成立、能随时开关的分层文件"
summary_en: "An engine needs layers that stand alone and can be switched at any bar"
level: "standard"
tags: ["分层", "分轨", "循环点", "电平"]
tags_en: ["layers", "stems", "loop points", "levels"]
alias: ["分层配乐", "互动分层", "interactive layers"]
order: 8
links: ["[[glossary:stems]]", "[[glossary:daw]]"]
instances: []
sources: ["https://www.fmod.com/docs/2.04/studio/authoring-events.html", "https://www.fmod.com/docs/2.04/studio/glossary.html"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论交互层与过渡条件，需要对照引擎事件文档并测试实际多层音频资产；单个曲库MIDI不含独立层开关，不能证明运行时分层与切换。"
---

::: zh
## 阻碍在哪

把一首完整混音交给游戏团队，他们没法用。引擎需要在战斗时加鼓、在潜行时只留低频、在剧情时淡出。这些操作要求各层是干净的分轨，有统一的起点、统一的长度、统一的电平。生成工具默认给的是成品混音，拆层往往比重新做还慢。

## 它怎么运转

引擎混音和 DAW 混音不一样，它按状态在运行时开关，没有人在旁边推推子。所以每一层必须能单独听而不空，合起来又不打架。层与层之间的电平差要预先设计，否则战斗层一开就盖住对白。循环点、静音段、尾音都要在文件里说清楚，不能靠猜。分层的单位是功能而不是乐器，一把大提琴可能同时属于低频层和旋律层。

## 怎么调整

按功能分层，低频、和声、旋律、打击、氛围，每层一个立体声文件，采样率和位深统一。所有层从同一小节开始，长度取整小节。层内避免长混响，尾音单独留在最后一小节。命名写清项目、状态、层名、BPM、调性、版本。交付前把每一层单独听一遍，再全部叠起来听一遍。层的数量控制在五六层以内，再多引擎和人都管不过来。交付包附一份说明，写清层与状态的对应关系。
:::

::: en
## Where it blocks

Hand a game team a finished mix and they cannot use it. The engine needs to add drums in combat, leave only low end in stealth, fade out under a story beat. That requires clean layers with one start point, one length and one level. Generation tools deliver a finished mix, and separating it afterwards often takes longer than rebuilding it.

## How it runs

Engine mixing differs from DAW mixing. It switches stems on and off at runtime with nobody riding a fader, so every layer must sound complete on its own and still fit when stacked. Level differences between layers have to be designed in advance, or the combat layer buries dialogue the moment it starts. Loop points, silence and tails must be stated in the file rather than guessed. Layers are divided by function, not by instrument; a single cello may belong to both the low layer and the melody layer.

## How to adjust

Split by function, low end, harmony, melody, percussion, atmosphere, one stereo file each, with matching sample rate and bit depth. Start every layer at the same bar and keep lengths to whole bars. Avoid long reverb inside a layer and leave tails in the final bar. Name files with project, state, layer, BPM, key and version. Listen to each layer alone before delivery, then to all of them together. Keep the count to five or six; beyond that neither the engine nor the team can track them. Ship a note that maps every layer to its states.
:::

